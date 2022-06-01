#install mysql:
    sudo apt install mysql-servermysql-client mycli
#important setting (set password for root)
    sudo mysql_secure_installation
    (choose policy low)
#login mysql as root:
    mysql -u root -p
