# Sincronizza l'insegna

Installa comitup sul tuo raspberry nella versione lite, trovi il link [qui](https://steele.debian.net/comitup/image_2020-06-05-Comitup-lite.zip) .

# Installiamo node 

_Per installare node su raspi pi 0 fai questi passaggi

```sh
wget https://nodejs.org/dist/v8.9.0/node-v8.9.0-linux-armv6l.tar.gz
tar -xzf nodexxx.tar.gz
```
_Per installare node su raspi pi2 o pi3 segui questi passaggi

digitare sul terminale

```
uname -m
```
questo servirà a capire che versione di node sarà supportata dal nostro raspi. Adesso scarica la versione giusta da [questo link](https://nodejs.org/en/download/).

Adesso, da terminale, inseriamo wget prima del link preso dal sito precedente 
_In questo modo scaricheremo l'archivio sul nostro computerino_

Estraiamo l'archivio digitando

```
tar -xzf nodexxx.tar.gz
```

>Nel caso in cui il pacchetto sia un .gz

```
tar xvf nodexxx.tar.xz
```

>Nel caso in cui il pacchetto sia un .xz

_"SUGGERIMENTO: quando stiamo per scrivere un nome di un file presente nel sistema clicca su TAB per completare automaticamente il nome del suddetto"_

# Copiamo node in un'altra cartella

Adesso copiamo node in usr/local, uscendo prima dalla cartella

```
cd node-xxxx/
sudo cp -R * /usr/local
```

controlliamo l'installazione con:

```
node -v
npm -v
```
### Installiamo github

Per scaricare github digitiamo

```
sudo apt install git
```
### Scarichiamo e usiamo il file da github

Cloniamo, per prima cosa, la depositories sul raspi digitando

```
git clone https://github.com/mediaintegrati/insegnaraspy.git
```

Dopo aver clonato questo repo assicurati di aver installato l'ultima versione di nodejs. 
Installa pigpio con il seguente codice: 

```
sudo apt install pigpio
```

Installa i moduli richiesti dal package.json  con il comando: 
```
npm i 
```
Installa la libreria pigpio
```
npm install pigpio
```
_Suggerimento: Se non dovesse funzionare utilizza sudo all'inizio

Sei pronto per eseguire il file index.js così:
```
sudo node index.js
```

Il pin PWM è il quinto dal basso, colonna di destra, tenendo la scheda SD del raspy verso l'alto.
Il ground è il quarto dal basso, colonna di destra, tenendo la scheda SD del raspy verso l'alto.
