# ETAPES DE L'INSTALLATION A PARTIR DE SOURCE

## MySQL 
Télécharger l'archive mysql.tar.gz  
ou copier la source depuis une clé usb  

° Extraction de l'archive  
```bash
cd /rep
tar -xzvf mysql.tar.gz

```
```bash
more README
more INSTALL
```

° Besoin de cmake, openssl,bison,flex et zlib  
```bash
sudo apt-get install libssl-dev cmake bison flex zlib1g-dev
```

° Configuration et construction  
```bash
mkdir build #(dossier pour les fichiers deconstruction)
cd build/
cmake ..
make
```
° Installation
```bash
sudo make install
```
° Ajouter mysql au variable d'environnement PATH  
```bash
echo 'export PATH=$PATH:/usr/local/mysql/bin' >> /home/mit/.bashrc
source ~/.bashrc
```
Screenshot:
<img src="https://github.com/Not-Kira/Intro-/blob/Not-Kira-screenshots/InstallationMYSQL.png" alt="Installation de MySQL terminé">  
Pour afficher la version installée :
```bash
mysql --version
```


## Apache
Télécharger l'archive httpd.tar.gz  
ou copier la source depuis une clé usb  

° Extraction de l'archive  
```bash
cd /home/rep #rep est le répertoire contenant httpd.tar.gz
tar -xzvf httpd.tar.gz
cd httpd/
```
```bash
more README
```
° Besoin de APR, APR-util et PCRE  
```bash
sudo apt-get install libapr1-dev libaprutil1-dev libpcre3-dev
```
° Configuration
```bash
./configure
```
#ERROR: C++ compiler missing  
```bash
sudo apt-get install g++
```
*refaire la configuration 
```bash
./configure
```
° Installation
```bash
make
sudo make install
```
° Ajouter apache à l'environnement PATH  
```bash
echo ‘export PATH=$PATH:/usr/local/apache2/bin’  >> ~/.bashrc
source ~/.bashrc
```
Screenshot:
<img src="https://github.com/Not-Kira/Intro-/blob/Not-Kira-screenshots/InstallationApache~2.png" alt="Installation de Apache terminé">  
Pour afficher la version installée :
```bash
httpd -v
```

## PHP
Télécharger l'archive httpd.tar.gz  
ou copier la source depuis une clé usb  

° Extraction de l'archive  
```bash
cd /home/rep #(rep est le répertoire contenant php.tar.gz)
tar -xzvf php.tar.gz
cd php/
```
```bash
more README
more INSTALL
```
#Dépendance nécessaire: libxml2,pkg-config,sqlite3
```bash
sudo apt-get install libxml2-dev pkg-config sqlite3
```
° Configuration  
```bash
./configure
make
```
° Installation
```bash
sudo make install
```
Screenshot:
<img src="https://github.com/Not-Kira/Intro-/blob/Not-Kira-screenshots/InstallationPHP~2.png" alt="Installation de PHP terminé">  
Pour afficher la version installée :  
```bash
php -v
```
