# Introduction
Data on the population currently incarcerated in any of the thirty-five state prisons under the jurisdiction of the California Department of Corrections and Rehabilitation (CDCR) as of December 2023. Information was acquired via the California Public Records Act (CPRA). The Department applied several privacy (health information, age, etc.) related exclusionary criteria to release these records to Redo.io. The CDCR identification numbers are hashed to add another layer of privacy and security. 

Note: Data and analyses in this repository are fully independent of the Three Strikes Project, Stanford University and the Resentencing Data Initiative. This is an open data related effort not supported or related to any of the aforementioned parties.

# Citation 

If you make use of our dataset(s), please cite our work as follows: 

"Redo.io. cdcr-offenses-data (Version 1.0.0) [Dataset]. https://github.com/redoio/offenses data"

# License 

[![License: ODbL](https://img.shields.io/badge/License-ODbL-brightgreen.svg)](https://opendatacommons.org/licenses/odbl/)

This cdcr-offenses-data repository is made available under the Open Database License: http://opendatacommons.org/licenses/odbl/1.0/ by Redo.io. Any rights in individual contents of the database are licensed under the Database Contents License: http://opendatacommons.org/licenses/dbcl/1.0/

# Access 

Our datasets are publicly available and downloadable. For data previews and exploration, you can access the same demographics.csv, current commitments.csv and prior commitments.csv data on data.world (log in required).

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
`controlling offense`	| str | Offense number from the California criminal code (penal code, vehicular code, other) that the incarcerated person is currently serving time for, i.e. main offense that the person is sentenced for hence it "controls" their incarceration (PC187, PC664, PC214(a), etc.) |
`description`	| str | Text description or details about the controlling offense |
`offense begin date`	| datetime | Date on which the offense was committed |
`offense end date`	| datetime | Date on which the offense was committed |
`controlling case number`	| str | Case number of the individual's controlling offense |
`controlling case sentencing county`	| str | County or geographical location where the incarcerated individual was sentenced for their offense. County where the case was deliberated with a judge, defense and prosecutor and the sentence term and length was decided. County that has the authority to decide whether to resentence the individual or provide any other form of relief. 
`sentence type` |	str | Specifies whether the offense is a second strike or third strike or something else. Indicates the number of serious felonies that the individual committed and has served time for. Third strike felony carries a minimum sentence of 25 years to life. |
`aggregate sentence in months`	| int | Total length of the sentence in months. Numerical count that can be converted to years, decades, etc.<br>Note: Sentences of the type "Condemned" carry a sentence length of 100,000 months or 1,000,000 months. |
`offense category`	| str | Specifies the nature of the offense (drug related, property related, crimes against a person) |
`erpd mepd month and year`	| str | Earliest Possible Release Date (EPRD): date determinately-sentenced offenders will be released based on the sentence imposed by the court, less any applicable credits; Minimum Eligible Parole Date (MEPD): date indeterminately-sentenced offenders (i.e., persons sentenced to life with the possibility of parole, or “lifers”) are eligible for parole consideration by the Parole Board based on the sentence imposed by the court, less any applicable credits |
`current location`	| str | Name of the prison facility where the person is incarcerated (one of CDCR's state prisons - San Quentin, CA Institution for Men, CA Central Women's Facility, etc.) |

## Current Commitments 

Files: `current_commitments.csv` `current_commitments.xlsx` 

| variable | type | description |
| ------------ | ------------------- | --------- |
`cdcno`	| str | Unique md5 hash identifier for each individual in the CDCR (California Department of Corrections and Rehabilitation) prison system. Individual is incarcerated or imprisoned in any one of the state's prisons as of December 2023. |
`sentencing county`	| str | County or geographical location where the incarcerated individual was sentenced for their offense. County where the case was deliberated with a judge, defense and prosecutor and the sentence term and length was decided. | 
`case number`	| str | Case number of the individual's offense |
`sentence from abstract of judgement` | str | Length of the sentence in text form: life without parole, life with parole, 4 years, etc. |
`offense` | str | Offense number from the California criminal code (penal code, vehicular code, other) that the incarcerated person is currently serving time for. |
`offense description`	| str | Text description or details about the offense. |
`offense begin date`	| datetime | Date on which the offense was committed |
`offense end date`	| datetime | Date on which the offense was committed |
`in prison`	| str | Specifies whether the offense was committed in prison or not. This could be a fight with another incarcerated person, defying the order or command of an officer, not following the rules of the facility or prison in any way |
`offense category`	| str | Specifies the nature of the offense (drug related, property related, crimes against a person, case enhancement) |
`offense time with enhancement` | str | Total months of the sentence taking into account additional months added due to enhancements. For example, a robbery offense may result in a sentence length of 10 years. A robbery with a firearm (enhancement) could result in a sentence of 10 years plus a few additional years. |
`relationship` | str | Specifies whether the sentence was served concurrently, i.e. in parallel to other sentences or if the sentence is being served individually, i.e. no overlap with other sentences |

## Prior Commitments 

Files: `prior_commitments.csv` `prior_commitments.xlsx` 

| variable | type | description |
| ------------ | ------------------- | --------- |
`cdcno`	| str | Unique md5 hash identifier for each individual in the CDCR (California Department of Corrections and Rehabilitation) prison system. Individual is incarcerated or imprisoned in any one of the state's prisons as of December 2023. |
`sentencing county`	| str | County or geographical location where the incarcerated individual was sentenced for their offense. County where the case was deliberated with a judge, defense and prosecutor and the sentence term and length was decided. | 
`case number`	| str | Case number of the individual's offense |
`sentence from abstract of judgement` | str | Length of the sentence in text form: life without parole, life with parole, 4 years, etc. |
`offense` | str | Offense number from the California criminal code (penal code, vehicular code, other) that the incarcerated person served time for and completed their sentence. |
`offense description`	| str | Text description or details about the offense |
`offense begin date`	| datetime | Date on which the offense was committed |
`offense end date`	| datetime | Date on which the offense was committed |
`in prison`	| str | Specifies whether the offense was committed in prison or not. This could be a fight with another incarcerated person, defying the order or command of an officer, not following the rules of the facility or prison in any way |
`offense category`	| str | Specifies the nature of the offense (drug related, property related, crimes against a person, case enhancement) |
`offense time with enhancement` | str | Total months of the sentence taking into account additional months added due to enhancements. For example, a robbery offense may result in a sentence length of 10 years. A robbery with a firearm (enhancement) could result in a sentence of 10 years plus a few additional years. |
`relationship` | str | Specifies whether the sentence was served concurrently, i.e. in parallel to other sentences or if the sentence is being served individually, i.e. no overlap with other sentences |
`release date`	| str | Date on which the individual was released from prison after they finished serving the sentence. Since this is a prior offense, it is no longer on the individual's list of current offenses, which means they have served the full sentence stipulated by the court |

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
13. [There are two kinds of enhancements reported in the datasets provided. Some enhancements are available as rows in the prior and current commitments files with `Case Enhancement` listed in the `Offense Category` column. Additionally, there are offense enhancements in the columns `Off Enh1`, `Off Enh2`, etc. What are the differences between these enhancement variables? ](#question-there-are-two-kinds-of-enhancements-reported-in-the-datasets-provided-some-enhancements-are-available-as-rows-in-the-prior-and-current-commitments-files-with-case-enhancement-listed-in-the-offense-category-column-additionally-there-are-offense-enhancements-in-the-columns-off enh1-off-enh2-etc-what-are-the-differences-between-these-enhancement-variables)
14. [The current and prior commitments datasets contain a variable called `Offense Time with Enhancement`. Does this include time for case, sentence or offense enhancements?](#question-the-current-and-prior-commitments-datasets-contain-a-variable-called-offense-time-with-enhancement-does-this-include-time-for-case-sentence-or-offense-enhancements)
15. [How is the `Offense Begin Date` and `Offense End Date` determined? Under what circumstances are these dates different? ](#question-how-is-the-offense-begin-date-and-offense-end-date-determined-under-what-circumstances-are-these-dates-different)
16. [Is the expected release date the sum of the `Offense End Date` and the `Aggregate Sentence in Months` variables for determinately sentenced individuals? ](#question-is-the-expected-release-date-the-sum-of-the-offense-end-date-and-the-aggregate-sentence-in-months-variables-for-determinately-sentenced-individuals)
17. [How is the `Aggregate Sentence in Months` variable calculated and reported? ](#question-how-is-the-aggregate-sentence-in-months-variable-calculated-and-reported)
18. [Under what circumstances does the CDCR ID for an individual change?](#question-under-what-circumstances-does-the-cdcr-id-for-an-individual-change)

#### `Question` The structure of the CDCR ID is not recognizable to me. Why is that?
`Answer` We anonymize the original or raw CDCR IDs using an md5 hash algorithm. In simple terms, though our prison sentences data is collected under the California Public Records Act (CPRA), we added an additional anonymization layer to protect incarcerated individuals' privacy. All individual names are hidden from public view. Additionally, their CDCR IDs are hashed, i.e. mapped to a new unique 10-character identifier that conceals the original value but remains consistent across all datasets: demographics, current commitments and prior commitments.

#### `Question` I found a compelling case but I cannot learn more about the individual using an anonymized CDCR ID. What should I do? 
`Answer` Please contact us with your request and we will be happy to provide you with the individual(s) original CDCR ID(s) and personal name(s) we have on file.

#### `Question` I noticed that some sentences are missing case numbers. Why are they not available? 
`Answer` Unfortunately, CDCR will not disclose certain information under the California Public Records Act (CPRA) despite our best efforts to collect full and complete information about prison sentences. 
We recognize that missing case numbers and CDCR IDs limits the use of our dataset. We are continuing to urge CDCR to provide more complete data to avoid these pitfalls. 
However, we hope that in instances wherein a case number for a controlling offense is missing, other information on their current and prior commitments may help identify the person in question. 
Please contact us with your inquiry and we will be happy to assist you further.

#### `Question` How do I cite the data and results? 
`Answer` Please reference our data, dashboards and analyses as follows: 

Redo.io [Computer software]. (2025). Retrieved from tool.redoio.info

#### `Question` How does this data differ from information acquired via a data sharing agreement? 
:green-badge[Answer] Our prison sentences data is a subset of the data that CDCR typically provides under a formal data sharing agreement between a county and the state. 
Formal data sharing agreements for prison sentences data typically include sex registration status, mental health level of care, CSRA scores, COMPAS scores, milestones achieved, education credits, gender etc. 
Though our CPRA requests to CDCR include all of the aforementioned variables (and more), CDCR states that they cannot disclose certain variables due to privacy restrictions in the law. 
For example, they stated that providing the gender and sex registration status of an individual would be a violation of the Prison Rape Elimination Act (PREA)

#### `Question` Has CDCR specified why certain variables cannot be disclosed under the CPRA? 
`Answer` CDCR refused to provide an explanation for omissions per variable. They provided a general explanation of the exclusionary criteria they applied:

"The CA Department of Corrections and Rehabilitation has partially denied your request because some of the identified records are exempt from disclosure. As such, the data elements requested have not been included in these data. The applicable exemptions are fully discussed below:
Code of Federal Regulations title 45, sections 160.103, 164.502(a), 164.508(a)(1), Government Code section 7927.705 Penal Code sections 11075, 11076, and 13102; Government Code section 7927.705 California Code of Regulations title 15, section 3261.2(e); Government Code section 7927.705 Government Code section 7927.70 Government Code section 7927.705; The Prison Rape Elimination Act (PREA), Code of Federal Regulations, Title 28, Part 115.41(i) requires agencies to implement appropriate controls on the dissemination of information related to a person’s gender identity to ensure that sensitive information is not exploited to the individual’s detriment. Pursuant to Government Code sections 7927.705 and 7922.000, Penal Code 290.45, and WIC 827, these data exclude identifying information pertaining to offenders under the age of 18, where disclosure is prohibited by law, and those who CDCR has determined that the release of their information would create an unreasonable risk of danger to themselves."

#### `Question` My county has an existing data sharing agreement with the state. Can Redo.io help me analyze the datasets CDCR sends us? 
`Answer` Absolutely. We are happy to build custom solutions for your needs and use cases. Our public facing tool is meant to be a general purpose resource for an initial exploratory analysis. Please contact us with your request and we will be happy to support you.

#### `Question` My county does not have an existing data sharing agreement with the state. But we have several data needs and questions. Can Redo.io support us in these efforts?
`Answer` Absolutely. If our existing tools and datasets are insufficient for your needs, we are happy to work with you to develop solutions that best fit your objectives. Please contact us with your request and we will be happy to support you.
                                                            
#### `Question` The structure of the CDCR ID is not recognizable to me. Why is that?
`Answer` The CDCR IDs are hashed using an md5 hash algorithm. In simple terms, though the prison sentences data is collected through the California Public Records Act (CPRA), we added an additional anonymization layer to protect incarcerated individuals' privacy. All individual names are hidden from public view. Additionally, their CDCR IDs are hashed, i.e. mapped to a new unique 10-character identifier that conceals the original value but remains consistent across all datasets: demographics, current commitments and prior commitments.

#### `Question` I found a compelling case but I cannot learn more about the individual using an anonymized CDCR ID. What should I do? 
`Answer` Please contact us with your request and we will be happy to provide you the individual's or cohort's original CDCR ID(s) and personal name(s) we have on file.

#### `Question` I noticed that some sentences are missing case numbers. Why are they not available? 
`Answer` Unfortunately, CDCR reduces to disclose some case details under the California Public Records Act (CPRA) despite our best efforts to collect full and complete information about prison sentences. 
We recognize that missing case numbers and CDCR IDs limits the power of our dataset. We are continuing to urge CDCR to provide more complete information to make our datasets more actionable for attorneys and researchers. Please contact us with your inquiry and we will be happy to assist you further.

#### `Question` How do I cite the data and results? 
`Answer` Please reference our data, dashboards and analyses as follows: 

Redo.io [Computer software]. (2025). Retrieved from tool.redoio.info

#### `Question` How does this data differ from information acquired via a data sharing agreement? 
`Answer` Our prison sentences data is a subset of the data that CDCR typically provides under a formal data sharing agreement between a county and the state. 
Formal data sharing agreements for prison sentences data typically include sex registration status, mental health level of care, CSRA scores, COMPAS scores, milestones achieved, education credits, gender etc. 
Though our CPRA requests to CDCR include all of the aforementioned variables (and more), CDCR states that they cannot disclose them under the CPRA due to privacy restrictions in the law. For example, they stated that providing the gender and sex registration status of an individual would be a violation of the Prison Rape Elimination Act (PREA)

#### `Question` My county has an existing data sharing agreement with the state. Can Redo.io help me analyze the datasets CDCR sends us? 
`Answer` Absolutely. We are happy to build custom solutions for your needs and use cases. Our public facing tool is meant to be a general purpose resource for an initial exploratory analysis. Please contact us with your request and we will be happy to support you.

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
