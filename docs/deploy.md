# Deploy

Sviluppare velocemente un'applicazione avrebbe poco senso se poi si perdono giornate intere per il deploy, giusto?

Corda usa [Laravel Envoy](https://laravel.com/docs/5.3/envoy) per automatizzare le operazioni più comuni, come il deploy.

#### Per installare Laravel Envoy
```
composer global require "laravel/envoy=~1.0"
```

Nel file Envoy.blade.php basterà inserire le variabili del progetto (nome utente sul server, dominio, repository git) e Envoy si occuperà del resto!


