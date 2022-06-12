# JQuery

**Inicio función jquery**  
~~~
$(function () {

});
~~~

**jQuery Métodos**  
>El método addClass() agrega uno o más nombres de clase a los elementos seleccionados.
Este método no elimina los atributos de clase existentes, solo agrega uno o más nombres de clase al atributo de clase.  

>El método removeClass() elimina uno o más nombres de clase de los elementos seleccionados.  

>El hasClass() es un método incorporado en jQuery que comprobación de si los elementos con el nombre de la clase especificada existe o no.  

~~~
$(function () {
    $("#titulo-rojo").click(function () {
        $("#inicio h1").addClass('text-danger');
    });

    $("#titulo-negro").click(function () {
        $("#inicio h1").removeClass("text-danger");
    });

    $("#verificar-rojo").click(function () {
        alert($("#inicio h1").hasClass('text-danger'));
    });
});
~~~

**jQuery Métodos**  
>El método append() inserta contenido específico al final de los elementos seleccionados.   

>El método html() establece o devuelve el contenido (innerHTML) de los elementos seleccionados.  
Cuando se usa este método para devolver contenido, devuelve el contenido del PRIMER elemento coincidente.  
Cuando se utiliza este método para configurar el contenido, sobrescribe el contenido de TODOS los elementos coincidentes.  

>El método animate() realiza una animación personalizada de un conjunto de propiedades CSS.  
Este método cambia un elemento de un estado a otro con estilos CSS. El valor de la propiedad CSS se cambia gradualmente para crear un efecto animado.  
Solo se pueden animar valores numéricos (como "margin:30px"). Los valores de cadena no se pueden animar (como "background-color:red"), excepto las cadenas "mostrar", "ocultar" y "alternar". Estos valores permiten ocultar y mostrar el elemento animado.  

~~~
$(function () {
    $("#completar-titulo").click(function () {
        $("#inicio h1").append(" - Sesión Conceptual");
    })

    $("#limpiar-titulo").click(function () {
        $("#inicio h1").html('Javascript Parte II');
    })

    $("#animate").click(function () {
        $("#inicio h1").animate({ 'height': 'toggle' }, 'slow');
    })
});
~~~