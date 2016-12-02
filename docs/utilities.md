# Utility

Quante volte capita di fare e rifare sempre le stesse cose?

A noi capita sempre di dover mandare una Mail da un form di contatto, iscrivere un utente ad una newsletter su mailchimp, salvare i dati del form in un semplice file CSV.

Corda ha tre classi omonime che permettono con poco sforzo di eseguire queste operazioni.



## Mail

Vuoi mandare una mail? 

```php
Mail::send($mail_to,$subject,$message);
```

ecco fatto ;)

NB: Ricorda di impostare l'indirizzo di invio nel file .env

## Newsletter

```php
NewsLetter::subscribe('LIST_ID_NUMBER',array('email' => $email_address));
```

Il fornitore di newsletter di default è Mailchimp.

NB: ricorda di impostare il tuo MailChimp Api ID nel file .env 



## CSV

```php
Csv::export(array($mail_to, $message,$other_field), $filename);
```

il file sarà salvato in app/storage/csv/ 

