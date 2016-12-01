# Routing e Richieste

## Router

Le route della tua applicazione sono definite in app/routes.php.

Creare una nuova route è molto semplice,  basta chiamare il metodo corrispondente alla richiesta HTTP che si intente fare, passando come parametri

- l'URI che si vuole raggiungere
- un array composto dal controller che dovrà gestire la richiesta e il relativo metodo che verrà chiamato, oppure una funzione anonima per gestire 'al volo' la richiesta.



ecco un esempio di richiesta GET

```php
$router->get('/form', ['App\Controllers\FormController', 'form']);
```



ecco invece un esempio di richiesta POST

```php
$router->post('/form', ['App\Controllers\FormController', 'save']);
```



## Controller

Un controller è una classe che permette attraverso i suoi metodi di gestire ed elaborare le richieste che arrivano dalle route definite nell'applicazione.

Ecco il codice di un semplice controller

```php
<?php
Namespace App\Controllers;

use Nodopiano\Corda\Controller;

class FormController extends Controller
{

    public function form()
    {
      // do something here
    }
}

```

Tutto qui? 

Si, un controller in Corda è davvero molto semplice!
