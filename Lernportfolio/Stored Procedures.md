# Stored Procedures
## Was sind Stored Procedures
Stored Procedures sind in der datenbank gespeicherte abläufe. Es ist Gleich wie CTEs einfach das dies befehle. Diese befehle werden direkt in der Datenbank ausgefürt was Performance verbessert.
## Wie macht man eine Stored Precedure
Man Schreibt am anfang Delimiter nach dem schreibt man noch zwei Dollar zeichen hin. Dann schreibt man CREATE PROCEDURE und dann den namben von der Stored Procedure. Dan muss man noch BEGIN und END (Wieder mit $$ am schluss nicht für BEGIN aber.) vor und nach dem Code Schreiben. Ganz am Schluss muss man dann auch nochmals Delimiter hinschreiben min einem abstand und dann noch einem semicolone. Man kann auch verschiedene Parameter mit geben dies is wie mit normalen funktionen in codes. Am Schluss soll es dann wie im folgendem Bild zu sehen ist:

![image](https://github.com/user-attachments/assets/4a69b24d-9128-47cf-8361-b04887f45375)

und dies würde man dann mit CALL GetKundendaten(1); aufrufen.
