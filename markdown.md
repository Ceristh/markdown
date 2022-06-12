# Notas
[markdown](https://joedicastro.com/pages/markdown.html)

GitHub curso udemy push [^fernando_herrera] y documentacion de github [^skills_github]

### Indice
+ [Terminal](#Terminal)  
+ [GitHub](#GitHub)  
+ [HTML](#HTML)  
+ [JQuery](#JQuery)  
+ [JavaScript](#JavaScript)  
+ [Links](#Links)  

## Terminal    

**comandos ocupados frecuentemente:** 
~~~ 
cd assets
mkdir css img js
cd ..
~~~

## GitHub    

**comandos ocupados frecuentemente:**  
*repositorio nuevo: "markdown"
~~~
git init -b main
git add . && git commit -m "initial commit"
git remote add origin https://github.com/Ceristh/markdown.git
git push -u origin main
~~~
~~~
echo "# markdown" >> README.md
git init
git add .
git add README.md
git commit -am "README.md: actualizado"
git log
git branch -m main
git remote add origin https://github.com/Ceristh/markdown.git
git remote set-url origin https://github.com/Ceristh/markdown.git
git pull --rebase origin main
git push -u origin main

**--rebase:** Si extrae cambios remotos con la bandera --rebase, sus cambios locales se vuelven a aplicar sobre los cambios remotos. (rebasing=rebasando)
**--merge:** Si extrae cambios remotos con la bandera --merge, que también es la predeterminada, sus cambios locales se fusionan con los cambios remotos. Esto da como resultado una confirmación de combinación que apunta a la última confirmación local y la última confirmación remota. (merging=fusionan)
~~~

## HTML  

~~~
<table class="table table-bordered">
    <thead>
        <tr>
            <th width="33%">RUT</th>
            <th width="33%">Nombre</th>
            <th width="33%">Correo Electrónico</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td id="rut">rut</td>
            <td id="nombre">nombre</td>
            <td id="email">email</td>
        </tr>
    </tbody>
</table>
~~~

## JQuery  

**Mensaje en consola**  
~~~

~~~

## JavaScript  

**Mensaje en consola**  
~~~
console.log("Mensaje desde script js");
~~~
**Advertencia en consola**  
~~~
console.warn("Mensaje de advertencia");
~~~
**Error en consola**  
~~~
console.error("Mensaje de error");
~~~
**prompt = para ingresar informacion**  
>*getElementById = id en el html - innerHTML = informacion de id dentro de html*
~~~
var nombre = prompt("Ingrese su nombre","");
console.log('El nombre del usuario es ' + nombre);

document.getElementById("nombre").innerHTML = nombre;
~~~
**parseInt = Int especifico para numeros, no letras**  
>*Convierte (parsea) un argumento de tipo cadena y devuelve un entero de la base especificada.*  
>*Si parseInt encuentra un carácter que no es un numeral de la base especificada, lo ignora a él y a todos los caracteres correctos siguientes, devolviendo el valor entero obtenido hasta ese punto. parseInt trunca los números en valores enteros. Se permiten espacios anteriores y posteriores.*  
~~~
var n1 = prompt("Ingrese el \n primer número","5");
var n2 = prompt("Ingrese el segundo número","");

var suma = parseInt(n1) + parseInt(n2);
~~~
**parseFloat = string Las cadenas son útiles para almacenar datos que se pueden representar en forma de texto.**  
>*La función parseFloat() analiza un argumento (si es necesario, lo convierte en una cadena) y devuelve un número de coma flotante.*  
>*string - La cadena (string) que representa al valor que se desea convertir. Si este argumento no es una cadena, entonces, será convertida en una usando la operación abstracta ToString. Se ignora el espacio en blanco inicial en este argumento.*  
~~~
var precio1USD = parseFloat(precio1) * tasa;
var precio2USD = parseFloat(precio2) * tasa;
var precio3USD = parseFloat(precio3) * tasa;

var totalPesos = parseFloat(precio1) + parseFloat(precio2) + parseFloat(precio3);
var totalUSD = parseFloat(precio1USD) + parseFloat(precio2USD) + parseFloat(precio3USD);
~~~
**toFixed(2) = string**  
>*El método toFixed() formatea un número usando notación de punto fijo.*  
>*toFixed() devuelve una representación de cadena de numObj que no usa notación exponencial y tiene exactamente dígitos dígitos después del decimal. El número se redondea si es necesario, y la parte fraccional se rellena con ceros si es necesario para que tenga la longitud especificada*  
~~~
document.getElementById('cuerpo-tabla').innerHTML = `
    <tr>
        <td>${producto1}</td>
        <td>${precio1}</td>
        <td>${precio1USD.toFixed(2)}</td>
    </tr>
`;

document.getElementById('cuerpo-tabla').innerHTML += `
    <tr>
        <td>${producto2}</td>
        <td>${precio2}</td>
        <td>${precio2USD.toFixed(2)}</td>
    </tr>
`;

document.getElementById('cuerpo-tabla').innerHTML += `
    <tr>
        <td>${producto3}</td>
        <td>${precio3}</td>
        <td>${precio3USD.toFixed(2)}</td>
    </tr>
`;
~~~
**document.write = para escribir en documento html - resultado de variables**  
~~~
document.write('El nombre del usuario es ' + nombre);
document.write("<br><strong>"+ n1 + " + " + n2 +" = </strong>"+ suma);
~~~

## Links  
+ [Volver al inicio](#Notas)  


[^fernando_herrera]: https://www.udemy.com/course/git-github/learn/lecture/7380934#overview  
[^skills_github]: https://skills.github.com/   