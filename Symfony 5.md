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
### Permisos carpeta
>chmod 777 * -R carpeta/
### Crear link
> $this->addsql("insert into central.accesoxmodulos (opcion, nivel, madre, ruta, frame, modulogr, id, orden, parametros) values('Contabilidad',0,'','portada_contabilidad','','Contabilidad',nextval('central.accesoxmodulos_id_seq'),1,'')");<br>
> $this->addsql("INSERT INTO central.accesoxmodulos( opcion, nivel, madre, ruta, frame, modulogr, id, orden, parametros)VALUES ('Separator', 2, 'Configuracion', null, null, 'Contabilidad', nextval('central.accesoxmodulos_id_seq'), 19, null)");<br>
> $this->addsql("INSERT INTO central.accesoxmodulos( opcion, nivel, madre, ruta, frame, modulogr, id, orden, parametros)VALUES ('Programacion diferidos', 2, 'Configuracion','conta_programacionDiferidos', '', 'Contabilidad', nextval('central.accesoxmodulos_id_seq'), 20, ''));

$this->addsql("INSERT INTO central.accesoxmodulos( opcion, nivel, madre, ruta, frame, modulogr, id, orden, parametros) VALUES ('Separator', 2, 'Procesos', null, null, 'Contabilidad', nextval('central.accesoxmodulos_id_seq'), 20, null)");
$this->addsql("INSERT INTO central.accesoxmodulos( opcion, nivel, madre, ruta, frame, modulogr, id, orden, parametros)VALUES ('Ejecutar diferidos', 2, 'Procesos','conta_ejecutarDiferidos', '', 'Contabilidad', nextval('central.accesoxmodulos_id_seq'), 21, '')");


### Crear una aplicacion
> composer create-project symfony/website-skeleton miprimerproyecto
### Archivo base64 prueba
> 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4HvS45kPyGkc+ER95EfSo6YmLgI3pEkDn6mP3BIn+Kjb7cPzQv4/sXGxWusjw0/CrEJKSsPvP5rZBBeub/V6jmgKZW5kc3RyZWFtCmVuZG9iagoKOSAwIG9iago8PC9UeXBlL0ZvbnQvU3VidHlwZS9UcnVlVHlwZS9CYXNlRm9udC9CQUFBQUErTGliZXJhdGlvblNlcmlmCi9GaXJzdENoYXIgMAovTGFzdENoYXIgMTUKL1dpZHRoc1s3NzcgNzIyIDUwMCA0NDMgNTAwIDc3NyA0NDMgNTAwIDI3NyAyNTAgNTAwIDUwMCAzMzMgMzMzIDUwMCA0NDMKXQovRm9udERlc2NyaXB0b3IgNyAwIFIKL1RvVW5pY29kZSA4IDAgUgo+PgplbmRvYmoKCjEwIDAgb2JqCjw8L0YxIDkgMCBSCj4+CmVuZG9iagoKMTEgMCBvYmoKPDwvRm9udCAxMCAwIFIKL1Byb2NTZXRbL1BERi9UZXh0XQo+PgplbmRvYmoKCjEgMCBvYmoKPDwvVHlwZS9QYWdlL1BhcmVudCA0IDAgUi9SZXNvdXJjZXMgMTEgMCBSL01lZGlhQm94WzAgMCA2MTIgNzkyXS9Hcm91cDw8L1MvVHJhbnNwYXJlbmN5L0NTL0RldmljZVJHQi9JIHRydWU+Pi9Db250ZW50cyAyIDAgUj4+CmVuZG9iagoKNCAwIG9iago8PC9UeXBlL1BhZ2VzCi9SZXNvdXJjZXMgMTEgMCBSCi9NZWRpYUJveFsgMCAwIDYxMiA3OTIgXQovS2lkc1sgMSAwIFIgXQovQ291bnQgMT4+CmVuZG9iagoKMTIgMCBvYmoKPDwvVHlwZS9DYXRhbG9nL1BhZ2VzIDQgMCBSCi9PcGVuQWN0aW9uWzEgMCBSIC9YWVogbnVsbCBudWxsIDBdCi9MYW5nKGVzLUNPKQo+PgplbmRvYmoKCjEzIDAgb2JqCjw8L0NyZWF0b3I8RkVGRjAwNTcwMDcyMDA2OTAwNzQwMDY1MDA3Mj4KL1Byb2R1Y2VyPEZFRkYwMDRDMDA2OTAwNjIwMDcyMDA2NTAwNEYwMDY2MDA2NjAwNjkwMDYzMDA2NTAwMjAwMDM3MDAyRTAwMzE+Ci9DcmVhdGlvbkRhdGUoRDoyMDIxMDYwMzEwMTMxOS0wNScwMCcpPj4KZW5kb2JqCgp4cmVmCjAgMTQKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDA3NTkxIDAwMDAwIG4gCjAwMDAwMDAwMTkgMDAwMDAgbiAKMDAwMDAwMDIzMCAwMDAwMCBuIAowMDAwMDA3NzM0IDAwMDAwIG4gCjAwMDAwMDAyNTAgMDAwMDAgbiAKMDAwMDAwNjcxMCAwMDAwMCBuIAowMDAwMDA2NzMxIDAwMDAwIG4gCjAwMDAwMDY5MjYgMDAwMDAgbiAKMDAwMDAwNzI4NCAwMDAwMCBuIAowMDAwMDA3NTA0IDAwMDAwIG4gCjAwMDAwMDc1MzYgMDAwMDAgbiAKMDAwMDAwNzgzMyAwMDAwMCBuIAowMDAwMDA3OTMwIDAwMDAwIG4gCnRyYWlsZXIKPDwvU2l6ZSAxNC9Sb290IDEyIDAgUgovSW5mbyAxMyAwIFIKL0lEIFsgPDc5MjIzMUJBREVBRTk1QkIzRUM3RjM1M0Q4NTZEMUM0Pgo8NzkyMjMxQkFERUFFOTVCQjNFQzdGMzUzRDg1NkQxQzQ+IF0KL0RvY0NoZWNrc3VtIC82MDdCNjlBRjQyNkREMUUwQkQyMUVGRDkyODBBN0FBOAo+PgpzdGFydHhyZWYKODEwNQolJUVPRgo=
### Envio de archivos ftp
> https://github.com/dg/ftp-php<br>
> https://packagist.org/packages/ijanki/ftp-bundle
### Consulta sql limpio
>$consDoc="select * from contabilidad.saldoxdocumentos where docSoporte=:docSoporte and id_cuenta=:idCuenta and id_tercero=:idTercero and saldo>0 order by saldo desc Limit 1";<br>
>$Parameters=array(':docSoporte'=>$detContable['docsoporte'],':idCuenta'=>$detContable['cuenta'],':idTercero'=>$detContable['tercero']);<br>
>$result = $bd->getConnection()->prepare($consDoc);<br>
>$result->execute($Parameters);<br>
>$existeDoc = $result->fetchAll();<br>
### Validar tipo y peso de archivo
>$(document).on('change','input[type="file"]',function()<br>
>        {<br>
>            var fileName = this.files[0].name;<br>
>            var fileSize = this.files[0].size;<br>
>            var label = document.querySelector('.labelArchivo');<br>

>           if(fileSize > 2000000)<br>
>            {<br>
>                this.value = '';<br>
>                label.textContent='Seleccione una imagen'<br>
>                bootbox.alert("El archivo no debe superar los 2MB");<br>
>            }<br>
>            else<br>
>            {<br>
>                var ext = fileName.split('.').pop();<br>
>                ext = ext.toLowerCase();<br>
>                switch (ext)<br>
>                {<br>
>                    case 'jpg':<br>
>                    case 'jpeg':<br>
>                    case 'png':<br>
>                    case 'pdf':<br>
>                        break;<br>
>                    default:<br>
>                        this.value = '';<br>
>                        label.textContent='Seleccione una imagen'<br>
>                        bootbox.alert("Archivo no admitido");<br>
>                }<br>
>            }<br>
>        });<br>
