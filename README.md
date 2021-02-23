# pos2enu
## Premessa
Questo script permette la conversione di un file *.pos risultante dall'elaborazione del software Open Source Rtklib (www.rtklib.com).
In particolare viene effettuata una media pesata (ponderata) sulle coordinate geografiche Lat,Lon,Hei avente in uscita un'unica
coordinata già convertita in un sistema di coordiante piane. (es. UTM33 - EPSG 32633)
Di seguito vengono riportati i passaggi per l'installazione delle dipendenze necessarie al corretto funzionamento dello script.

NB: per il sistema operativo Windows 10 è necessario abilitare la bash di Windows, ad esempio (https://www.lffl.org/2016/08/guida-abilitare-la-bash-windows-10.html)

## Installazione per Debian or Ubuntu Linux
```
$ sudo apt-get update && sudo apt-get upgrade
$ mkdir bin
$ cd $HOME/bin
$ git clone https://github.com/Marcuzzo77/gpsql.git
$ sudo apt-get install -y dialog
$ sudo apt-get update
$ sudo apt-get install l dialog
$ wget -O pgfutter https://github.com/lukasmartinelli/pgfutter/releases/download/v1.2/pgfutter_linux_amd64
$ chmod +x pgfutter
$ echo "export PATH="$PATH:$HOME/bin/gpsql"" >> .bashrc
$ cd gpsql
$ gpsql.sh
$ ./gpsql
```

## Installazione per Mac OSX
```
$ mkdir bin
$ cd $HOME/bin
$ git clone https://github.com/Marcuzzo77/gpsql.git
$ brew install dialog
$ wget -O pgfutter https://github.com/lukasmartinelli/pgfutter/releases/download/v1.2/pgfutter_darwin_amd64
$ chmod +x pgfutter
$ echo 'export PATH="$PATH:$HOME/bin/gpsql"' >> .bashrc
$ cd gpsql
$ gpsql.sh
$ gpsql
````

## Installazione per Windows 10
```
$ sudo apt-get update && sudo apt-get upgrade
$ mkdir bin
$ cd $HOME/bin
$ git clone https://github.com/Marcuzzo77/gpsql.git
$ sudo apt-get install -y dialog
$ wget -O pgfutter https://github.com/lukasmartinelli/pgfutter/releases/download/v1.2/pgfutter_linux_amd64
$ chmod +x pgfutter
$ echo 'export PATH="$PATH:$HOME/bin/gpsql"' >> .bashrc
$ cd gpsql
$ gpsql.sh
```
