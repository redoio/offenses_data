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

| Variable | Type | Description |
| --- | --- | --- |
| `cdcno` | str | Unique identifier (MD5 hash) for each individual under CDCR jurisdiction, including those housed in a state prison, temporarily released, or held in a non-CDCR facility. Excludes parolees. Individuals serving CDCR sentences in county jails are included. |
| `ethnicity` | str | Race or ethnicity of the incarcerated person (e.g., White, Black, Asian, Hispanic, Pacific Islander). |
| `controlling offense` | str | California penal, vehicular, or other code number for the offense governing the individual's current incarceration (e.g., PC187, PC664, PC214(a)). |
| `description` | str | Text description of the controlling offense. |
| `offense begin date` | datetime | Date the controlling offense began. |
| `offense end date` | datetime | Date the controlling offense ended, if applicable. |
| `controlling case number` | str | Case number associated with the controlling offense. |
| `controlling case sentencing county` | str | County where the individual was sentenced for the controlling offense. |
| `sentence type` | str | Indicates whether the sentence is a second strike, third strike, or other. |
| `aggregate sentence in months` | int | Total sentence length in months. Note: "Condemned" sentences are recorded as 100,000 or 1,000,000 months. |
| `offense category` | str | Broad category of the offense (e.g., drug-related, property-related, crimes against a person). |
| `eprd mepd month and year` | str | For determinate sentences: Earliest Possible Release Date (EPRD), calculated from the court-imposed sentence minus applicable credits. For indeterminate sentences: Minimum Eligible Parole Date (MEPD), the earliest date a "lifer" may be considered for parole. |
| `current location` | str | Name of the facility where the individual is currently housed. Note: CDCR sentences being served in county jails typically appear as "<County Name> Control Office". |

---

## Current Commitments

Files: `current_commitments.csv` `current_commitments.xlsx`

| Variable | Type | Description |
| --- | --- | --- |
| `cdcno` | str | Unique identifier (MD5 hash) for each individual under CDCR jurisdiction, including those housed in a state prison, temporarily released, or held in a non-CDCR facility. Excludes parolees. Individuals serving CDCR sentences in county jails are included. |
| `sentencing county` | str | County where the individual was sentenced for this offense. |
| `case number` | str | Case number associated with this offense. |
| `sentence from abstract of judgement` | str | Sentence as written in the abstract of judgment. Values include LWOP (Life Without Parole), LWP (Life With Parole), Condemned, or a specific term in years and months. |
| `offense` | str | California penal, vehicular, or other code number for the offense the individual is currently serving time for. |
| `offense description` | str | Text description of the offense. |
| `offense begin date` | datetime | Date the offense began. |
| `offense end date` | datetime | Date the offense ended, if applicable. |
| `in prison` | str | Indicates whether the offense was committed while incarcerated. |
| `offense category` | str | Broad category of the offense (e.g., drug-related, property-related, crimes against a person, case enhancement). |
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
| `sentence from abstract of judgement` | str | Sentence as written in the abstract of judgment. Values include LWOP (Life Without Parole), LWP (Life With Parole), Condemned, or a specific term in years and months. |
| `offense` | str | California penal, vehicular, or other code number for the offense the individual previously served time for and completed. |
| `offense description` | str | Text description of the offense. |
| `offense begin date` | datetime | Date the offense began. |
| `offense end date` | datetime | Date the offense ended, if applicable. |
| `in prison` | str | Indicates whether the offense was committed while incarcerated. |
| `offense category` | str | Broad category of the offense (e.g., drug-related, property-related, crimes against a person, case enhancement). |
| `offense time with enhancement` | str | Total sentence length in months, including any enhancements (e.g., additional years added for use of a firearm during a robbery). |
| `relationship` | str | Whether this sentence was served concurrently (overlapping with other sentences) or consecutively (no overlap). |
| `release date` | str | Date the individual was released upon completing this sentence. |

# Frequently Asked Questions 

### Table of Contents

