# SQl-data-cleaning
### INTRODUCE
This is an educational project on data cleaning and preparation using SQL. The original database in CSV format is located in the file club_member_info.csv. Here, we will explore the steps that need to be applied to obtain a cleansed version of the dataset.

### UPDATE FULLNAME
> 	`UPDATE club_member_info_cleaned 
SET full_name = UPPER(full_name)`

### TRIM FULLNAME
`UPDATE club_member_info_cleaned 
SET full_name = TRIM(full_name)`

### TRIM MARTIRAL_STATUS
`UPDATE club_member_info_cleaned 
SET martial_status = TRIM(martial_status) `

### SET BLANK AS NULL
`UPDATE club_member_info_cleaned 
SET martial_status = 'NUll' WHERE martial_status LIKE ''`

### Check Blank age
`select * FROM club_member_info_cleaned cmic 
WHERE age LIKE ''`

### Age
`SELECT * FROM club_member_info_cleaned cmic 
WHERE age > '100'`

`select * from club_member_info_cleaned cmic 
WHERE age < 18 OR age > 90 OR age ISNULL `

`UPDATE club_member_info_cleaned 
SET age = (SELECT MODe(age) from club_member_info_cleaned )
WHERE age < 18 OR age > 90 OR age ISNULL `

`SELECT mode(age)from club_member_info_cleaned cmic `

### Phone
`SELECT * FROM club_member_info_cleaned cmic 
WHERE phone LIKE ''`

`UPDATE club_member_info_cleaned 
SET phone = 'NULL' WHERE phone LIKE ''`

### Full_address
`SELECT * FROM club_member_info_cleaned cmic 
WHERE full_address LIKE ''`

### Job_title
`SELECT * FROM club_member_info_cleaned cmic 
WHERE job_title LIKE ''`

`UPDATE club_member_info_cleaned 
SET job_title = 'NULL' WHERE job_title LIKE ''`

### membership_date
`SELECT * FROM club_member_info_cleaned cmic 
WHERE membership_date LIKE ''`

### Export limit 10 rows
`select * FROM club_member_info_cleaned cmic limit 10;`
