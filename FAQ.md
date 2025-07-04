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
`Answer` CDCR stated that they cannot ensure that there are no errors or mistakes in the data reporting as well as their system of record. 

#### `Question` Can CDCR provide the full ERPD/MEPD dates (JAN 2024, FEB 2025, etc.)? 
`Answer` CDCR stated that they cannot provide the full EPRD/MEPD for individuals who are currently incarcerated. 

