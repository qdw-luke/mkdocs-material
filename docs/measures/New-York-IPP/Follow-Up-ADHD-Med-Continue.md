Status: Client-Ready
Author: Kelly O'Brien
CreateDate: 2016-02-04
ModifyDate: 2016-02-04
AAVersion: 4.9

#Follow Up Care for Children Prescribed ADHD Medications: C&M Phase (Prescribed)

| Attribute | Description |
| --------- | ----------- |
| **Official Name** | Follow Up Care for Children Prescribed ADHD Medications: C&M Phase (Prescribed) |
| **Long Display Name** | Follow Up Care for Children Prescribed ADHD Medication Cont |
| **Short Display Name** | Follow Up ADHD Med Continue |
| **Description** | Percentage of children 6-12 years of age newly started on an ADHD medication prescription that lasted at least 210 out of 300 days after prescription start date, who had one follow-up visit during the 30-day Initiation Phase and two follow-up visits in the 270 day period after the initiation phase. |
| **Purpose** | When managed appropriately, medication for ADHD can control symptoms of hyperactivity, impulsiveness and inability to sustain concentration. To ensure that medication is prescribed and managed correctly, it is important that children be monitored by a health care professional with prescribing authority. |
| **Denominator** | Patient had one or more medical visits in the three years prior to the MP end date.<br>AND<br>Patient is prescribed an ADHD Medication between 22 months before MP end date and 10 months before MP end date.<br>AND<br>Patient has not been on an ADHD medication in at least 120 days prior to the Index Prescription Start Date (IPSD).<br>AND<br>Patient has prescription for ADHD medication for at least 210 out of the 300 days following the IPSD. |
| **Denominator Exclusions** | Patient diagnosed during an acute inpatient encounter with a mental health or substance abuse issue within 300 days of prescription start date.<br>OR<br>Patient diagnosed with Narcolepsy at any time during the patient's history through MP end date. |
| **Denominator Exceptions** | N/A |
| **Numerator** | Patient has at least one face to face visit with a prescribing practitioner within 30 days of prescription start date.<br>AND<br>At least two visits with a prescribing practitioner in the 270 day period after the initiation phase (one of the two visits may be a telephone visit). |
| **Numerator Exclusions** | N/A |
| **Grain** | Person |
| **Unit** | Percent |
| **Calculation** | (count of patients from the denominator who meet the numerator criteria) / (count of patients who meet the denominator criteria)<br><br>Remove patients from the denominator and numerator if they meet the *denominator exclusion* criteria. |
| **Notes** | N/A |


##Technical Criteria

| Component | Logic | Ref # | Criteria |
| --------- | ----- | ----- | -------- |
| **Denominator** | | | D1 AND D2 AND D3 AND D4 AND D5 |
| |  | D1 | Patient had one or more medical visits in the three years prior to the MP end date as indicated by CPT codes in HEDIS (Outpatient CPT Value Set) |
| | AND | D2 | Patient is 6 years of age as of 10 months prior to MP start date through 12 years of age as of 10 months prior to MP end date |
| | AND | D3 | Patient is prescribed an ADHD Medication as defined by the NDC codes in HEDIS Drug table ADD-A between 22 months before period end and 10 months before period end |
| | AND | D4 | Patient has prescritption for ADHD Medication for 210 or more of the 300 days following the initial prescription |
| | AND | D5 | Patient has NOT had an ADHD Medication in active medication list for at least 120 days prior to prescription start date |
| | Value Sets | | D1: HEDIS Outpatient CPT<br>D3: HEDIS Drug table ADD-A |
| **Denominator Exclusions** | | | EX1 OR EX2 |
| |  | EX1 | Patient had an acute/inpatient encounter with a diagnosis of mental health or substance abuse as indicated by HEDIS (Mental Health Diagnosis Value Set, Chemical Dependency Value Set) during the 300 day period following the prescription start |
| | OR | EX2 | Patient was diagnosed with narcolepsy at any time before the measurement period end date |
| | Value Sets | | EX1: HEDIS Mental Health Diagnosis, HEDIS Chemical Dependency |
| **Denominator Exceptions** | | | None |
| **Numerator** | | | N1 AND N2 |
| |  | N1 | Patient has documentation of at least one face to face encounter with a practitioner with prescribing authority within 30 days of prescription start date as documented with one of the following code combinations:<br>-HEDIS ADD Stand Alone Visits Value Set<br>-HEDIS ADD Visits Group 1 Value Set with ADD POS Group 1 Value Set<br>-HEDIS ADD Visits Group 2 Value Set with ADD POS Group 2 Value Set |
| | AND | N2 | Patient has documentation of at least two encounters with a practitioner in the 270 days after the Initiation Phase, one of which can be a telephone encounter, as specified in the HEDIS Telephone Visits Value Set |
| | Value Sets | | N1: HEDIS ADD Stand Alone Visits, HEDIS ADD Visits Group 1 with ADD POS Group 1, HEDIS ADD Visits Group 2 with ADD POS Group 2<br>N2: HEDIS Telephone Visits |
| **Numerator Exclusions** | | | None |
