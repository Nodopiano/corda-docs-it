# Corda

## Per cominciare

Per cominciare è sufficiente clonare il respository del boilerplate e installare le dipendenze, in questo modo:

```
git clone https://github.com/Nodopiano/wp-api-php-boilerplate.git your-project
composer update
cp .env-example .env
```

a questo punto, configurate il vostro web server per servire i file dalla directory 'public' del progetto e vedrete la home page di Corda!.

## Sviluppare con Corda

Quando sviluppiamo un'applicazione di questo tipo non ha senso attivare apache o nginx per pochi file, ci basta il server integrato di php, per fare prima!
Bastano due comandi per fare quello che ci serve!

```
yarn
yarn start
```

NB: yarn è un gestore di pacchetti javascript estremamente performante, installalo con 
```
npm install -g yarn
```
il browser si aprirà alla pagina localhost:3000, già configurato per l'autoreload delle pagine ad ogni modifica!

