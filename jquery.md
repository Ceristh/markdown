# JQuery

**Inicio función jquery**  
~~~
$(function () {

});
~~~

**jQuery Métodos hover**  
>El .hover() método vincula los controladores para los eventos mouseentery mouseleave. Puede usarlo para simplemente aplicar comportamiento a un elemento durante el tiempo que el mouse está dentro del elemento.   

~~~
$(function () {
    $("#mostrar-ocultar").hover(
		//Primer función se dispara cuando el mouse se posiciona en el elemento
		function(){
			$("#contenedor-imagen").css({ 'display':'block'})
		},
		//Segunda función se dispara cuando el mouse se retira del elemento
		function(){
			$("#contenedor-imagen").css('display','none')
		}
	);
});
~~~

**jQuery Métodos addClass-removeClass-hasClass**  
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

**jQuery Métodos append-html-animate**  
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

**jQuery Métodos attr**  
>El método attr() establece o devuelve atributos y valores de los elementos seleccionados.  
Cuando se usa este método para devolver el valor del atributo, devuelve el valor del PRIMER elemento coincidente.  
Cuando se utiliza este método para establecer valores de atributo, establece uno o más pares de atributo/valor para el conjunto de elementos coincidentes.  

+ js
~~~
$("#selector-clases button, #selector-clases .btn").click(function(){
    var fondo = $(this).data('fondo');
    
    $("#cambio-color").attr('class', 'mt-4');
	$("#cambio-color").addClass(fondo);
});
~~~
+ HTML
~~~
<section id="selector-clases" class="container">
		<h2 class="mt-5" data-fondo="bg-primary">Selector por clases</h2>

		<button type="button" class="btn btn-success" data-fondo="bg-success" data-nombre="Primero">Success</button>
		<button type="button" class="btn btn-primary" data-fondo="bg-primary" data-nombre="Segundo">Primary</button>
		<button type="button" class="btn btn-info" data-fondo="bg-info" data-nombre="Tercero">Info</button>

		<div id="cambio-color" class="mt-4 p-2">
			<h4>Cambio de color</h4>
		</div>

</section>
~~~