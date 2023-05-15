<!-- query con join -->
1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
   SELECT students.name, students.surname
FROM students 
JOIN degrees ON students.degree_id = degrees.id 
WHERE degrees.name = 'Corso di Laurea in Economia';

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze
SELECT `degrees`.`department_id`,`degrees`.`level`, degrees.name
FROM `degrees`
JOIN `departments` ON `departments`.`id`
AND `departments`.`name` = 'Dipartimento di Neuroscienze'
WHERE LEVEL = 'magistrale';
3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
SELECT *
FROM courses
JOIN teachers ON teachers.id = teachers.id
WHERE teachers.id = '44';
4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il
relativo dipartimento, in ordine alfabetico per cognome e nome.
SELECT students.name AS nome_studente,students.surname AS cognome_studente, degrees.name AS nome_corso_di_laurea FROM students JOIN `degrees` ON `degree_id` = `students`.`degree_id` ORDER BY cognome_studente,nome_studente;
5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
SELECT degrees.name AS nome_corso_di_laurea, teachers.name AS nome_insegnante, teachers.surname as cognome_insegnante, courses.name AS nome_corso
FROM course_teacher 
JOIN courses ON course_teacher.course_id = courses.id JOIN degrees ON courses.degree_id = degrees.id JOIN teachers ON course_teacher.teacher_id = teachers.id ORDER BY degrees.name;
6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

7.  BONUS: Selezionare per ogni studente quanti tentativi d’esame ha sostenuto per
superare ciascuno dei suoi esami
