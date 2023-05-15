<!-- Dopo aver creato un nuovo database nel vostro phpMyAdmin e aver importato lo schema allegato, eseguite le query del file allegato.
Cosa consegnare?
Dopo aver testato le vostre query con phpMyAdmin, riportatele in un file .md e caricatelo nella vostra repo.
NOTA:
importate il database usando il file che vi ho passato qui sotto esattamente cosí come é.
NON decomprimete il file prima di importarlo.
STEPS:
Avvia MAMP
Vai alla pagine di PHPMYADMIN visitando la webstart page di mamp > tools > phpmyadmin
Nella sidebar di PHPMYADMIN clicca su new per creare un nuovo database, dagli il nome e clicca su create
Clicca sulla sidebar sul nome del db appena creato
nel menu in alto cerca la voce import
clicca su choose filee seleziona il file db_university.sql.gz
 clicca su go in fondo alla pagina -->

<!-- # Selezionare tutti gli studenti nati nel 1990 (160)
SHOW databases; USE 91_university; SHOW tables; DESCRIBE students; SELECT * FROM students WHERE YEAR(date_of_birth) = 1990;
# Selezionare tutti gli studenti che hanno più di 30 anni
SELECT * 
FROM `students`
WHERE TIMESTAMPDIFF(YEAR, `date_of_birth`, CURDATE()) > 30;
# Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)
SELECT * from courses; SELECT * from courses WHERE PERIOD = 'I semestre' AND YEAR = '1';
# Corsi che valgono più di 10 crediti (479)
SHOW tables; DESCRIBE courses; SELECT cfu FROM courses WHERE cfu > 10;
# Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)
SELECT * FROM exams; SELECT * FROM exams WHERE DATE = "2020-06-20" AND HOUR >= "14:00";
# Selezionare tutti i corsi di laurea magistrale (38)
SELECT * from degrees; SELECT * from degrees WHERE LEVEL = "MAGISTRALE";
# Da quanti dipartimenti è composta l'università? (12)
DESCRIBE departments; SELECT ID FROM departments;
# Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
 -->
<!-- query con join -->
1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
   SELECT students.name, students.surname
FROM students 
JOIN degrees ON students.degree_id = degrees.id 
WHERE degrees.name = 'Corso di Laurea in Economia';

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze
3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il
relativo dipartimento, in ordine alfabetico per cognome e nome
1. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
2. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)
3. BONUS: Selezionare per ogni studente quanti tentativi d’esame ha sostenuto per
superare ciascuno dei suoi esami
<!-- query by group -->
1. Contare quanti iscritti ci sono stati ogni anno
2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
3. Calcolare la media dei voti di ogni appello d'esame
4. Contare quanti corsi di laurea ci sono per ogni dipartimento