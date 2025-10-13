
<!-- README.md is generated from README.Rmd. Please edit that file -->

<img src="images/logo_tum.png" width="250"/>
<img src="images/logo_with_text-01.png" width="300"/>

<img src="images/logo_banner.png"/>

### Personal light exposure dataset for Munich, Germany; collected by the Technical University of Munich (TUM) following the protocol of Guidolin et al. 2024 (MeLiDos field study)

**Version v1.0.1**

<!-- badges: start -->

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.16893901.svg)](https://doi.org/10.5281/zenodo.16893901)
<!-- badges: end -->

<figure>
<img src="output/figures/Figure_1.png"
alt="Overview of light exposure data. (A) location of data collection. (B) collection periods for participants, (C) photoperiods, and (D) double plot of median, interquartile range (50%), 75%, and 95% ribbons of light exposure across all participants. Shaded areas indicate nighttime from civil dusk to civil dawn." />
<figcaption aria-hidden="true">Overview of light exposure data. (A)
location of data collection. (B) collection periods for participants,
(C) photoperiods, and (D) double plot of median, interquartile range
(50%), 75%, and 95% ribbons of light exposure across all participants.
Shaded areas indicate nighttime from civil dusk to civil
dawn.</figcaption>
</figure>

### About this repository

This repository contains the comprehensive dataset for the
[MeLiDos](www.melidos.eu) field study site of Munich, Germany. Data were
collected by the [Technical University of Munich
(TUM)](https://www.tum.de/en/) and are further processed and analysed by
the [Translational Sensory & Circadian Neuroscience Unit
(TSCN)](https://www.tscnlab.org). A detailed description of the
experiment is available in [Guidolin et al.,
2024](https://www.ncbi.nlm.nih.gov/pubmed/39592960).

This repository is transitioning towards a
[FAIR](https://www.go-fair.org/fair-principles/) and fully human and
machine-readable light exposure dataset, based on a [community-based and
peer-reviewed Metadata
descriptor](https://bmcdigitalhealth.biomedcentral.com/articles/10.1186/s44247-024-00113-9).
As part of this transition, files will be converted from
semi-rectangular data, to fully [tabular
data](https://specs.frictionlessdata.io/tabular-data-package/). Further,
metadata will be added and converted from XLSX to JSON. For full
traceability, all versions will be archived in
[Zenodo](https://zenodo.org) and are accessible through their own
persistent identifier (DOI).

### Citation

APA reference:

> Hilden, S., Lee, S., Zauner, J., & Spitschan, M., (2025). Personal
> light exposure dataset for Munich, Germany (Version 1.0.1) \[Data
> set\]. URL:
> <https://github.com/MeLiDosProject/HildenEtAl_Dataset_2025>. DOI:
> doi.org/10.5281/zenodo.16893901

## Summary of the dataset

| Dataset name | TUM |
|----|----|
| Period of data collection (total) | May 2024 to July 2024 |
| Location | Munich, Germany |
| Number of participants enrolled | N=10 |
| Number of participants included in data analysis and this repository | N=10 |
| Duration of experiment for each participant | N=7 days (Monday to Monday) |

### Included files

The following files are included with this Dataset:

- `data/Metadata_Melidos_TUM.xlsx`: Preliminary Metadata prior to
  conversion to JSON
  <!-- - `data/Study_dates_MeLiDos_FUSPCEU.xlsx`: Recruitment dates to clean light exposure recordings -->

- `data`: Folder with measurement and project data in the following
  structure:

<!-- -->

        data/
            raw/
                group/
                   demographics/
                   discharge/
                   screening/
                individual/
                   $ParticipantID/
                         chronotype/
                         continuous/
                             actlumus_wrist/
                             actlumus_head/
                             actlumus_chest/
                             currentconditions/
                             exercisediary/
                             experiencelog/
                             mHLEA_digital/
                             mHLEA_paper/
                             sleepdiary/
                             wearlog/
                             wellbeingdiary/
                         demographics/
                         discharge/
                         screening/

- `LICENSE`: Licensing terms. This dataset is published with a
  permissive CC-BY-4.0 license

All data are anonymous.

# Folder structure

## Group

This folder contains grouped data, i.e. any data that are collected at
the group level and/or were grouped to facilitate import during
analyses.

| Folder name | Content |
|----|----|
| **demographics** | N=10 csv files. Contains demographic information for each participant. |
| **discharge** | N=10 csv files, which contains answers from all questionnaires that N=10 participants had to fill at discharge: 1) Light Exposure Behaviour Assessment (LEBA instrument), 2) Visual Light Sensitivity Questionnaire-8 (VLSQ-8), 3) Assessment of Sleep Environment (ASE) questionnaire, 4) Modified Theory Framework of Acceptability (mTFA) questionnaire, 5) Feedback (1 Y/N and multiple choice questions). |
| **screening** | N=10 csv files for N=10 participants containing screening information. |

## Individual

This folder contains individual-level data for N=10 participant, each
stored in a separate folder named after the participant ID (PID). The
data within each participant folder follows the following structure.

| Folder name | Content |
|----|----|
| **continuous/actlumus_chest** | txt files from ActLumus worn at chest level, one for each participant. Also, a report (`_Report`) from the device. |
| **continuous/actlumus_head** | txt files from ActLumus worn at eye level, one for each participant. Also, a report (`_Report`) from the device. |
| **continuous/actlumus_wrist** | txt files from ActLumus worn at the wrist, one for each participant. Also, a report (`_Report`) from the device. |
| **continuous/currenconditions/** | Questionnaire comprising 3 questionnaires on 1) current mood (MoodZoom), 2) light conditions (custom) and 3) alertness (Karolinska Sleepiness Scale). Completed 4/times per day, at 11:00, 14:00, 17:00 and 20:00. Participants instructed to completed as close as possible to the indicated times. The participant sometimes additionally reported upon waking and before going to bed. |
| **continuous/exercisediary/** | Custom made questionnaire on exercise. Completed daily in the evening |
| **continuous/experiencelog/** | Custom made questionnaire about experiences wearing the light glasses. Completed any time participant had an experience to report (no restrictions). |
| **continuous/mHLEA_digital/** | Custom made questionnaire to test Daily in the evening |
| **continuous/mHLEA_paper/** | Custom made paper-based questionnaire to test Daily in the evening. This was transcribed to xlsx files by the experimenter after study end for each participant. |
| **continuous/sleepdiary/** | Daily in the morning |
| **continuous/wearlog/** | Any time participant had removed or started wearing the light logger |
| **continuous/wellbeingdiary/** | Daily in the evening |
| **chronotype/** | Munich Chronotype Questionnaire (MCTQ) & Morning Eveningness Questionnaire (MEQ) completed at study intake (Monday, day 1) |
| **demographics/** | Screening questionnaire containing demographic and health information. Completed online before study intake. |
| **discharge/** | n=1 csv file with LEBA, VLSQ8, feedback, mTFA, and ASE. Completed at discharge (Monday, day 8). |
| **screening** | N=1 csv file containing screening information. |
