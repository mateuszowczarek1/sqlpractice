# SQL Practice
```sql
1. SELECT `first_name`, `last_name`, `gender` FROM patients where `gender` = 'M'
2. SELECT `first_name`, `last_name` FROM patients where `allergies` IS null
3. SELECT `first_name` FROM patients where `first_name` LIKE 'C%'
4. SELECT `first_name`, `last_name` FROM patients where `weight` between 100 AND 120
5. update `patients` set `allergies` = 'NKA' where `allergies` IS NULL;
6. select concat(`first_name`, ' ', `last_name`) as `full_name` FROM `patients`
7. select patients.first_name, patients.last_name, province_names.province_name from `patients` join `province_names` on patients.province_id = province_names.province_id // inner join
8. SELECT COUNT(*) AS total_patients FROM patients WHERE YEAR(birth_date) = 2010;
9. SELECT first_name, last_name, max(height) as height from patients
10. select * FROM patients WHERE patient_id IN(1,45,534,879,1000)
11. SELECT count (*) from admissions
12. SELECT * FROM admissions where admission_date = discharge_date
13. SELECT `patient_id`, count(patient_id) AS total_admissions FROM admissions where `patient_id` = 579
14. SELECT distinct `city` AS `unique_cities`FROM `patients` WHERE `province_id` = 'NS'
15. SELECT first_name, last_name, birth_date from patients where height > 160 and weight > 70
16. select first_name, last_name, allergies from patients  where allergies not null and city = 'Hamilton'
17. select distinct(YEAR(birth_date)) AS birth_year from patients ORDER BY birth_year asc
18. select distinct(first_name) from patients group by first_name having count(`first_name`) = 1
19. select patient_id, first_name from patients where first_name like 's%s' and len(first_name) >= 6
20. select patients.patient_id, patients.first_name, patients.last_name FROM patients join admissions on patients.patient_id = admissions.patient_id where admissions.diagnosis = 'Dementia'
```