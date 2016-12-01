# WordPress Api



## API

Corda arriva equipaggiato con una funzione molto utile e particolare, un interfaccia semplice e intuitiva per le API di WordPress. 

I metodi disponibili sono  piuttosto eloquenti:



### Posts

```php
public function posts($id)
```

Se riceve un id risponde con il singolo post, altrimenti con tutti i post del sito.

### Pages

```php
public function pages($id)
```

Se riceve un id risponde con la singola pagina, altrimenti con tutte le pagine del sito.



### Usare le API 

Come utilizzare le Api nel proprio controller:

```php
<?php

Use Nodopiano\Corda\WordPress;

Class WordpressController extends Controller 
{
  public function getWordpressApi()
  {
    return (new WordPress)->posts()->get();
  }
  
}
```







## Repository

Se usiamo le API di WordPress in molti controller, può essere noioso importare la libreria e creare un nuovo oggetto in ogni metodo. 

In ogni controller che estende il controller default di Corda è iniettato un repository (Nodopiano\Corda\Repositories\ApiRepository) che permette di utilizzare le api di WordPress in modo più semplice e veloce.

Lo stesso blocco di codice del paragrafo precendente diventa:

```php
Class WordPressController extends Controller
{
	public function getWordpressApi()
	{
        return $this->api->posts()->get();
	}
}

```

In **config/api.php** è possibile specificare quale API utilizzare (non è detto che si usi sempre wordpress) e l'endpoint per le chiamate REST.