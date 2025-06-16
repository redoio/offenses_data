# Introduction
Data on the population currently incarcerated in any of the thirty-five state prisons under the jurisdiction of the California Department of Corrections and Rehabilitation (CDCR) as of December 2023. Information was acquired via the California Public Records Act (CPRA). The Department applied several privacy (health information, age, etc.) related exclusionary criteria to release these records to Redo.io. The CDCR identification numbers are hashed to add another layer of privacy and security. 

Note: Data and analyses in this repository are fully independent of the Three Strikes Project, Stanford University and the Resentencing Data Initiative. This is an open data related effort not supported or related to any of the aforementioned parties.

# Citation 

If you make use of our dataset(s), please cite our work as follows: 

"Redo.io. cdcr-offenses-data (Version 1.0.0) [Dataset]. https://github.com/redoio/offenses_data"

# License 

[![License: ODbL](https://img.shields.io/badge/License-ODbL-brightgreen.svg)](https://opendatacommons.org/licenses/odbl/)

This cdcr-offenses-data repository is made available under the Open Database License: http://opendatacommons.org/licenses/odbl/1.0/ by Redo.io. Any rights in individual contents of the database are licensed under the Database Contents License: http://opendatacommons.org/licenses/dbcl/1.0/

# Access 

Our datasets are publicly available and downloadable. For data previews and exploration, you can access the same demographics.csv, current_commitments.csv and prior_commitments.csv data on data.world (log in required).
## `data.world` <img src= "https://github.com/user-attachments/assets/55d79e7d-fece-4b5a-a78d-2a87bb4a8601" width = "3%" height = "3%">

Links:<br>
https://data.world/redoio<br>
https://data.world/redoio/ca-prison-sentences<br>
https://data.world/redoio/ca-prison-former-sentences<br> 

# Data Dictionary 

## Demographics 

Files: `demographics.csv` `demographics.xlsx` 

| variable | type | description |
| ------------ | ------------------- | --------- |
`cdcno`	| str | Unique md5 hash identifier for each individual in the CDCR (California Department of Corrections and Rehabilitation) prison system. Individual is incarcerated or imprisoned in state custody as of December 2023. Note: This data set includes individuals housed in an institution, on temporary release, or in a non-CDCR institution (excluding parolees). Therefore, individuals serving prison sentences in county jails are also included. |
`ethnicity`	| str | Ethnicity or race of the incarcerated person (White, Black, Asian, Hispanic, Pacific Islander, etc.) |
`controlling_offense`	| str | Offense number from the California criminal code (penal code, vehicular code, other) that the incarcerated person is currently serving time for, i.e. main offense that the person is sentenced for hence it "controls" their incarceration (PC187, PC664, PC214(a), etc.) |
`description`	| str | Text description or details about the controlling offense |
`offense_begin_date`	| datetime | Date on which the offense was committed |
`offense_end_date`	| datetime | Date on which the offense was committed |
`controlling_case_number`	| str | Case number of the individual's controlling offense |
`controlling_case_sentencing_county`	| str | County or geographical location where the incarcerated individual was sentenced for their offense. County where the case was deliberated with a judge, defense and prosecutor and the sentence term and length was decided. County that has the authority to decide whether to resentence the individual or provide any other form of relief. 
`sentence_type` |	str | Specifies whether the offense is a second strike or third strike or something else. Indicates the number of serious felonies that the individual committed and has served time for. Third strike felony carries a minimum sentence of 25 years to life. |
`aggregate_sentence_in_months`	| int | Total length of the sentence in months. Numerical count that can be converted to years, decades, etc.<br>Note: Sentences of the type "Condemned" carry a sentence length of 100,000 months or 1,000,000 months. |
`offense_category`	| str | Specifies the nature of the offense (drug related, property related, crimes against a person) |
`erpd_mepd_month_and_year`	| str | Earliest Possible Release Date (EPRD): date determinately-sentenced offenders will be released based on the sentence imposed by the court, less any applicable credits; Minimum Eligible Parole Date (MEPD): date indeterminately-sentenced offenders (i.e., persons sentenced to life with the possibility of parole, or “lifers”) are eligible for parole consideration by the Parole Board based on the sentence imposed by the court, less any applicable credits |
`current_location`	| str | Name of the prison facility where the person is incarcerated (one of CDCR's state prisons - San Quentin, CA Institution for Men, CA Central Women's Facility, etc.) |

## Current Commitments 

Files: `current_commitments.csv` `current_commitments.xlsx` 

| variable | type | description |
| ------------ | ------------------- | --------- |
`cdcno`	| str | Unique md5 hash identifier for each individual in the CDCR (California Department of Corrections and Rehabilitation) prison system. Individual is incarcerated or imprisoned in any one of the state's prisons as of December 2023. |
`sentencing_county`	| str | County or geographical location where the incarcerated individual was sentenced for their offense. County where the case was deliberated with a judge, defense and prosecutor and the sentence term and length was decided. | 
`case_number`	| str | Case number of the individual's offense |
`sentence_from_abstract_of_judgement` | str | Length of the sentence in text form: life without parole, life with parole, 4 years, etc. |
`offense` | str | Offense number from the California criminal code (penal code, vehicular code, other) that the incarcerated person is currently serving time for. |
`offense_description`	| str | Text description or details about the offense. |
`offense_begin_date`	| datetime | Date on which the offense was committed |
`offense_end_date`	| datetime | Date on which the offense was committed |
`in_prison`	| str | Specifies whether the offense was committed in prison or not. This could be a fight with another incarcerated person, defying the order or command of an officer, not following the rules of the facility or prison in any way |
`offense_category`	| str | Specifies the nature of the offense (drug related, property related, crimes against a person, case enhancement) |
`offense_time_with_enhancement` | str | Total months of the sentence taking into account additional months added due to enhancements. For example, a robbery offense may result in a sentence length of 10 years. A robbery with a firearm (enhancement) could result in a sentence of 10 years plus a few additional years. |
`relationship` | str | Specifies whether the sentence was served concurrently, i.e. in parallel to other sentences or if the sentence is being served individually, i.e. no overlap with other sentences |

## Prior Commitments 

Files: `prior_commitments.csv` `prior_commitments.xlsx` 

| variable | type | description |
| ------------ | ------------------- | --------- |
`cdcno`	| str | Unique md5 hash identifier for each individual in the CDCR (California Department of Corrections and Rehabilitation) prison system. Individual is incarcerated or imprisoned in any one of the state's prisons as of December 2023. |
`sentencing_county`	| str | County or geographical location where the incarcerated individual was sentenced for their offense. County where the case was deliberated with a judge, defense and prosecutor and the sentence term and length was decided. | 
`case_number`	| str | Case number of the individual's offense |
`sentence_from_abstract_of_judgement` | str | Length of the sentence in text form: life without parole, life with parole, 4 years, etc. |
`offense` | str | Offense number from the California criminal code (penal code, vehicular code, other) that the incarcerated person served time for and completed their sentence. |
`offense_description`	| str | Text description or details about the offense |
`offense_begin_date`	| datetime | Date on which the offense was committed |
`offense_end_date`	| datetime | Date on which the offense was committed |
`in_prison`	| str | Specifies whether the offense was committed in prison or not. This could be a fight with another incarcerated person, defying the order or command of an officer, not following the rules of the facility or prison in any way |
`offense_category`	| str | Specifies the nature of the offense (drug related, property related, crimes against a person, case enhancement) |
`offense_time_with_enhancement` | str | Total months of the sentence taking into account additional months added due to enhancements. For example, a robbery offense may result in a sentence length of 10 years. A robbery with a firearm (enhancement) could result in a sentence of 10 years plus a few additional years. |
`relationship` | str | Specifies whether the sentence was served concurrently, i.e. in parallel to other sentences or if the sentence is being served individually, i.e. no overlap with other sentences |
`release_date`	| str | Date on which the individual was released from prison after they finished serving the sentence. Since this is a prior offense, it is no longer on the individual's list of current offenses, which means they have served the full sentence stipulated by the court |

# Contact 

Contact aparna.komarla@gmail.com for any questions
