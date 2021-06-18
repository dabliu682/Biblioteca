## Comandos Symfony 5
### Cargar Data Fixture
>php bin/console doctrine:fixtures:load
### Correr Migraciones
> php bin/console doctrine:migrations:migrate
### Obtener rol de usuario en twig
> app.user.roles[0]
### Limpiar cache
>php bin/console cache:clear
### Colocar imagen base 64 en twig
>img style="border: 1px solid;" class="d-block w-100" src="{{ 'data:image;base64,'~requerimiento.anexo2 }}"
### Cambiar configuracion de ruta (src/Routing)
>Este cambio se realiza en config/routes.yaml<br>
>anexos:resource: "../src/Routing/anexos.yaml"
### Construccion de una ruta
>anexos_listar:<br>
>
>>path: /anexos<br>
>
>>defaults: {_controller: App\Controller\AnexoController::listar}

