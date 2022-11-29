
### um in den psql-modus zu gelangen
psql

### für Hilfe über SQL-Anweisungen
\h 

### für Hilfe über interne Anweisungen
\?  

### oder Semikolon, um eine Anfrage auszuführen
\g 

### um zu beenden
\q 

### listet alle Datenbanken
\l 

### Erstelle neue Datenbank
CREATE DATABASE databasename;


### Verbinde mit Datenbank (test1)
psql -h localhost -p 5432 -U postgres test1
+ wenn nicht auf eigenem Rechner statt localhost ipadresse 
+ alternative: \c test1

### Löschen einer Datenbank (test1)
###### !!! Alle Daten weg !!!
DROP DATABASE test1;

### Erstellen einer Tabelle
CREATE TABLE table_name(
    Column name + data type + constraints*
)
###### data types: 
+ boolean
1,yes,y,t,true entspricht true
0, no, false f entspricht false 
+ VARCHAR(n)
Variable Länge eines Strings. Entgegen CHAR(n) wird die Länge nicht auf n aufgefüllt, wenn kürzer
+ TEXT
Unlimitierte Textlänge
+ SMALLINT / INT 
Ganzzahlen
+ SERIAL / BIGSERIAL
Perfekt für ID / PRiMARY KEY
Zählt hoch
+ float(n)
Genauigkeit von n Stellen
+ float8 oder real
TIME, DATE, TIMESTAMP
JSON
...
https://www.geeksforgeeks.org/postgresql-data-types/

### Contraints für Tabellenspalte
+ NOT NULL
+ PRIMARY KEY

### Zeige alle Tabellen 
\d
\d tabellenname 
+ genaue beschreibung einer Tabelle

### Einfügen Insert in Tabelle 
INSERT INTO (spalte1, spalte2...) VALUES ('wert1', 'wert1',..., DATE '1990-12-19')
+ DATE damit der Wert als DAtum interpretiert wird und nicht als String




