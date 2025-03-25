# Bulkimport: Mysql Data Loader LOAD DATA INFILE
## CSV-Datei vom Server laden
LOAD DATA INFILE "C:/path/import.csv" ...
## CSV-Datei vom Client laden (Local!)
LOAD DATA LOCAL INFILE "C:/path/import.csv" ...
### Ablauf 
Für dass muss man aber achtung geben da es für normal blockiert ist man muss folgende schritte befolgen.
* Der Server sollte folgende Einstellung haben: ![image](https://github.com/user-attachments/assets/e58f4fc5-4e49-476d-88cd-5a6b8b0bb764)
* Auch sollte kein spezieller Import-Pfad gesetzt sein!![image](https://github.com/user-attachments/assets/88e5f449-e899-4196-ba75-01987fc56fb1)
* Der MySQL.exe-Klient sollte folgende Einstellung im my.ini haben: ![image](https://github.com/user-attachments/assets/f5c8179b-2327-41c2-9b7a-fff31ee36815)
* Bei Workbench muss die "Connection" angepasst werden: OPT_LOCAL_INFILE=1 unter Database > Manage Connections... > "DB" >  Advanced > Others:  einfügen, oder: ![image](https://github.com/user-attachments/assets/5cc5d5ca-f759-44ce-a11b-568923cd3c94)
* Neustart
## LOAD DATA LOCAL INFILE Tipps
### Tabelle 
![image](https://github.com/user-attachments/assets/1db40fa7-171a-491e-b536-8c2047a5fdbc)![image](https://github.com/user-attachments/assets/c32ccc5c-7452-4344-9b84-3f38a21318bc)
### Tips
* Leere Felder und Datumsformat anpassen: ![image](https://github.com/user-attachments/assets/d17d1a15-e08e-4d14-a855-05d53b56eb7b)
* Spaltenreihenfolge ändern: ![image](https://github.com/user-attachments/assets/c5edaccc-6db0-4f64-904c-fbb04a1bb947)
* Spalten auslassen:![image](https://github.com/user-attachments/assets/c0184b43-de9a-4955-92e1-ae0fdf31dfee)
* Attribut hinzufügen:![image](https://github.com/user-attachments/assets/7104e469-ce38-42ab-bdf2-9515ae4fdf6a)
* Werte ändern: ![image](https://github.com/user-attachments/assets/eeedb045-1a81-4fad-a2c5-3a170c449835) Falls es null sein könnte müsste man noch: ![image](https://github.com/user-attachments/assets/426716a7-a234-4150-86d0-082a7c975c1b)
* Daten aus einer anderen Tabelle einfügen: ![image](https://github.com/user-attachments/assets/4fb7fab4-916e-4f04-a112-847197997586)
## Datenbasis DB_Adressen
### [Generator](https://migano.de/testdaten.php)
![image](https://github.com/user-attachments/assets/b8410e97-3539-4378-9421-e27627fc1fb6)
### Finde redundante Datensätze
Die ausgangs position ist: ![image](https://github.com/user-attachments/assets/804d06c4-c8c1-489f-96b4-c79980893554)
* dann macht man eine temporäre tabelle: ![image](https://github.com/user-attachments/assets/62e5a333-bf23-46a2-8b32-2e9ad7d9be56) ![image](https://github.com/user-attachments/assets/c3a345e3-70a9-4e4d-88ee-b4316cfdc228)
* Update die Fk's und ersetzte die alte tabelle: ![Uploading image.png…]()
