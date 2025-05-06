# Backups erzeugen
## Backup-Tools für MySQL/MariaDB

- **MySQLDump**: Wer über einen Shell-Zugang verfügt, kann mit der integrierten (Voll-)Backup-Funktion von MySQL und dem Befehl `mysqldump` arbeiten. Allerdings erlauben nicht alle Hoster den Zugriff auf diese Funktion, die im Übrigen die schnellste Backup-Durchführung ermöglicht.

- **phpMyAdmin**: Mit dieser Administrations-Plattform für SQL-Datenbanken können Benutzer die gewünschte Datenbank einfach im gewünschten Format, z. B. SQL, exportieren. Allerdings kann es dazu kommen, dass das **PHP-Script** bei zu großen Datenbanken vom Server abgebrochen wird. Zudem funktioniert nur die Einspielung von Backups mit einer Größe von bis zu 2 MB.

- **BigDump**: Das Tool BigDump bietet die perfekte Ergänzung zu phpMyAdmin, da es beliebig große Backups wieder einspielen kann. Eine eigene Sicherungs-Funktion bietet es allerdings nicht.

- **HeidiSQL**: Die Backup-Lösung für Windows-Systeme basiert nicht auf PHP und hat daher keine Probleme mit großen Backups. Dem Tool, das ansonsten phpMyAdmin sehr ähnlich ist, fehlt allerdings die Möglichkeit zur Automatisierung des Sicherungsprozesses.

- **Mariabackup**: Ist ein Open-Source-Tool, das von MariaDB bereitgestellt wird, um physische Online-Backups von InnoDB, Aria und MyISAM-Tabellen durchzuführen. Es wurde ursprünglich von Percona XtraBackup abgezweigt. Es ist auf Linux und Windows verfügbar.
