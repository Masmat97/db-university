University


1. Selezionare tutti gli studenti nati nel 1990 (160).
    SELECT * FROM students WHERE date_of_birth BETWEEN "1990-01-01"AND "1990-12-31" ORDER BY `id` ASC;

2.  Selezionare tutti i corsi che valgono più di 10 crediti (479).
    SELECT * FROM `courses` WHERE cfu > 10 ORDER BY `id` ASC;

3.  Selezionare tutti gli studenti che ad OGGI hanno almeno 30 anni compiuti (3725).
    SELECT * FROM students WHERE date_of_birth <='1994-06-19';

4.  Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286).
    SELECT * FROM `courses` WHERE period = "I semestre" AND year=1 ORDER BY `id` ASC;

5.  Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21).
    SELECT * FROM `exams` WHERE hour > "14:00:00" AND date = "2020-06-20";

6.  Selezionare tutti i corsi di laurea magistrale (38).
    SELECT * FROM degrees WHERE name LIKE '%magistrale%';

7.  Da quanti dipartimenti è composta l'università? (12).
    SELECT * FROM `departments`;

8.  Quanti sono gli insegnanti che non hanno un numero di telefono? (50).
    SELECT * FROM `teachers` WHERE phone IS NULL;

9.  Inserire nella tabella degli studenti un nuovo record con i propri dati (per il campo degree_id, inserire un valore casuale).
    INSERT INTO students (id,degree_id,name,surname)
    VALUES ('5001', '12', 'Matteo', 'Mascio');

10. Cambiare il numero dell’ufficio del professor Pietro Rizzo in 126.
    UPDATE teachers
    SET office_number = '126'
    WHERE surname LIKE  'Rizzo';

11. Eliminare dalla tabella studenti il record creato precedentemente al punto 9.
    DELETE FROM students WHERE id = 5001;    