# pos2enu
## Premessa
pos2enu è uno script shell scritto in tcsh che permette la conversione di un file *.pos risultante dall'elaborazione del software Open Source Rtklib (www.rtklib.com).
In particolare viene effettuata una media pesata (ponderata) sulle coordinate geografiche Lat,Lon,Hei avente in uscita un'unica
coordinata già convertita in un sistema di coordinate piane. (default UTM33 - EPSG 32633)
Di seguito vengono riportati i passaggi per l'installazione delle dipendenze necessarie al corretto funzionamento dello script.
Attualmente è possibile convertire il file *.pos avente per risultato finale la media pesata in coordinate piane a seconda dell'EPSG impostato nella variabile iniziale dello script.

NB: per il sistema operativo Windows 10 è necessario abilitare la bash di Windows, ad esempio (https://www.lffl.org/2016/08/guida-abilitare-la-bash-windows-10.html)

## Installazione per Debian or Ubuntu Linux
```
$ sudo apt-get update && sudo apt-get upgrade
$ sudo apt-get install proj-bin
$ mkdir bin
$ cd $HOME/bin
$ git clone https://github.com/marcuzz0/pos2enu.git
$ echo "export PATH="$PATH:$HOME/bin/pos2enu"" >> .bashrc
```

## Installazione per Mac OSX
```
$ brew install proj
$ mkdir bin
$ cd $HOME/bin
$ git clone https://github.com/marcuzz0/pos2enu.git
$ echo 'export PATH="$PATH:$HOME/bin/pos2enu"' >> .bashrc
````

## Installazione per Windows 10
```
$ sudo apt-get update && sudo apt-get upgrade
$ sudo apt-get install proj-bin
$ mkdir bin
$ cd $HOME/bin
$ git clone https://github.com/marcuzz0/pos2enu.git
$ echo "export PATH="$PATH:$HOME/bin/pos2enu"" >> .bashrc
```

## Come si utilizza
```
$ pos2enu /percorso_del_file_da_convertire
```
