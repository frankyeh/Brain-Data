# Queensland Twin Adolescent Brain (QTAB)

Queensland Twin Adolescent Brain (QTAB) project was established with the purpose of promoting the conduct of health-related research in adolescence.

The project scans adolescent twins at two sessions (session 1: N = 422, age 9-14 years; session 2: N = 304, 10-16 years). The MRI protocol included T1-weighted (MP2RAGE), T2-weighted, FLAIR, high-resolution TSE, SWI, resting-state fMRI, DWI, and ASL scans. Two fMRI tasks were added in session 2 to probe emotion-relevant neural processes (emotional conflict task) and evoke activity in the Theory of Mind network (passive movie watching task). 

The cognitive and mental health data were also collected. The cognitive function was accessed using standardised tests, obtained self-reports of symptoms for anxiety and depression, perceived stress, sleepiness, as well as measures of pubertal development, peer relationships, early life factors, and family sociodemographic factors. Additional biological samples for genomic and metagenomic analysis were also collected. 

# Source and Citation

https://openneuro.org/datasets/ds004146/versions/1.0.0

Strike, Lachlan T. and Hansell, Narelle K. and Miller, Jessica L. and Chuang, Kai-Hsiang and Thompson, Paul M. and de Zubicaray, Greig I. and McMahon, Katie L. and Wright, Margaret J. (2022). Queensland Twin Adolescent Brain (QTAB). OpenNeuro. [Dataset] doi: doi:10.18112/openneuro.ds004146.v1.0.0

# Download

- [SRC Files (topup/eddy corrected DWI signals)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EuXbJayHWkBBsjR7ndjGKlUBLFo54qBOPvcSU6e8B1yJXw?e=heNzR9)
- [FIB Files (ready-to-track files)](https://pitt-my.sharepoint.com/:f:/g/personal/yehfc_pitt_edu/EsmXfM8VtvZMhSCrmMTI4q4Ba0qB5k37fPCkBnl4wOouTA?e=HlNjkP)
- Tractography results (pending)
- [Basic demographic data](https://openneuro.org/crn/datasets/ds004146/snapshots/1.0.0/files/participants.tsv)
- Restricted demographic data: (i.e., age in months, zygosity, multiple birth status, birth order), as well as non-imaging phenotypic data is stored at The University of Queensland's institutional repository, UQ eSpace (https://doi.org/10.48610/e891597). Access to the dataset can be requested via the "Request access to the dataset link" in the UQ eSpace record.


# Methods

## Reconstruction

> A multishell diffusion scheme was used, and the b-values were 1000 and 3000 s/mm². The number of diffusion sampling directions were 10 and 30, respectively. The in-plane resolution was 2 mm. The slice thickness was 2 mm. The susceptibility artifact was estimated using reversed phase-encoding b0 by TOPUP from the Tiny FSL package (http://github.com/frankyeh/TinyFSL), a re-compilied version of FSL TOPUP (FMRIB, Oxford) with multi-thread support. FSL eddy was used to correct for eddy current distortion. The correction was conducted through the integrated interface in DSI Studio ("Chen" release)(http://dsi-studio.labsolver.org). The diffusion MRI data were rotated to align with the AC-PC line. The restricted diffusion was quantified using restricted diffusion imaging (Yeh et al., MRM, 77:603–612 (2017)). The diffusion data were reconstructed using generalized q-sampling imaging (Yeh et al., IEEE TMI, ;29(9):1626-35, 2010) with a diffusion sampling length ratio of 1.25. The tensor metrics were calculated using DWI with b-value lower than 1750 s/mm². The preprocessing was conducted using the cluster resources at 'Advanced Cyberinfrastructure Coordination Ecosystem: Services & Support' (ACCESS) under allocation CIS200026.

> A deterministic fiber tracking algorithm (Yeh et al., PLoS ONE 8(11): e80713, 2013) was used with augmented tracking strategies (Yeh, Neuroimage, 2020 Dec;223:117329) to improve reproducibility. The anatomy prior of a tractography atlas (Yeh et al., Neuroimage 178, 57-68, 2018) was used to map Arcuate_Fasciculus_L  with a distance tolerance of 16 (mm) in the ICBM152 space. An ROA was placed at track tolerance region (36,47,33) . The track-to-voxel ratio was set to 2. The anisotropy threshold was randomly selected. The angular threshold was randomly selected from 15 degrees to 90 degrees. The step size was randomly selected from 0.5 voxel to 1.5 voxels. Tracks with length shorter than 30 or longer than 300 mm were discarded. Topology-informed pruning (Yeh et al. Neurotherapeutics, 16(1), 52-58, 2019) was applied to the tractography with 32 iteration(s) to remove false connections. Shape analysis (Yeh, Neuroimage, 2020 Dec;223:117329) was conducted to derive shape metrics for tractography.


# Script

**1. Download and convert to SRC files**

```
aws s3 sync --no-sign-request --region eu-west-1 --exclude "*" --include "*dwi.*" s3://openneuro.org/ds004146 ds004146 
```

After download the files, all nifti, bval, and bvec files were moved to the same directory before running the following script:

```
#!/bin/bash
for sub in $(ls *_ses-01_dir-AP_run-01_dwi.nii.gz)
do    
    singularity exec /ocean/projects/cis200024p/frankyeh/dsistudio_latest.sif dsi_studio --action=src --source=${sub:0:12}-01_dir-AP_run-01_dwi.nii.gz --other_source=${sub:0:12}-02_dir-AP_run-01_dwi.nii.gz --output=${sub:0:12}.ap.src.gz > ${sub:0:12}.ap.log.txt
    singularity exec /ocean/projects/cis200024p/frankyeh/dsistudio_latest.sif dsi_studio --action=src --source=${sub:0:12}-01_dir-PA_run-01_dwi.nii.gz --other_source=${sub:0:12}-02_dir-PA_run-01_dwi.nii.gz --output=${sub:0:12}.pa.src.gz > ${sub:0:12}.pa.log.txt
done

```

**2. TOPUP/EDDY and save corrected SRC files**

Correct artifacts using AP and PA SRC files and generate corrected AP-PA combined SRC files.
The script needs a number input that allows for running the task using clusters job arrary

```
#!/bin/bash
subs_ap=$(ls -Lr *AP.nii.gz.src.gz)
subs_ap=(${subs_ap// /})
subs_pa="${subs_ap[$1]:0:28}PA.nii.gz.src.gz"
if [ ! -e $sub_pa ]; then
     echo "." > ${sub_pa}_not_found.txt
else    
     echo "processing ${subs_ap[$1]}"
     dsi_studio --action=rec --source=${subs_ap[$1]} --rev_pe=${subs_pa} --cmd="[Step T2][File][Save Src File]=${subs_pa:0:10}.src.gz"
fi
```

The following is the job array to run the above script using sbatch. The script needs an the file name of the script to run the job array.

```
#!/bin/bash
#SBATCH -t 24:00:00
#SBATCH -p RM-shared
#SBATCH -N 1
#SBATCH --ntasks-per-node 8
#SBATCH --mem=15GB
#SBATCH --array=0-999
set -x
sh $1 $SLURM_ARRAY_TASK_ID
```

**3. reconstruction**

The following command generate native space FIB files for automatic fiber tracking
```
dsi_studio --action=rec --source=*.src.gz
```

The following command generate template space FIB files for correlational tractography
```
dsi_studio --action=rec --source=*.src.gz --method=7 --template=0 --record_odf=1 --dti_no_high_b=1
```

