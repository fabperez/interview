# interview

### ¿Puede describir la diferencia entre "Progressive Enhancement" y "Graceful Degradation"?
PR es hacer un producto accesible en todos los browsers, es decir, como programar del browser mas viejo al mas nuevo.
GD desarrollar con las característica mas actuales y tratar de arreglar las “trabas”  ya sea con librerias de javascript, plugins o un mensaje de actualización para el usuario.

### ¿Puede describir el proceso que sigue cuando crea una página web?
Dependendiendo del tipo del proyecto puedo o usar generadores con Yeoman, o crear el Scaffolding manualmente. En caso de ser la segunda opción realizo los siguiente pasos:
	•	Creación de archivo index.html. (php, jsp, dependiendo del proyecto)
	•	Crear estructura de carpetas para recursos del sitio:
	◦	CSS - Archivos css
	◦	IMAGES - Imágenes
	◦	JS - Archivos Javascript
	◦	ASSETS - Librerías. (jquery, modernizr, prototype, etc.)
	◦	FONTS - Fuentes tipográficas.

### ¿Cómo optimizaría los recursos de un sitio web?
* Evitar los CSS @import
* Colocar el CSS en la cabecera
* Minimizar el CSS, HTML o Javascript
* Evitar redirecciones innecesarias
* Cacheo del contenido en el browser
* Uso de "Sprites CSS".

