<!-- query by group -->
1. Contare quanti iscritti ci sono stati ogni anno
SELECT COUNT(*) AS iscritti_annuali, YEAR(enrolment_date) AS anno FROM students GROUP BY YEAR(enrolment_date)
2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
   SELECT COUNT(office_address)AS numero_di_insegnanti_nello_stesso_stabile, office_address AS indirizzo
FROM teachers 
GROUP BY (office_address)
3. Calcolare la media dei voti di ogni appello d'esame

4. Contare quanti corsi di laurea ci sono per ogni dipartimento