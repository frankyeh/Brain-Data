The MPI-Leipzig Mind-Brain-Body dataset contains MRI and behavioral data from 318 participants. Datasets for all participants include at least a structural quantitative T1-weighted image and a single 15-minute eyes-open resting-state fMRI session.
 
The participants took part in one or two extended protocols: Leipzig Mind-Brain_BodyInteractions (LEMON) and Neuroanatomy & Connectivity Protocol (N&C). The data from LEMON protocol is included in the ‘ses-01’ subfolder; the data from N&C protocol in ‘ses-02’ subfolder.

LEMON focuses on structural imaging. 228 participants were scanned.  In addition to the quantitative T1-weighted image (MP2RAGE, from 227 participants), the participants also have a structural T2-weighted image (225), a diffusion-weighted image with 60 directions (228) and a 15-minute eyes-open resting-state session (227) including scans for geometric distortion correction in DWI and rs-fMRI. Updated imaging sequences were introduced into the LEMON protocol after data acquisition for 112 participants. Before the change, a low-resolution 2D FLAIR image was acquired for for radiological screening (111). After the change, 2D FLAIR was replaced with high-resolution 3D SPACE sequence with fluid-attenuated inversion-recovery preparation (116). The second update  was a change from a Siemens product Susceptibility-Weighted Imaging (SWI) sequence (109) to an in-house SWI sequence (114). The in-house sequence allows both magnitude and phase data to be stored, enabling offline processing and Quantitative Susceptibility Mapping (QSM). 
The N&C protocol focuses on resting-state fMRI data. 199 participants were scanned with this protocol; 109 participants also took part in the LEMON protocol. Structural data was not acquired for the overlapping LEMON participants. For the unique N&C participants, only a T1-weighted and a low-resolution FLAIR image were acquired. Four 15-minute runs of eyes-open resting-state are the main component of N&C; they are complete for 194 participants, three participants have 3 runs, one participant has 2 runs and one participant has a single run. Due to a bug in multiband sequence used in this protocol, the echo time for N&C resting-state is longer than in LEMON — 39.4 ms vs 30 ms.

Forty-five participants have complete imaging data: quantitative T1-weighted, T2-weighted, high-resolution 3D FLAIR, DWI, SWI sequence allowing QSM, and 75 minutes of resting-state. Both gradient-echo and spin-echo field maps are available in both datasets for all EPI-based sequences (rsfMRI and DWI).

Extensive behavioral data was acquired in both protocols. They include trait and state questionnaires, as well as behavioral tasks. Here we only list the tasks and more extensive descriptions are available in the manuscripts.

# LEMON QUESTIONNAIRES/TASKS
Cognitive Test Battery
California Verbal Learning Test (CVLT)
Testbatterie zur Aufmerksamkeitsprüfung (TAP: Alertness, Incompatibility, Working Memory)
Trail Making Test (TMT: A, B)
Wortschatztest (WST)
Leistungsprüfungssystem 2 (LPS-2: Subset 3)
Regensburger Wortflüssigkeitstest (RWT: S-Words, Animals,)

Emotion and Personality Test Battery
NEO Five-Factor Inventory (NEO-FFI)
Impulsive Behavior Scale (UPPS)
Behavioral Inhibition and Approach System (BISBAS)
Cognitive Emotion Regulation Questionnaire (CERQ)
Measure of Affective Style (MARS)
Fragebogen zur Sozialen Unterstützung (F-SozU K-22)
The Multidimensional Scale of Perceived Social Support (MSPSS)
Coping Orientations to Problems Experienced (COPE)
Life Orientation Test-Revised (LOT-R)
Perceived Stress Questionnaire (PSQ)
Trier Inventory of Chronic Stress (TICS)
Three-factor eating questionnaire (TFEQ)
Yale Food Addiction Scale (YFAS)
The Trait Emotional Intelligence Questionnaire (TEIQue-SF)
Trait Scale of the State-Trait Anxiety Inventory (STAI)
State-Trait Anger expression Inventory (STAXI)
Toronto-Alexithymia Scale (TAS)
Multidimensional Mood Questionnaire (MDBF)
New York Cognition Questionnaire (NYC-Q)
Future Time perspective (FTP)
Three-factor Eating Questionnaire (FEV)

Physiological measures 
Resting-state EEG
Continuous Peripheral Physiological Recordings During rs-fMRI (ECG, pulse, respiration, beat-to-beat blood pressure)
Seated Resting Blood Pressure    
Blood Drawing    
Anthropometry    
Hair Sample

Assessment of Past and Present Psychiatric Symptoms
Standardized Clinical Interview for DSM IV (SCID-I)    
Screening for Clinically Relevant Symptoms (HAM-D, BSL-23)     
Screening for Alcohol Abuse (AUDIT)    
Screening for Substance Abuse

# N&C QUESTIONNAIRES
Adult Self Report (ASR)
Goldsmiths Musical Sophistication Index (Gold-MSI)
Internet Addiction Test (IAT)
Involuntary Musical Imagery Scale (IMIS)
Multi-Gender Identity Questionnaire (MGIQ)
Brief Self-Control Scale (SCS)
Short Dark Triad (SD3)
Social Desirability Scale-17 (SDS)
Self-Esteem Scale (SE)
Tuckman Procrastination Scale (TPS)
Varieties of Inner Speech (VISQ)
UPPS-P Impulsive Behavior Scale (UPPS-P)
Attention Control Scale (ACS)
Beck's Depression Inventory-II (BDI)
Boredom Proneness Scale (BP)
Esworth Sleepiness Scale (ESS)
Hospital Anxiety and Depression Scale (HADS)
Multimedia Multitasking Index (MMI)
Mobile Phone Usage (MPU)
Personality Style and Disorder Inventory (PSSI)
Spontaneous and Deliberate Mind-Wandering (S-D-MW)
Short New York Cognition Scale (Short-NYC-Q)
New York Cognition Scale (NYC-Q)
Abbreviated Math Anxiety Scale (AMAS)
Behavioral Inhibition and Approach System (BIS/BAS)
NEO Personality Inventory Revised (NEO-PI-R)
Body Consciousness Questionnaire (BCQ)
Creative achievement questionnaire (CAQ)
Five facets of mindfulness (FFMQ)
Metacognition (MCQ-30)

# N&C TASKS
Conjunctive continuous performance task (CCPT)
Emotional task switching (ETS)
Adaptive visual and auditory oddball target detection task (Oddball)
Alternative uses task (AUT)
Remote associates test (RAT)
Synesthesia color picker test (SYN)
Test of creative imagery abilities (TCIA)
## Release Link
https://github.com/data-indi/retro/releases/tag/mpi-lemon
