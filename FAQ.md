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
19. [How are non-violent, non-sexual, and non-serious offenders identified?](#question-how-are-non-violent-non-sexual-and-non-serious-offenders-identified)
20. [What are the demographics, current commitments, and prior commitments datasets?](#question-what-are-the-demographics-current-commitments-and-prior-commitments-datasets)
21. [What is CDCR?](#question-what-is-cdcr)
22. [What do "as of 2023" and "as of 2025" mean?](#question-what-do-as-of-2023-and-as-of-2025-mean)
23. [Where can the raw datasets be downloaded?](#question-where-can-the-raw-datasets-be-downloaded)
24. [Are the ethnicity values aligned with CENSUS labels?](#question-are-the-ethnicity-values-aligned-with-census-labels)
25. [Does Redo.io use AI, and if so, is it safe and how can I learn more?](#question-does-redoio-use-ai-and-if-so-is-it-safe-and-how-can-i-learn-more)
26. [Do you track user data, and how does the platform protect my privacy?](#question-do-you-track-user-data-and-how-does-the-platform-protect-my-privacy)

#### `Question` The structure of the CDCR ID is not recognizable to me. Why is that?
`Answer` We anonymize the original or raw CDCR IDs using an md5 hash algorithm. In simple terms, though our prison sentences data is collected under the California Public Records Act (CPRA), we added an additional anonymization layer to protect incarcerated individuals' privacy. All individual names are hidden from public view. Additionally, their CDCR IDs are hashed, i.e. mapped to a new unique 10-character identifier that conceals the original value but remains consistent across all datasets: demographics, current commitments and prior commitments.

#### `Question` I found a compelling case but I cannot learn more about the individual using an anonymized CDCR ID. What should I do?
`Answer` Please contact us with your request and we will be happy to provide you the individual's or cohort's original CDCR ID(s) and personal name(s) we have on file.

#### `Question` I noticed that some sentences are missing case numbers. Why are they not available?
`Answer` Unfortunately, CDCR will not disclose certain information under the California Public Records Act (CPRA) despite our best efforts to collect full and complete information about prison sentences. We recognize that missing case numbers and CDCR IDs limits the use of our dataset. We are continuing to urge CDCR to provide more complete data to avoid these pitfalls. However, we hope that in instances wherein a case number for a controlling offense is missing, other available information on their current and prior commitments may help identify the person in question. Please contact us with your inquiry and we will be happy to assist you further.

#### `Question` How do I cite the data and results?
`Answer` Please reference our data, dashboards and analyses as follows:

Redo.io [Computer software]. (2026). Retrieved from https://tool.redoio.info

#### `Question` How does this data differ from information acquired via a data sharing agreement?
`Answer` Our prison sentences data is a subset of the data that CDCR typically provides under a formal data sharing agreement between a county and the state.
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

#### `Question` Are individuals serving prison sentences or CDCR commitments in county jails included in the dataset?
`Answer` Yes, this data set includes individuals serving prison sentences in county jail. The cohort for the current commits, prior commits and demographics include individuals housed in an institution, on temporary release, or in a non-CDCR institution (excluding parolees).

#### `Question` Why it is not possible to share information on programming, milestones achieved and rehabilitation credits? This information does not compromise individual privacy, HIPAA protections, or put individuals at risk in any way or form.
`Answer` CDCR states that they are unable to provide responsive records pertaining to specific milestone and rehabilitation credits per Penal Code sections 11075, 11076, and 13102; Government Code section 7927.705, as these data are considered Criminal Offender Record Information (CORI).

#### `Question` Can we be certain that there are no errors in the dataset?
`Answer` CDCR states that they cannot ensure that there are no errors or mistakes in the data reporting as well as their system of record.

#### `Question` Can CDCR provide the full ERPD/MEPD dates (JAN 2024, FEB 2025, etc.)?
`Answer` CDCR states that they can only provide the month and year values of the ERPD/MEPD as opposed to the full date values for individuals who are currently incarcerated.

#### `Question` There are two kinds of enhancements reported in the datasets provided. Some enhancements are available as rows in the prior and current commitments files with `Case Enhancement` listed in the `Offense Category` column. Additionally, there are offense enhancements in the columns `Off Enh1`, `Off Enh2`, etc. What are the differences between these enhancement variables?
`Answer` CDCR states that enhancements reflect additional penalties applied to a sentence. Offense enhancements are directly related to the charge in which the individual was convicted. Case enhancements are related to prior felony convictions or additional case factors not specifically related to the convicted offense.

#### `Question` The current and prior commitments datasets contain a variable called `Offense Time with Enhancement`. Does this include time for case, sentence or offense enhancements?
`Answer` CDCR states that the `Offense Time with Enhancement` is the aggregate time imposed by the court for an offense plus time imposed for any associated offense enhancements.

#### `Question` How is the `Offense Begin Date` and `Offense End Date` determined? Under what circumstances are these dates different?
`Answer` CDCR states that the offense begin and end dates reflect two possible scenarios: 1) when the crime occurred over a period of time, or 2) when the record represents multiple counts, the begin date is the earliest offense date and the end date is the last date. In the case of the second scenario, if a record represents more than two counts, not all offense dates are available in CDCR's system of record.

#### `Question` Is the expected release date the sum of the `Offense End Date` and the `Aggregate Sentence in Months` variables for determinately sentenced individuals?
`Answer` CDCR states that this is not the case. The release date is calculated based on when the individual’s sentence began and the total sentence imposed, excluding any credits earned for program participation and good behavior while serving their sentence, minus credits lost for rules violations.

#### `Question` How is the `Aggregate Sentence in Months` variable calculated and reported?
`Answer` CDCR states that the `Aggregate Sentence in Months` variable reflects the total sentence imposed, which include all offenses and any offense enhancements and/or case enhancements across all cases for the prison term, and does not include commitments from prior prison terms.

#### `Question` Under what circumstances does the CDCR ID for an individual change?
`Answer` An individual can have multiple CDCR numbers. A CDCR number would be reused if an individual was released to parole and returned to custody while on parole. A new CDCR number is issued when an individual returns to CDCR after having been discharged from under CDCR’s jurisdiction, or a person identifies as a different gender than previously and is housed at an institution appropriate for the new identity. Therefore, we cannot be certain that an individual regardless of the number of releases, paroles, commitments, etc. is always given the same CDCR ID.

#### `Question` How are non-violent, non-sexual and non-serious offenders identified?
`Answer` "Non-non-non" refers to individuals whose cases are non-violent, non-sexual, and non-serious. Redo.io developed criteria for this classification, including offense groups and categorizations for super-strike felonies, registerable sex offenses, violent felonies, and homicide offenses, in collaboration with attorneys from the Three Strikes Project at Stanford Law. A full list of categorized penal codes is available here: https://github.com/redoio/scenarios/blob/main/offense_categories/selection_criteria.xlsx.
Definitions of "non-non-non" offenders differ across our platform and can be customized using the Scenario Builder tool. For example, "non-non-non" offenders may be defined as those with cases meeting all of the following criteria:
(a). No current commitments in serious felonies, violent felonies, registerable sex offenses, or super-strike offenses
(b). No prior commitments in registerable sex offenses or super-strike offenses
(c). Sentenced to at least 20 years
(d). Served at least 10 years

#### `Question` What are the demographics, current commitments, and prior commitments datasets?
`Answer` These datasets come from California Public Records Act (CPRA) requests to the California Department of Corrections and Rehabilitation (CDCR). Our prison sentences data is split across three datasets, each capturing a different part of a person's record with CDCR. The demographics dataset contains individual-level characteristics, such as ethnicity, case number, parole dates, and the primary controlling offense. There is exactly one demographics record per person who is currently incarcerated. The current commitments dataset contains all of the commitments a person currently has with CDCR, including the controlling offense, and a person can have multiple current commitment records. The prior commitments dataset contains all of the commitments or sentences a person has already completed, and a person can have multiple prior commitment records; if a person has no prior criminal history, their prior commitments may be empty. In summary, every currently incarcerated person has exactly one record in demographics and one or more records in current commitments, while prior commitments can hold multiple records or none at all, depending on a person's history.

#### `Question` What is CDCR?
`Answer` CDCR stands for the California Department of Corrections and Rehabilitation, the state agency responsible for operating California's prisons and supervising incarcerated and paroled individuals. Our prison sentences data is collected from CDCR under the California Public Records Act (CPRA).

#### `Question` What do "as of 2023" and "as of 2025" mean?
`Answer` These labels indicate the snapshot date of each dataset. The year values refer to everyone incarcerated in CDCR custody as of that date, including individuals serving CDCR commitments in county jails. All three datasets, demographics, current commitments, and prior commitments, are available for each date. The 2023 datasets are current as of December 2023, and the 2025 datasets are current as of April 2025.

#### `Question` Where can the raw datasets be downloaded?
`Answer` The raw datasets are available on the Harvard Dataverse: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi%3A10.7910%2FDVN%2FQCTMSI

#### `Question` Are the ethnicity values aligned with CENSUS labels?
`Answer` No. The ethnicity values in our data are reported by CDCR and do not directly match racial groups used in the U.S. Census. They can, however, be mapped to Census categories (White, Black or African American, American Indian or Alaska Native, Asian, Native Hawaiian or Other Pacific Islander, and Hispanic or Latino).

#### `Question` Does Redo.io use AI, and if so, is it safe and how can I learn more?
`Answer` Yes, Redo.io uses AI as part of its analytics and tooling. We are committed to using it responsibly and transparently. To learn more about where and how we apply AI, along with the safeguards we have in place, please see the "How We Use AI" page on our platform: https://tool.redoio.info/how_we_use_ai.

#### `Question` Do you track user data, and how does the platform protect my privacy?
`Answer` We take user privacy seriously and limit the data we collect. For a full explanation of what we do and do not track, and the measures we use to protect your privacy, please see the "How We Use Your Data" page on our platform: https://tool.redoio.info/how_we_use_your_data.