1. [The structure of the CDCR ID is not recognizable to me. Why is that?](#question-the-structure-of-the-cdcr-id-is-not-recognizable-to-me-why-is-that)
2. [I found a compelling case but I cannot learn more about the individual using an anonymized CDCR ID. What should I do?](#question-i-found-a-compelling-case-but-i-cannot-learn-more-about-the-individual-using-an-anonymized-cdcr-id-what-should-i-do)
3. [I noticed that some sentences are missing case numbers. Why are they not available?](#question-i-noticed-that-some-sentences-are-missing-case-numbers-why-are-they-not-available)
4. [How do I cite the data and results?](#question-how-do-i-cite-the-data-and-results)
5. [How does this data differ from information acquired via a data sharing agreement?](#question-how-does-this-data-differ-from-information-acquired-via-a-data-sharing-agreement)
6. [Has CDCR specified why certain variables cannot be disclosed under the CPRA?](#question-has-cdcr-specified-why-certain-variables-cannot-be-disclosed-under-the-cpra)
7. [My county has an existing data sharing agreement with the state. Can Redo.io help me analyze the datasets CDCR sends us?](#question-my-county-has-an-existing-data-sharing-agreement-with-the-state-can-redoio-help-me-analyze-the-datasets-cdcr-sends-us)
8. [My county does not have an existing data sharing agreement with the state. But we have several data needs and questions. Can Redo.io support us in these efforts?](#question-my-county-does-not-have-an-existing-data-sharing-agreement-with-the-state-but-we-have-several-data-needs-and-questions-can-redoio-support-us-in-these-efforts)
9. [Are individuals serving prison sentences or CDCR commitments in county jails included in the dataset?](#question-are-individuals-serving-prison-sentences-or-cdcr-commitments-in-county-jails-included-in-the-dataset)
10. [Why it is not possible to share information on programming, milestones achieved and rehabilitation credits? This information does not compromise individual privacy, HIPAA protections, or put individuals at risk in any way or form.](#question-why-it-is-not-possible-to-share-information-on-programming-milestones-achieved-and-rehabilitation-credits-this-information-does-not-compromise-individual-privacy-hipaa-protections-or-put-individuals-at-risk-in-any-way-or-form)
11. [Can we be certain that there are no errors in the dataset?](#question-can-we-be-certain-that-there-are-no-errors-in-the-dataset)
12. [Can CDCR provide the full ERPD/MEPD dates (JAN 2024, FEB 2025, etc.)?](#question-can-cdcr-provide-the-full-erpdmepd-dates-jan-2024-feb-2025-etc)
13. [There are two kinds of enhancements reported in the datasets provided. Some enhancements are available as rows in the prior and current commitments files with `Case Enhancement` listed in the `Offense Category` column. Additionally, there are offense enhancements in the columns `Off Enh1`, `Off Enh2`, etc. What are the differences between these enhancement variables?](#question-there-are-two-kinds-of-enhancements-reported-in-the-datasets-provided-some-enhancements-are-available-as-rows-in-the-prior-and-current-commitments-files-with-case-enhancement-listed-in-the-offense-category-column-additionally-there-are-offense-enhancements-in-the-columns-off-enh1-off-enh2-etc-what-are-the-differences-between-these-enhancement-variables)
14. [The current and prior commitments datasets contain a variable called `Offense Time with Enhancement`. Does this include time for case, sentence or offense enhancements?](#question-the-current-and-prior-commitments-datasets-contain-a-variable-called-offense-time-with-enhancement-does-this-include-time-for-case-sentence-or-offense-enhancements)
15. [How is the `Offense Begin Date` and `Offense End Date` determined? Under what circumstances are these dates different?](#question-how-is-the-offense-begin-date-and-offense-end-date-determined-under-what-circumstances-are-these-dates-different)
16. [Is the expected release date the sum of the `Offense End Date` and the `Aggregate Sentence in Months` variables for determinately sentenced individuals?](#question-is-the-expected-release-date-the-sum-of-the-offense-end-date-and-the-aggregate-sentence-in-months-variables-for-determinately-sentenced-individuals)
17. [How is the `Aggregate Sentence in Months` variable calculated and reported?](#question-how-is-the-aggregate-sentence-in-months-variable-calculated-and-reported)
18. [Under what circumstances does the CDCR ID for an individual change?](#question-under-what-circumstances-does-the-cdcr-id-for-an-individual-change)

#### `Question` The structure of the CDCR ID is not recognizable to me. Why is that?
`Answer` We anonymize the original or raw CDCR IDs using an md5 hash algorithm. Though our prison sentences data is collected under the California Public Records Act (CPRA) and therefore can be released as is, we added an additional anonymization layer to protect incarcerated individuals' privacy. The original CDCR IDs are mapped to a new unique 10-character identifier that conceals the original value but remains consistent across all datasets: demographics, current commitments and prior commitments. Additionally, all individual names released by CDCR are hidden from public view. 

#### `Question` I found a compelling case but I cannot learn more about the individual using an anonymized CDCR ID. What should I do? 
`Answer` Please contact us through our Data Request form (https://tool.redoio.info/data_request) and we will be happy to provide you with the individual(s) original CDCR ID(s) and personal name(s) we have on file. 

#### `Question` I noticed that some sentences are missing case numbers. Why are they not available? 
`Answer` Unfortunately, CDCR does not disclose certain case numbers, CDCR IDs, individual names and other details under the California Public Records Act (CPRA) despite our best efforts to collect full and complete information about the incarcerated population.  We recognize that missing case numbers and CDCR IDs limits the use of our dataset. We are continuing to urge CDCR to provide more complete data to avoid these pitfalls. However, we hope that in instances wherein a case number for a controlling offense is missing, other information on their current and prior commitments may help identify the person in question. Please contact us with your inquiry and we will be happy to assist you further.

#### `Question` How do I cite the data and results? 
`Answer` Please reference our data, dashboards and analyses as follows: 

Redo.io [Computer software]. (2026). Retrieved from https://tool.redoio.info.

#### `Question` How does this data differ from information acquired via a data sharing agreement? 
`Answer` Our prison sentences data is a subset of the data that CDCR typically provides under a formal Data Sharing Agreement (DSA) between a county and the state. Formal DSAs for prison sentences data typically include sex registration status, mental health level of care, CSRA scores, COMPAS scores, rehabilitation milestones achieved, education credits, gender etc. Though we request CDCR to include all of the aforementioned variables, CDCR states that they cannot disclose this data due to privacy restrictions in the law. For example, CDCR stated that providing the gender and sex registration status of an individual would be a violation of the Prison Rape Elimination Act (PREA).

#### `Question` Has CDCR specified why certain variables cannot be disclosed under the CPRA? 
`Answer` CDCR refused to provide an explanation for lack of disclosure of each variable. They provided a generic explanation on the exclusionary criteria applied:

"The CA Department of Corrections and Rehabilitation has partially denied your request because some of the identified records are exempt from disclosure. As such, the data elements requested have not been included in these data. The applicable exemptions are fully discussed below:
Code of Federal Regulations title 45, sections 160.103, 164.502(a), 164.508(a)(1), Government Code section 7927.705 Penal Code sections 11075, 11076, and 13102; Government Code section 7927.705 California Code of Regulations title 15, section 3261.2(e); Government Code section 7927.705 Government Code section 7927.70 Government Code section 7927.705; The Prison Rape Elimination Act (PREA), Code of Federal Regulations, Title 28, Part 115.41(i) requires agencies to implement appropriate controls on the dissemination of information related to a person’s gender identity to ensure that sensitive information is not exploited to the individual’s detriment. Pursuant to Government Code sections 7927.705 and 7922.000, Penal Code 290.45, and WIC 827, these data exclude identifying information pertaining to offenders under the age of 18, where disclosure is prohibited by law, and those who CDCR has determined that the release of their information would create an unreasonable risk of danger to themselves."

#### `Question` My county has an existing data sharing agreement with the state. Can Redo.io help me analyze the datasets CDCR sends us? 
`Answer` Absolutely. We are happy to build custom solutions for your needs and use cases. Our public facing tool is meant to be a general purpose resource for an initial exploratory analysis. Please contact us with your request and we will be happy to support you.

#### `Question` My county does not have an existing data sharing agreement with the state. But we have several data needs and questions. Can Redo.io support us in these efforts?
`Answer` Absolutely. If our existing tools and datasets are insufficient for your needs, we are happy to work with you to develop solutions that best fit your objectives. Please contact us with your request and we will be happy to support you.
                                                            
#### `Question` My county does not have an existing data sharing agreement with the state. But we have several data needs and questions. Can Redo.io support us in these efforts?
`Answer` Absolutely. If our existing tools and datasets are insufficient for your needs, we are happy to work with you to develop solutions that best fit your objectives. Please contact us with your request and we will be happy to support you.

#### `Question` Are individuals serving prison sentences or CDCR commitments in county jails included in the dataset?
`Answer` Yes, this data set includes individuals serving prison sentences in county jail. The cohort for the current commits, prior commits and demographics include individuals housed in an institution, on temporary release, or in a non-CDCR institution (excluding parolees).

#### `Question` Why it is not possible to share information on programming, milestones achieved and rehabilitation credits? This information does not compromise individual privacy, HIPAA protections, or put individuals at risk in any way or form.
`Answer` CDCR states that they are unable to provide responsive records pertaining to specific milestone and rehabilitation credits per Penal Code sections 11075, 11076, and 13102; Government Code section 7927.705, as these data are considered Criminal Offender Record Information (CORI).

#### `Question` Can we be certain that there are no errors in the dataset? 
`Answer` CDCR states that they cannot ensure that there are no errors or mistakes in the data reporting as well as their system of record. 

#### `Question` Can CDCR provide the full ERPD/MEPD dates (JAN 2024, FEB 2025, etc.)? 
`Answer` CDCR states that they cannot provide the full EPRD/MEPD for individuals who are currently incarcerated. 

#### `Question` There are two kinds of enhancements reported in the datasets provided. Some enhancements are available as rows in the prior and current commitments files with `Case Enhancement` listed in the `Offense Category` column. Additionally, there are offense enhancements in the columns `Off Enh1`, `Off Enh2`, etc. What are the differences between these enhancement variables? 

`Answer` CDCR states that enhancements reflect additional penalties applied to a sentence. Offense enhancements are directly related to the charge in which the individual was convicted. Case enhancements are related to prior felony convictions or additional case factors not specifically related to the convicted offense.
 
#### `Question` The current and prior commitments datasets contain a variable called `Offense Time with Enhancement`. Does this include time for case, sentence or offense enhancements?

`Answer` CDCR states that the `Offense Time with Enhancement` is the aggregate time imposed by the court for an offense plus time imposed for any associated offense enhancements.

#### `Question` How is the `Offense Begin Date` and `Offense End Date` determined? Under what circumstances are these dates different?

`Answer` CDCR states that the offense begin and end dates reflect two possible scenarios: 1) when the crime occurred over a period of time, or 2) when the record represents multiple counts, the begin date is the earliest offense date and the end date is the last date. In the case of the second scenario, if a record represents more than two counts, not all offense dates are available in CDCR's system of record. 
 
#### `Question`  Is the expected release date the sum of the `Offense End Date` and the `Aggregate Sentence in Months` variables for determinately sentenced individuals?

`Answer` CDCR states that this is not the case. The release date is calculated based on when the individual’s sentence began and the total sentence imposed, excluding any credits earned for program participation and good behavior while serving their sentence, minus credits lost for rules violations.

#### `Question` How is the `Aggregate Sentence in Months` variable calculated and reported?

`Answer` CDCR states that the `Aggregate Sentence in Months` variable reflects the total sentence imposed, which include all offenses and any offense enhancements and/or case enhancements across all cases for the prison term, and does not include commitments from prior prison terms. 
 
#### `Question` Under what circumstances does the CDCR ID for an individual change?

`Answer` An individual can have multiple CDCR numbers. A CDCR number would be reused if an individual was released to parole and returned to custody while on parole. A new CDCR number is issued when an individual returns to CDCR after having been discharged from under CDCR’s jurisdiction, or a person identifies as a different gender than previously and is housed at an institution appropriate for the new identity. Therefore, we cannot be certain that an individual regardless of the number of releases, paroles, commitments, etc. is always given the same CDCR ID.
