# SQl-data-cleaning
### INTRODUCE
This is an educational project on data cleaning and preparation using SQL. The original database in CSV format is located in the file club_member_info.csv. Here, we will explore the steps that need to be applied to obtain a cleansed version of the dataset.

### UPDATE FULLNAME
`UPDATE club_member_info_cleaned 
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

|full_name|age|martial_status|email|phone|full_address|job_title|membership_date|
|---------|---|--------------|-----|-----|------------|---------|---------------|
|ADDIE LUSH|40|married|alush0@shutterfly.com|254-389-8708|3226 Eastlawn Pass,Temple,Texas|Assistant Professor|7/31/2013|
|ROCK CRADICK|46|married|rcradick1@newsvine.com|910-566-2007|4 Harbort Avenue,Fayetteville,North Carolina|Programmer III|5/27/2018|
|SYDEL SHARVELL|46|divorced|ssharvell2@amazon.co.jp|702-187-8715|4 School Place,Las Vegas,Nevada|Budget/Accounting Analyst I|10/6/2017|
|CONSTANTIN DE LA CRUZ|35|NUll|co3@bloglines.com|402-688-7162|6 Monument Crossing,Omaha,Nebraska|Desktop Support Technician|10/20/2015|
|GAYLOR REDHOLE|38|married|gredhole4@japanpost.jp|917-394-6001|88 Cherokee Pass,New York City,New York|Legal Assistant|5/29/2019|
|WANDA DEL MAR|44|single|wkunzel5@slideshare.net|937-467-6942|10864 Buhler Plaza,Hamilton,Ohio|Human Resources Assistant IV|3/24/2015|
|JOANN KENEALY|41|married|jkenealy6@bloomberg.com|513-726-9885|733 Hagan Parkway,Cincinnati,Ohio|Accountant IV|4/17/2013|
|JOETE CUDIFF|51|divorced|jcudiff7@ycombinator.com|616-617-0965|975 Dwight Plaza,Grand Rapids,Michigan|Research Nurse|11/16/2014|
|MENDIE ALEXANDRESCU|46|single|malexandrescu8@state.gov|504-918-4753|34 Delladonna Terrace,New Orleans,Louisiana|Systems Administrator III|3/12/1921|
|FEY KLOSS|52|married|fkloss9@godaddy.com|808-177-0318|8976 Jackson Park,Honolulu,Hawaii|Chemical Engineer|11/5/2014|
