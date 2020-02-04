# Sincronizza l'insegna

Dopo aver clonato questo repo assicurati di aver installato l'ultima versione di nodejs. 
Installa pigpio con il seguente codice: 

```
sudo apt install pigpio
```

Installa i moduli richiesti dal package.json  con il comando: 
```
npm i 
```

Sei pronto per eseguire il file index.js così:
```
sudo node index.js
```

Il pin PWM è il quinto dal basso, colonna di destra, tenendo la scheda SD del raspy verso l'alto.
Il ground è il quarto dal basso, colonna di destra, tenendo la scheda SD del raspy verso l'alto.
