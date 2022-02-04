# P6-AIC
Sauvegarde mysql script python 
ce script permet de faire un sauvegarde quotidien de la base de données sql sur un serveur ftp 
Installation d'un serveur LAMP sous Debian 11 (Linux - Apache - MySQL / MariaDB - PHP).
Installer et configurer le serveur FTP "ProFTPD" sous Debian 11
# Mise en place d'un script dans le but d'automatiser la sauvegarde de base de données. 
Version du script : 1.4
Tester avec : python3 sur linux
# le nom de la base de données à sauvegarder.
DB_NAME = 'wp202110_itgrace'
# le nom d'utilisateur  de la base de données.
DB_USER = 'root'
# le repertoire de sauvegarde
BACKUP_PATH = '/backup/dbbackup/'
# Rendre le script executable avec la commande 
chmod +x dbbackup.py
# Executer le script comme ceci
python3 sauvegarde_Wordpress.py.3
# Planifier l'execution du script par intervalle regulier  de 2 heures à l'aide de crontab
crontab -e
0 2 * * python3 /usr/local/bin
