#### 1. test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
`CREATE TABLE employee(
	id INTEGER,
	name VARCHAR(50),
	birthday DATE,
	email VARCHAR(100)
);`

#### 2. Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
`UPDATE employee
SET name = 'Ikra'
WHERE name = 'Aubrey'`

`UPDATE employee
SET birthday = '1964-06-20'
WHERE id = 45;`

`UPDATE employee
SET name = 'Ayşe',
	  email = 'ayse@gmail.com'
WHERE name = 'Pippa';	`

`UPDATE employee
SET name = 'Rosita',
	birthday = '2000-06-08',
	email = 'rosita@statcounter.com'
WHERE name = 'Roselia';`

`UPDATE employee
SET birthday = '2003-08-01'
WHERE id = 7
RETURNING*;`

#### 3. Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
`DELETE FROM employee
WHERE name = 'Ikra';`

`DELETE FROM employee
WHERE id = 45;`

`DELETE FROM employee
WHERE name = 'Ayşe';`

`DELETE FROM employee
WHERE birthday > '2000-05-06'
RETURNING * ;`

`DELETE FROM employee
WHERE birthday > '1979-01-01'
RETURNING *;`
