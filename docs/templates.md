# Templates e View

Corda usa Twig, un sistema di template html per PHP. 
Si rimanda alla [documentazione di Twig](http://twig.sensiolabs.org/doc/templates.html) per i dettagli.

Corda è già preimpostato con una master view (views/app.html) che può essere modificata a seconda delle proprie esigenze. Al suo interno vengono inseriti gli altri template chiamati dalle view.

## View

Come fare per rispondere con una view da un controller? 
Corda offre un comodo metodo globale view() che riceve due parametri:

- il nome del file html 
- un array con le variabili da passare alla vista.

```
  return view('index.html',array('message' => 'Hello!'));
```

Ecco fatto! sarà costruita una view usando il template _index.html_ e passando la variabile _message_.

## Response

Ma come fare quando quello che voglio ritornare non è un vista ma un semplice json? 
Corda ha un altro metodo globale, che si chiama, guardacaso, json().

Riceve un array di variabili che andranno convertite e ritornate in formato json.
```
  return json($this->api->pages(61));
```

