# Introduction
Data on the population currently incarcerated in the California Department of Corrections and Rehabilitation (CDCR) as of December 2023 acquired via the California Public Records Act (CPRA). CDCR applied several privacy (health information, age, etc.) related exclusionary criteria to release the data. Some CDCR identification numbers are hashed for de-identification as a result. 

Note: Data and analyses in this repository are fully independent of the Three Strikes Project, Stanford University and the Resentencing Data Initiative. This is an exploratory effort not supported or related to any of the aforementioned parties.

# Demo
We demonstrate a full execution of the resentencing eligibility model (https://github.com/redoio/resentencing_data_initiative/) on the CDCR population data. We establish a set of eligibility rules, classify offenses based on their nature and severity, and then create a scenario in which we identify the best candidates for resentencing.

## Output
As of 4/29/2024, a sample run on 50,000 randomly selected individuals out of 95,476 total individuals in CDCR custody (as reported by the department), returned 360 eligible candidates.<br>
<br>
Note: This cohort simply meets the sample eligibility crtiera. There is no certainty that these individuals are falsely incarcerated or harshly sentenced. Such determinations require complex case reviews by attorneys. 

The selection process does not account for age-related criteria since the department denied sharing individual birthdays. Age is a pertinent factor, however, in PIR eligibility in some counties. The Los Angeles County District Attorney's Office, for example, reviews adult cases if the individual is over the age of 50 differently from juvenile cases if the offense was committed at age 14 or 15 (https://github.com/redoio/resentencing_data_initiative/eligibility_model/code/offense_classification/county/los_angeles)

# Citation 

If you make use of our dataset(s), please cite our work as follows: 

"Redo.io. cdcr-prison-pop (Version 1.0.0) [Dataset]. https://github.com/redoio/prison_pop"

# License 

[![License: ODbL](https://img.shields.io/badge/License-ODbL-brightgreen.svg)](https://opendatacommons.org/licenses/odbl/)

This cdcr-prison-pop repository is made available under the Open Database License: http://opendatacommons.org/licenses/odbl/1.0/ by Redo.io. Any rights in individual contents of the database are licensed under the Database Contents License: http://opendatacommons.org/licenses/dbcl/1.0/

# Contact 
Contact aparna.komarla@gmail.com for any questions
