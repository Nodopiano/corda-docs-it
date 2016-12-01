# Configurazione

Corda può essere configurato a piacere per utilizzare un database, delle api e per caricare automaticamente delle variabili nel Container dell'applicazione.

Può anche utilizzare delle variabili per differenziare l'ambiente di sviluppo da quello di produzione. 



## Variabili di Ambiente

Le variabili di ambiente sono inserite nel file .env nella root del progetto. 

Il file va creato al primo avvio, è possibile utilizzare come base il file di esempio '.env-example'.

Contiene informazioni relative al mail server, l'indirizzo di invio e i parametri di mailchimp.



## Variabili di Sistema

Le variabili di sistema sono contenute in files php nella cartella app/config

Ogni file ritorna semplicemente un array di array, che ha come chiavi i nomi delle variabili.
Un file è piuttosto importante, è config.php, che ritorna i nomi di tutti i servizi che vanno caricati:

```php
<?php
return [
    'services' => [
      'api',
      'your-service'
      // etc
    ],
];
```



Aggiungedo un'elemento a questo array, il dependency container cercherà un file di configurazione chiamato come il servizio inserito e lo caricherà con la medesima chiave. 

Ad esempio, il servizio 'api' viene caricato nel container usado come chiave 'api'.


## Container

Per recuperare le chiavi di configurazione inserite nel container basta chiamare il metodo statico get

```pho
App::get('api')
```

e questo ritornerà un array con tutte le configurazioni del servizio 'api'.