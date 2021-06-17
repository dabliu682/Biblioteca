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
><img style="border: 1px solid;" class="d-block w-100" src="{{ 'data:image;base64,'~requerimiento.anexo2 }}">
