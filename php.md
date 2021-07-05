### Extaer solo numeros
>$string = '908.354.365-1';
>$outputString = preg_replace('/[^0-9]/', '', $string);
>echo("The extracted numbers are: $outputString \n");
