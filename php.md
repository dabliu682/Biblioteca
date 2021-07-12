### Extaer solo numeros
$string = '908.354.365-1';<br>
$outputString = preg_replace('/[^0-9]/', '', $string);<br>
echo("The extracted numbers are: $outputString \n");
### Reemplazar algo en una cadena de texto
>$informes=$form['informes'];<br>
>$outputString = str_replace(' ', '_', $informes);
