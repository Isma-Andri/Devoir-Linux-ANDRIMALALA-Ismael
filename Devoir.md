# ETAPES DE L'INSTALLATION A PARTIR DE SOURCE

## MySQL 
Télécharger l'archive mysql.tar.gz  
ou copier la source depuis une clé usb  

° Extraction de l'archive puis installation
```bash
cd /rep
tar -xzvf mysql.tar.gz
more README
more INSTALL
#Besoin de cmake, openssl,bison,flex et zlib
sudo apt-get install libssl-dev cmake bison flex zlib1g-dev
mkdir build #(dossier pour les fichiers deconstruction)
cd build/
cmake ..
make
sudo make install
echo 'export PATH=$PATH:/usr/local/mysql/bin' >> /home/mit/.bashrc
source ~/.bashrc
```
<img src="https://github.com/Not-Kira/Intro-/blob/Not-Kira-screenshots/InstallationMYSQL.png" alt="Installation de MySQL terminé">


## Apache
Télécharger l'archive httpd.tar.gz  
ou copier la source depuis une clé usb  

° Extraction de l'archive puis installation
```bash
cd /home/rep #rep est le répertoire contenant httpd.tar.gz
tar -xzvf httpd.tar.gz
cd httpd/
more README
#Besoin de APR, APR-util et PCRE
sudo apt-get install libapr1-dev libaprutil1-dev libpcre3-dev
./configure
#ERROR: C++ compiler missing
sudo apt-get install g++
./configure
make
sudo make install
echo ‘export PATH=$PATH:/usr/local/apache2/bin’  >> ~/.bashrc
source ~/.bashrc
cd /home/rep (rep est le répertoire contenant php.tar.gz)
tar -xzvf php.tar.gz
cd php/
more README
more INSTALL
#Dépendance nécessaire: libxml2,pkg-config,sqlite3
```

<img src="https://github.com/Not-Kira/Intro-/blob/Not-Kira-screenshots/InstallationApache~2.png" alt="Installation de Apache terminé">  

## PHP
Télécharger l'archive httpd.tar.gz  
ou copier la source depuis une clé usb  

° Extraction de l'archive puis installation
```bash
cd /home/rep #(rep est le répertoire contenant php.tar.gz)
tar -xzvf php.tar.gz
cd php/
more README
more INSTALL
#Dépendance nécessaire: libxml2,pkg-config,sqlite3
sudo apt-get install libxml2-dev pkg-config sqlite3
./configure
make
sudo make install
```
<img src="https://github.com/Not-Kira/Intro-/blob/Not-Kira-screenshots/InstallationPHP~2.png" alt="Installation de PHP terminé">  

