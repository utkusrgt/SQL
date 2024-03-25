CREATE TABLE employee (
    id SERIAL PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
	birthday DATE,
	email VARCHAR(100)
	);

UPDATE employee
SET first_name = 'UPDATED'
	WHERE first_name LIKE 'A%'
	RETURNING *;

DELETE FROM employee

    WHERE id IN (1,2,3,4,5)
    RETURNING *;