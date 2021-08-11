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
>anexos:
>
>>resource: "../src/Routing/anexos.yaml"
### Construccion de una ruta
>anexos_listar:<br>
>
>>path: /anexos<br>
>
>>defaults: {_controller: App\Controller\AnexoController::listar}
### Cambiar configuracion de ruta (src/Views)
>Este cambio se realiza en config/packages/twig.yaml<br>
>twig:
>
>>paths: ['%kernel.project_dir%/src/Views']
>
>>#default_path: '%kernel.project_dir%/templates'
### Buscar fechas timestamp
>SELECT * FROM usuarios.requerimientos WHERE fecha_registro>= '2021-06-21 00:00:00' and  fecha_registro<= '2021-06-21 23:59:59'
### Ruta con variable
>a href="{{ path('usuario_requerimiento_ver',{'id':requerimiento.id}) }}"
### paginacion 
>composer require knplabs/knp-paginator-bundle<br>
>https://github.com/KnpLabs/KnpPaginatorBundle
