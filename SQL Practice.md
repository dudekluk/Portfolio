# SQL Query Examples

## Table of Contents

* [Easy Questions](#easy-questions)
    * [1. Show first name, last name, and gender of patients whose gender is 'M'](#easy-question-1)
    * [2. Show first name and last name of patients who does not have allergies. (null)](#easy-question-2)
    * [3. Show first name of patients that start with the letter 'C'](#easy-question-3)
    * [4. Show first name and last name of patients that weight within the range of 100 to 120 (inclusive)](#easy-question-4)
    * [5. Update the patients table for the allergies column. If the patient's allergies is null then replace it with 'NKA'](#easy-question-5)
    * [6. Show first name and last name concatenated into one column to show their full name.](#easy-question-6)
    * [7. Show first name, last name, and the full province name of each patient.](#easy-question-7)
    * [8. Show how many patients have a birth_date with 2010 as the birth year.](#easy-question-8)
    * [9. Show the first_name, last_name, and height of the patient with the greatest height.](#easy-question-9)
    * [10. Show all columns for patients who have one of the following patient_ids: 1, 45, 534, 879, 1000.](#easy-question-10)
    * [11. Show the total number of admissions.](#easy-question-11)
    * [12. Show all the columns from admissions where the patient was admitted and discharged on the same day.](#easy-question-12)
    * [13. Show the patient id and the total number of admissions for patient_id 579.](#easy-question-13)
    * [14. Based on the cities that our patients live in, show unique cities that are in province_id 'NS'?](#easy-question-14)
    * [15. Write a query to find the first_name, last name and birth date of patients who has height greater than 160 and weight greater than 70.](#easy-question-15)
    * [16. Write a query to find list of patients first_name, last name, and allergies where allergies are not null and are from the city of 'Hamilton'](#easy-question-16)
* [Medium Questions](#medium-questions)
    * [1. Find Unique Birth Years](#medium-question-1)
    * [2. Find Unique First Names](#medium-question-2)
    * [3. Find Patients with First Name Starting and Ending with 's' and at Least 6 Characters](#medium-question-3)
    * [4. Find Patients with Diagnosis 'Dementia'.](#medium-question-4)
    * [5. Order Patients by First Name Length and Alphabetically](#medium-question-5)
    * [6. Count Male and Female Patients](#medium-question-6)
    * [7. Find Patients with Allergies to 'Penicillin' or 'Morphine'](#medium-question-7)
    * [8. Find Patients Admitted Multiple Times for the Same Diagnosis](#medium-question-8)
    * [9. Count Patients per City and Order](#medium-question-9)
    * [10. Identify Patient or Doctor Roles](#medium-question-10)
    * [11. Order Allergies by Popularity](#medium-question-11)
    * [12. Find Patients Born in the 1970s](#medium-question-12)
    * [13. Display Full Name in a Specific Format](#medium-question-13)
    * [14. Calculate Total Height per Province](#medium-question-14)
    * [15. Find Weight Difference for Patients with Last Name 'Maroni'](#medium-question-15)
    * [16. Count Admissions per Day of the Month](#medium-question-16)
    * [17. Find Most Recent Admission for Patient_id 542](#medium-question-17)
    * [18. Find Admissions Matching Specific Criteria](#medium-question-18)
    * [19. Calculate Total Admissions per Doctor](#medium-question-19)
    * [20. Find Doctor's First and Last Admission Dates](#medium-question-20)
    * [21. Count Patients per Province](#medium-question-21)
    * [22. Display Patient, Admission Diagnosis, and Doctor Information](#medium-question-22)
    * [23. Find Duplicate Patients](#medium-question-23)
    * [24. Display Patient Information with Unit Conversions](#medium-question-24)
    * [25. Find Patients with No Admissions](#medium-question-25)
* [Hard Questions](#hard-questions)

## Easy Questions

### <a name="easy-question-1">1. Show first name, last name, and gender of patients whose gender is 'M'</a>
```sql
SELECT
  first_name,
  last_name,
  gender
FROM patients
WHERE gender = 'M';
```
### <a name="easy-question-2">2. Show first name and last name of patients who does not have allergies. (null)</a>
```sql
SELECT
  first_name,
  last_name
FROM patients
WHERE allergies is null
```

### <a name="easy-question-3">3. Show first name of patients that start with the letter 'C'</a>
```sql
SELECT
  first_name 
FROM patients
WHERE first_name like 'C%'
```
### <a name="easy-question-4">4. Show first name and last name of patients that weight within the range of 100 to 120 (inclusive)</a>
```sql
SELECT
  first_name,
  last_name
FROM patients
WHERE weight between 100 and 120
```
### <a name="easy-question-5">5. Update the patients table for the allergies column. If the patient's allergies is null then replace it with 'NKA'</a>
```sql
UPDATE patients
SET allergies = 'NKA'
WHERE allergies is null
```
### <a name="easy-question-6">6. Show first name and last name concatenated into one column to show their full name.</a>
```sql
SELECT
  CONCAT(first_name,' ', last_name)
FROM patients
```
### <a name="easy-question-7">7. Show first name, last name, and the full province name of each patient.</a>
```sql
SELECT
  first_name,
  last_name,
  province_name
FROM patients
  JOIN province_names ON patients.province_id = province_names.province_id
```
### <a name="easy-question-8">8. Show how many patients have a birth_date with 2010 as the birth year.</a>
```sql
SELECT COUNT(*)   
FROM patients
WHERE YEAR(birth_date) = 2010
```
### <a name="easy-question-9">9. Show the first_name, last_name, and height of the patient with the greatest height.</a>
```sql
SELECT
  first_name,
  last_name,
  height
FROM patients
ORDER BY height desc
LIMIT 1
```
### <a name="easy-question-10">10. Show all columns for patients who have one of the following patient_ids: 1, 45, 534, 879, 1000.</a>
```sql
SELECT *
FROM patients
WHERE   
  patient_id IN(1, 45, 534, 879, 1000)
```
### <a name="easy-question-11">11. Show the total number of admissions.</a>
```sql
SELECT COUNT(*)
FROM admissions
```
### <a name="easy-question-12">12. Show all the columns from admissions where the patient was admitted and discharged on the same day.</a>
```sql
SELECT *
FROM admissions
WHERE admission_date = discharge_date
```
### <a name="easy-question-13">13. Show the patient id and the total number of admissions for patient_id 579.</a>
```sql
SELECT
  patient_id,
  COUNT(*)   
FROM admissions
WHERE patient_id = 579
```
### <a name="easy-question-14">14. Based on the cities that our patients live in, show unique cities that are in province_id 'NS'.</a>
```sql
SELECT DISTINCT(city)
FROM patients
WHERE province_id = 'NS'
```
### <a name="easy-question-15">15. Write a query to find the first_name, last name and birth date of patients who has height greater than 160 and weight greater than 70.</a>
```sql
SELECT
  first_name,
  last_name,
  birth_date
FROM patients
WHERE height > 160 AND weight > 70
```
### <a name="easy-question-16">16. Write a query to find list of patients first_name, last name, and allergies where allergies are not null and are from the city of 'Hamilton'.</a>
```sql
SELECT
  first_name,
  last_name,
  allergies
FROM patients
WHERE allergies IS NOT NULL AND city = 'Hamilton'
```




