University


1.  SELECT * FROM students WHERE date_of_birth BETWEEN "1990-01-01"AND "1990-12-31" ORDER BY `id` ASC;
2.  SELECT * FROM `courses` WHERE cfu > 10 ORDER BY `id` ASC;
3.  SELECT * FROM students WHERE date_of_birth <='1994-06-19';
4.  SELECT * FROM `courses` WHERE period = "I semestre" AND year=1 ORDER BY `id` ASC;
5.  SELECT * FROM `exams` WHERE hour > "14:00:00" AND date = "2020-06-20";
6.  SELECT * FROM degrees WHERE name LIKE '%magistrale%';
7.  SELECT * FROM `departments`;
8.  SELECT * FROM `teachers` WHERE phone IS NULL;
9.  INSERT INTO students (id,degree_id,name,surname)
    VALUES ('5001', '12', 'Matteo', 'Mascio');
10. UPDATE teachers
    SET office_number = '126'
    WHERE surname LIKE  'Rizzo';
11. DELETE FROM students WHERE id = 5001;    