### ¿Qué herramientas usa para probar el rendimiento de su código?
* JSPerf (http://jsperf.com/)

### ¿Qué es el DocType?
El doctype es la declaración de tipo de documento.
* DTD es dónde se define la estructura que debe tener el documento y utilizamos el doctype para informar qué DTD usamos. Algunos: 
    * XML 
    * SGML 
    * HTML Strict
    * XHTML.

### ¿Cuál es la diferencia entre “visibility:hidden” y “display:none”?
Display: none. El elemento se ocultará y en la página se mostrará como si el elemento no estuviera. 

visibility: hidden. El elemento aún ocupará el mismo espacio que antes. El elemento se ocultará, pero aún afecta al diseño.

### ¿Mencione al menos 5 eventos JQuery?
Ready(), focus(), keypress(), click(), mouseover()

### ¿Como diseñarias tres columnas de texto en una zona de contenido?
Usando la propiedad float.

### ¿Sabes las diferencias entre null y undefined en Javascript?
Undefined quiere decir que la variable ha sido declarada pero que aun no tiene un valor asignado. Undefined es un tipo.

Null es un valor asignado. Puede ser asignado a la variable como representacion de que no tiene valor. Null es un objeto.

### ¿Sabes como crear un objeto en Javascript?
```javascript
var person = { firstName: "John", eyeColor: "blue" , age:50 };
```

### ¿Porque es recomendable usar el evento $(document).ready()?
Nos indica una señal de que el documento esta listo para ser manipulado con Jquery.

### ¿Sabes las diferencias entre un id y una clase?
Una clase puede ser utilizada muchas veces in un mismo documento de HTML, pero un ID solo lo puedes usar una vez.

### ¿Dfierencia de usar var en la declaración y cuándo no?
Si declaro la variable en el ámbito global puedo usar o no usar var. Si declaro la variable dentro de una función con la palabra var entonces estoy creando una variable de ámbito local, Si no uso var entonces la variable se creara como ámbito global.

```javascript
function(){
var a = 3;// Local
c =2;// Global
}
```

### ¿Qué significa el atributo defer/async cuándo se añade a la etiqueta script? 
* Async: Podremos especificar que dicho archivo pueda ser ejecutado de manera asíncrona, sin que el código HTML se vea bloqueado por su presencia.
```javascript
<script async src="script.js"> 
```
* Defer: permite indicar que el script se ejecutará una vez se haya cargado el resto de la página. 
``` javascript 
<script defer src="script.js">
```

### ¿Cuál es la diferencia entre == y ===?
* == Compara dos valores y devuelve true si ambos son iguales.
* === igualdad estricta o idéntica. Similar a == pero también compara el tipo de datos.
```javascript
var a = 1;
if(a == '1'){..} // return true
if(a === 1){...} // return false
```
### ¿Cómo compruebas si una variable es nulo ó undefined?
Haciendo una condición a la variable. Por ejemplo: 
```javascript
(variable !== null)
```

### ¿Cómo compruebas si una variable es un objeto?
Usando typeof(var), instanceof.

### ¿Qué son los closures?
Un closure es la manera en como una función dentro de otra función contenedora puede hacer referencia a las variables después de que la función contenedora ha terminado de ejecutarse.

### ¿Cómo haces una depuración en JavaScript? 
* Breakpoints
* console.log()

### ¿Diferencia entre window.onload y onDocumentReady?
Ready después de que el HTML ha sido cargado, onload cuando el html mas recursos de la pagina han sido cargados por ejemplo: imágenes, videos, otros.

### ¿En que parte del documento es más recomendable agregar los links y scripts: header o footer?
* Etiquetas <link> en el header.  
* Los scripts hasta abajo, antes de cerrar la etiqueta body

Es más recomendable porque le damos lugar a que se cargue todo el documento HTML con sus estilos y después trabajar con la funcionalidad del Javascript evitando que la página se detenga para ejecutar primero las funcionalidades del Javascript. Haciendo esto le damos un mejor rendimiento y velocidad a la pagina web.

### ¿Cuál es el resultado de: "1"+2+4?
Convierte todos los números a cadena y los concatena dando un resultado de: 124
```javascript
var a = "1" + 2 + 4; // 124
var b = 5 + 4+ "3"; // 93
var c = "4" + 2 * 2; // 44
```

### ¿Cómo puedes cambiar la clase o estilo de un elemento en JavaScript?
```javascript
var elements = document.getElementsByClassName('bordergreen');
var el = elements[0];
el.className = 'borderred';
```
Si el elemento tiene un ID:
```javascript
document.getElementById('divBorde').style.border = '1px solid red';
```

### ¿Qué es el Javascript no obstrusivo y cómo lo implementas?
El Javascript no obstrusivo es aquel que está totalmente separado de la información – estructura de la página.      

La forma de implementarlo es colocando las líneas de código Javascript en un archivo externo o también dentro de la etiqueta <head> pero es mas recomendable colocarlo en un archivo externo.

### ¿Cómo se utilizan los namespaces en Javascript?
Definiendo las variables dentro de un contenedor único, este contenedor es llamado espacio de nombres (namespace). Podemos definir un objeto y dentro de este objeto declarar las variables. Ejemplo:
```javascript
var myProject = {
    var1: "una variable",
    var2 = "otra variable",
    var3 = { uno: 1, dos: 2 };
    doSomething = function () { ... }
}
```
Accedemos a las variables como myProject.var1

### ¿Qué tipos de datos soporta Javascript?
Cadenas, numéricas, undefined, booleanas.

### ¿Cuál es la diferencia entre innerHTML y append?
* innerHTML : cambia el contenido de un elemento.
* append: es un método Jquery que podemos usar para insertar contenido en el extremo de los elementos seleccionados.

### ¿Mencione algunas etiquetas del HTML5?
article, header, footer, nav, section

### ¿Qué son sprites?
Es un conjunto de imágenes diferentes agrupadas todas ellas en una misma imagen.

No podemos usar <span> para crear los contenedores porque span es un elemento inline y necesitamos aplicar width y height, y hay que recordar lo siguiente: “width y height son sólo aplicables a elementos tipo block y elementos insertados en una posición que son reemplazados por un objeto (entre ellos img, input, textarea, select, object)”. Usaremos por tanto elementos div para crear las divisiones.

### Diferencias entre "display:" inline vs inline-block vs block
* inline no respeta width, height, margins, paddings. Los coloca al lado. 
* block coloca uno debajo del otro.
* inline-block los coloca uno al lado del otro pero respeta width, height, margins.

### Describa la diferencia entre cookies, sessionStorage y localStorage.

* SessionStorage guarda datos durante durante la sesión cuando el browser se mantenga abierto o refrescando la pagina, localStore es lo mismo pero persiste cuando el browser se cierra o se reabre. Ambas son del lado del cliente. 
* Cookies son del lado del server, guarda datos que van al server con los requests.

### ¿Cuál es la diferencia entre: function Person(){}, var person = Person() y var person = new Person()?
```javascript
function Person() {} // Declara un función pero no se ejecuta

var person = Person() // Declara una variable person, llama a la función person y le setea el retorno de la función.

var person = new Person() // Crea una nueva instacia de un objeto basado en una la función person. La variable persona es un objeto, no solo un string o number.
```

# Mencione algunas librerias de javscript
* MomentJS
* Jquery
* D3
* Sweet Alert

### ¿Por qué reciben el nombre de sentencias ternarias? ¿Qué significa la palabra "ternaria"?
Reciben este nombre porque la sentencia consta de 3 argumentos:
expresion bolean ? valor si es cierto : valor si es falso.
```javascript
var a = "test";
return (a === "test") ? "Si es test" : "No es test";
```
