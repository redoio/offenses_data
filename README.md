# Introduction
Data on the population currently incarcerated under the California Department of Corrections and Rehabilitation (CDCR) as of December 2023 and April 2025. Information was acquired via the California Public Records Act (CPRA). The Department applied several privacy (health information, age, etc.) related exclusionary criteria to release these records to Redo.io. The CDCR identification numbers are anonymized for an additional layer of privacy and security. 

Note: Data and analyses in this repository are fully independent of the Three Strikes Project, Stanford University and the Resentencing Data Initiative. This is an open data related effort not supported or related to any of the aforementioned parties.

# Citation 

If you make use of our dataset(s), please cite our work as follows: 

"Redo.io. cdcr-offenses-data (Version 1.0.0) [Dataset]. https://github.com/redoio/offenses_data"

# License 

[![License: ODbL](https://img.shields.io/badge/License-ODbL-brightgreen.svg)](https://opendatacommons.org/licenses/odbl/)

This cdcr-offenses-data repository is made available under the Open Database License: http://opendatacommons.org/licenses/odbl/1.0/ by Redo.io. Any rights in individual contents of the database are licensed under the Database Contents License: http://opendatacommons.org/licenses/dbcl/1.0/

# Access 

Our datasets are publicly available and downloadable. For data previews and exploration, you can access the same demographics.csv, current commitments.csv and prior commitments.csv data on https://data.world (log in required) and the Harvard Dataverse.

Links:<br>
https://data.world/redoio<br>
https://data.world/redoio/ca-prison-sentences<br>
https://data.world/redoio/ca-prison-former-sentences<br>
https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi%3A10.7910%2FDVN%2FQCTMSI

# Data Dictionary

Versions: `2023` and `2025`

## Demographics

Files: `demographics.csv` `demographics.xlsx`<br>

| Variable | Type | Calculated | Description |
| --- | --- | --- | --- |
| `cdcno` | str | No | Unique identifier (MD5 hash) for each individual under CDCR jurisdiction, including those housed in a state prison, temporarily released, or held in a non-CDCR facility. Excludes parolees. Individuals serving CDCR sentences in county jails are included. |
| `ethnicity` | str | No | Race or ethnicity of the incarcerated person (e.g., White, Black, Asian, Hispanic, Pacific Islander). |
| `controlling offense` | str | No | California penal, vehicular, or other code number for the offense governing the individual's current incarceration (e.g., PC187, PC664, PC214(a)). |
| `description` | str | No | Text description of the controlling offense. |
| `offense begin date` | datetime | No | Date the controlling offense began. |
| `offense end date` | datetime | No | Date the controlling offense ended, if applicable. |
| `controlling case number` | str | No | Case number associated with the controlling offense. |
| `controlling case sentencing county` | str | No | County where the individual was sentenced for the controlling offense. |
| `sentence type` | str | No | Indicates whether the individual is sentenced to a Determinate Sentence Length (DSL), Life with Parole, Life Without Parole (LWOP), Third Strike, Second Strike, or Condemned. |
| `aggregate sentence in months` | int | No | Total sentence length in months. Note: "Condemned" sentences are recorded as 100,000 or 1,000,000 months. |
| `offense category` | str | No | Broad category of the offense (e.g., drug crimes, property crimes, crimes against a person). |
| `eprd mepd month and year` | str | No | For determinate sentences: Earliest Possible Release Date (EPRD), calculated from the court-imposed sentence minus applicable credits. For indeterminate sentences: Minimum Eligible Parole Date (MEPD), the earliest date a "lifer" may be considered for parole. |
| `current location` | str | No | Name of the facility where the individual is currently housed. Note: CDCR sentences being served in county jails typically appear as "<County Name> Control Office". |
| `aggregate sentence in years` | float | Yes: `aggregate sentence in months` divided by 12 | Total sentence length in years. |
| `time served` | float | Yes: `today's date` minus `offense end date` | Total sentence length in years that has been completed. Note: This value represents the minimum time served. Because the value is refreshed every 3-4 months, the actual time served at any given point may be greater than what is recorded. |
| `expected release date` | datetime | Yes: `offense end date` + `aggregate sentence in years` | Possible release date based on sentence length and offense date. |

---

## Current Commitments

Files: `current_commitments.csv` `current_commitments.xlsx`

| Variable | Type | Description |
| --- | --- | --- |
| `cdcno` | str | Unique identifier (MD5 hash) for each individual under CDCR jurisdiction, including those housed in a state prison, temporarily released, or held in a non-CDCR facility. Excludes parolees. Individuals serving CDCR sentences in county jails are included. |
| `sentencing county` | str | County where the individual was sentenced for this offense. |
| `case number` | str | Case number associated with this offense. |
| `sentence from abstract of judgement` | str | Sentence as written in the abstract of judgment. Values include Life Without Parole (LWOP), Life With Parole, Condemned, or a specific term in years and months. |
| `offense` | str | California penal, vehicular, or other code number for the offense the individual is currently serving time for. |
| `offense description` | str | Text description of the offense. |
| `offense begin date` | datetime | Date the offense began. |
| `offense end date` | datetime | Date the offense ended, if applicable. |
| `in prison` | str | Indicates whether the offense was committed while incarcerated. |
| `offense category` | str | Broad category of the offense (e.g., drug crimes, property crimes, crimes against a person, case enhancement). |
| `offense time with enhancement` | str | Total sentence length in months, including any enhancements (e.g., additional years added for use of a firearm during a robbery). |
| `relationship` | str | Whether this sentence is served concurrently (overlapping with other sentences) or consecutively (no overlap). |
| `off enh<num>` | str | California penal, vehicular, or other code number for the enhancement associated with the offense. Columns are numbered `off enh1` through `off enh11` and `<num>` is a placeholder for the enhancement count. |
| `off enh desc<num>` | str | Text description of the enhancement. Columns are numbered `off enh desc1` through `off enh desc11` and `<num>` is a placeholder for the enhancement count. |
---

## Prior Commitments

Files: `prior_commitments.csv` `prior_commitments.xlsx`

| Variable | Type | Description |
| --- | --- | --- |
| `cdcno` | str | Unique identifier (MD5 hash) for each individual under CDCR jurisdiction, including those housed in a state prison, temporarily released, or held in a non-CDCR facility. Excludes parolees. Individuals serving CDCR sentences in county jails are included. |
| `sentencing county` | str | County where the individual was sentenced for this offense. |
| `case number` | str | Case number associated with this offense. |
| `sentence from abstract of judgement` | str | Sentence as written in the abstract of judgment. Values include Life Without Parole (LWOP), Life With Parole, Condemned, or a specific term in years and months. |
| `offense` | str | California penal, vehicular, or other code number for the offense the individual previously served time for and completed. |
| `offense description` | str | Text description of the offense. |
| `offense begin date` | datetime | Date the offense began. |
| `offense end date` | datetime | Date the offense ended, if applicable. |
| `in prison` | str | Indicates whether the offense was committed while incarcerated. |
| `offense category` | str | Broad category of the offense (e.g., drug crimes, property crimes, crimes against a person, case enhancement). |
| `offense time with enhancement` | str | Total sentence length in months, including any enhancements (e.g., additional years added for use of a firearm during a robbery). |
| `relationship` | str | Whether this sentence was served concurrently (overlapping with other sentences) or consecutively (no overlap). |
| `release date` | str | Date the individual was released upon completing this sentence. |
