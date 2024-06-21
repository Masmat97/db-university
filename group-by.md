1. Contare quanti iscritti ci sono stati ogni anno.

   SELECT COUNT(*), students.enrolment_date FROM students GROUP BY YEAR(enrolment_date);

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio.

   SELECT office_addres AS ufficio,COUNT(*)AS stesso_ufficio FROM `teacher`;


3. Calcolare la media dei voti di ogni appello d'esame.

   SELECT AVG(vote) AS media_voto, exam_student.exam_id AS esame
   FROM `exam_student`
   GROUP BY (exam_id);


4. Contare quanti corsi di laurea ci sono per ogni dipartimento.

   SELECT department_id
   COUNT(*)
   FROM degrees
   GROUP BY department_id;