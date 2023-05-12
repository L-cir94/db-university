# Consegna DB University
<!-- Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:
- sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
- ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni Corso può essere tenuto da diversi Insegnanti;
- ogni Corso prevede più appelli d'Esame;
- ogni Studente è iscritto ad un solo Corso di Laurea;
- ogni Studente può iscriversi a più appelli di Esame;
- per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.
Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni.
Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.
 -->
## data types

- Strings:  varchar(number), char(number), text, longtext
- numbers: tinyint, small/mendium int, int, bigint
- decimals: float(i, d), double(i,d), decimal(i,d)
- dates: DATETIME, DATE, YEAR, TIME, TIMESTAMP

## attributes

- NULL/NOTNULL
- DEFAULT
- AUTO_INCREMENT
- UNIQUE

## Entity 
- dipartimenti
- corsi di laurea
  - materie
- insegnanti
- appelli_esame
- studenti
  
dipartimento corsi di laurea
- one to many
corsi di laurea e materie 
- many to many
materie e insegnanti
- many to many
appelli di esame e materie
- one to many
appelli d'esame studenti (campo di voto one to one)
- many to many
studenti e corso di laurea 
-  one to many




