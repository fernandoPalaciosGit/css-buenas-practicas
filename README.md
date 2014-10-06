### ACCESIBILIDAD
todos los dispositivos, independientes de la plataforma, reconocen y compilan por igual el HTML.

La accesibilidad máxima (acceso a la informacion y contenido por gual sin depender de ninguna discapcidad del usuario), se alcanza solo con un HTML semantico.

### USABIILIDAD
El cliente , ya sea empresa o particulares (ofreciendo servicio), SIEMPRE exigen un cierto grado dde usabilidad en la web, dependiendo de sus necesidades y objetivos .
Esto se consigue a traves del estudio de la Experiencia de usuario (UX) y el diseño de Interfaces (IX). Se basa en hacer un estudio de la gente que va a encontrar y navegar por nuestra web y hacer target de sus necesidades.

La usabilidad y diseño de la web se consigue con estilios de CSS y programacion de scripting en el cliente.

### SOPORTE DE COMPATIBILIDADES
- Can I Use (chequear compatibilidad de css)
- Fallbacks de Javascript
- Fallback de CSS
- Modernizer

### PROGRESSIVE ENHANCEMENT
HTML semantico (contenido) + CSS (presentacion) + JAVASCRIPT (interacion)

De esta manera, se diseña y programa la web por caas bien defiidas y sea la que fuere que fallase, siempre tendremos la capa de contenido que siemlpre se mostrará

### INVENTARIO DE CONTENIDO
listado de todos los elemeentos que forman el contenido de una web
titulos, call to action, formularios, banners...

### SITE MAP
navegacion a traves de las vistas de nuesttra web

### COMPATIBILIDAD DE RESOLUCIONES DE PANTALLAS
 - trabajar en TODAS las resoluciones, una vez que tengamos el contenido inicial (partiendo de movil o de desktop), modularizar la pantalla para que se valla viendo ordenado y segun los estilos del diseño web el contenido adecuiado a esa resolucion.

 - cuando que remos apuntar a dispositivos de manera especifica estudiamos la mediaquiery para este en particular

### BREAKPOINTS === RESOLUCIONES CON MEDIA QUERYS

### DISPOSITIVOS DE PANTALLA CON RETINA DISPLAY o DOPLBLE DESSIDAD DE PIXELES
se crea un breakpoint de media query para estos tipos de pantalla y se sirve una imagen de mayor resolucion.

### MOBILIE FIRST
la maquetacion de contenido y diseño primero debe estar penssada para mobiles y despues ir escalando para PCs

UN SOLO CALL TO ACTION POR .WEB
se atrae mas a la gente con una sola interaccion, hay que estudiar cual es la motivacion principal de la web

### PATRONES DE DISEÑO
- Mobile First: diseñar primero para dispositivos mobiles o de menor a mayor resolucion
- Progressive Enhancement: primero contenido html, despues estilos css, y finalmente interaccion Javascript

### La imagen SIEMPRE debe vender el producto
por muy bonita que sea una fotografia y representtiva de nuestro gremio, solo hay una manera de decantarse por ella.
- resumir en una frase el objetivo de la web y queres que esa imagen VENDA ese concepto
- la imagen no debe ser tapada por ningun elemento

### ANALISIS DE LA WEB

###### 1 - Contenido
		- descripcion de la web: motivacion, target de clientes, inversion
		- inventario o sabana de contenido : elementos de la web y su contenido

###### 2 - distribucion, planeamiento y diseño de contenido
		-mockups, borradores, prototipos, maketas

###### 3 - diseño
		- fotografias, tipografias
		- diseño e interaccion de interfaces (mockups borradores)

###### 4 - maquetacion y programacion 
		- contenido web: html semantico
		- maquetacion web: css
		- programacion web: cliente y servidor
	
###### 5 - pruebas y vuelta a empezar

### MAQUETACION MOBILE FIRST
siempre empezar a maquetar (css) desde las resoluciones mas bajas
En un mobil (fisico) la resolucion de pantalla (la calidad visual de estilos) es mejor que la que ofrece una pantalla de PC


### OPTIMIZACION DE NAVEGADORES
- SERVIDOR
	- reducir la cantdad de peticiones de la web
	- por cada peticion (recurso) a la web requiere unos cuantos tiempos de espera (busqueda de fichero, credenciales, encapsular y cargar el contenido...).

- MANIPULAR RECURSOS
	- minimizar el peso de cada archivo (si es uno solo, mejor)
	- comprimir los archivos a uno solo, tanto de scripting, estilos y html. Se pueden usar Herramientas web, Prepros o Codekit).

- IMAGENES
	- utilizar varias versiones de una imagen en el formato que se vaya a mostrar
	- usar imagenes en formato de sprites cuando se puedan reutilizar.
	- utilizar una libreria de iconos en vez de imagenes
	- usar `icomoon` o `flaticon` en vez de una libreria de iconos como `fontAwesom`, Porque especificamos solo loa icoos de nuestra  alpcicacion

- CDN
	- para cargar librerias externas o imagenes
	- los recursos cargan mas rapidos que en tu servidor
	- reduces la cantidad de peticiones limitadas a tu sevidor de produccion (por lo general son 10 peticionesmaximas por servidor a la vez)

- CARGA DE PROCESOS
	- cuidar el tiempo de carga de Javascript, imagenes y estilos > RECURSOS DEL DEBUGGER
	- controlar la carga de los scripts de la web > TIMELINE DE DEBUGGER
	- fijarse que los FPS de renderizado de la pagina sea lo mas proximo posible a 60FPS que se traduciria en un a latencia optima, si el render de los FPS en MENOR, significa que le cuesta mas cargar la pagina. > SHOW FPS METER DEL DEBUGGER

- FALLBACKS
	- En animaciones con CSS utilizar `transition: translate-x()` en vez de `top - left`
	- usar los pseudoelementos de css para complementar el contenido de html que NO sea semantio ( . ; , * - ...)
	- limitar las fuentes tipograficas a 2
	- Cuando se vayan a cargar fuentes externar o por CDN, usar solo la codificacion de caracteres especifica y limitar la fuente a la tipografia especifica.
	- reducir las peticiones al servidor externo con su API REST
		https://developers.google.com/fonts/docs/getting_started#Syntax 

- FALLBACKS DE SCRIPTING
	- Cargar cierto contenido en cache del navegador del cliente
	- La cache importante es la quese especifica en el servidor, desde los archivos de HT-ACCESS, definimos los archivos que se cargan en cache de la maquina del servildor, la proxima vez que haga esa misma peticion, el servidor NO perdera tiempo en buscar recursos.


### GUIAS DE ESTILOS
- ANATOMIA DEL DOCUMENTO
		- utilizar `preprocesadores` y visualizacion ordenada de los documentos
		- `sectorizar` los css en varios archivos dependiendo de: 
				- layouts de responsive
				- utilidad semantica de elementos
				- mixins, parches y fallbacks reutilizables
				- elementos base de estilos
				- componentes reutilizables
				- librerias de terceros
		- `minificar` todos los archivos en uno solo, que se contenga exclusivamente @includes.
		- `comprimir` el archivo compilado anterior en pocas lineas.
		- `tabla de contenidos` en el archivo de @incluedes, detalla los diferentes archivos de estilos.
		Cada entrada en la tabla de contenidos marca el titulo del @include

		//////////////////////////////////////////////////////////////////////
		// $MAIN..................Import all our stylesheets                //
		// $NORMALIZE.............Reset all web browser default styles      //
		// $FONTS.................Import icon fonts and font face           //
		// $MIXINS................Reusable code by functions                //
		// $RESET.................Default styles on our website             //
		// $MOBILE................Landing page styles, mobile first         //
		// $CLASS-GAME-PROYECTS...Especific styles for articles of proyects //
		// $MIN-WIDTH-680.........Layout for higher styles than 680 pixels  //
		// $MIN-WIDTH-1024........Layout for higher styles than 1024 pixels //
		//////////////////////////////////////////////////////////////////////

		- `titulo de secciones`

		/////////////////////
		// $MIN-WIDTH-1024 //
		/////////////////////


### ESTRUCTURA DE ARCHIVOS
		- app/css
				main.css

		- app/scss/styles
				_main.scss	// tabla de contenidos + @includes

		- app/scss/styles/base
				_reset.scss
				_fonts.scss
				_mixins.scss

		- app/scss/styles/layout
				_mobile.scss
				_min-width-680.scss
				_max-width-1024.scss

		- app/scss/styles/components
				_class-nav-header.scss
				_modal-view.scss
				_buttons

		- app/scss/styles/vendors
				_normalize.scss


### REGLAS DE SELECTORES
- cada bloque de estilos identarlos con doble tab (parecido a la estructura del DOM)
- UN guion simples para delimitar los nombres de clase
- nombre de clases en un elemento del DOM separadas con DOS espacios
- DOS guiones dobles para delimitar el modificador de esa clase
- DOS guiones bajos para delimitar el descendiente del DOM de esa clase
	
	.my-block{ // representa un `nivel de abstraccion` especifico }
	.my-block__elemento{ // representa un `descendiente del DOM` }
	.my-block--modificador{ // representa un `estado diferente del elemento` }

```css
	
	comment-widget{ } // nivel de abstraccion: ¿Que es el elemento para la web?
	pokemon-widget{ }

			pokemon-widget--slide{ }	// estado del elemento: ¿Como se comporta el elemento en esta situacion?
			pokemon-widget--alert{ }

			pokemon-widget__list-top10{}		// contenido del elemento 

```


### TECNICAS DE MAQUETACION

###### maquetar toda la web a `una sola columna`
			- es mas facil de leer todo el contenido
			- en resoluciones de moviles, SOLO SE LEE A UNA COLUMNA

###### cada componente se debe comportar como un widget, `el css de un widget debe ser generico`
	```css
		<section class="fbm-news">
			<aside class="fbm-news--banner">

				<!-- ESTO ES UN WIDGET, trocito de html que se puede reutilizar -->
				<div class="banner--news"> 
					<h4 class="banner--news__title"></h4>
					<input class="banner--news__search" type="text">
					<input class="banner--news__send" type="submit">
				</div>

			</aside>
		</section>
	```

###### JS HOOKS
	```css
		<table class="nba-masters">
			<thead class="nba-master--header js-nba-master--header">
				<th></th>
			</thead>
		</table>
	```

###### SELECORES CUASI CALIFICADOS
Para comunicar a los desarrolladores donde queremos utilizar esa clase

	```css
		/*table*/.news-letter--header{ }
		/*p*/.intro{ }
		/*figure ul*/.img-thumbs{ }
	```

###### OOCSS -> orientacion a objetos en CSS
Se trata de abstraer las clasess como elementos heredados, con una jerarquia logica del contexto de esa clse
	
	```css
		.living-room
				.living-room--table
				.living-room--shelf
				.living-room--
	```

Entonces tenemos dos reglas de seleccion de clases a traves del shorcut `--`

`componentes` heredados de jerarquias (OOCSS) -> cuando los elementos son de caracter real

		```css
			.person-man
					.person-man--skirt
					.person--woman--skirt
		```


`comportamiento` del elemento de la clase -> cuando los elementos son de caracter intangibles

	```css
		/*inpu[type="button"]*/.user-action{ }
				.user-action--alert
				.user-action--trade
				.user-action--alert
	```

###### SISTEMA DE GRILLAS o LAYOUT
- nunca utilizar **anchos** ni **altos** en los elementos **contenedores** de nustro sistema de grillas.
- nuestro **layout debe ser fluido**, nunca hay que aplicarles dimensiones explicitas (px, em, vm, rem). 
- El sistema de grids debe, idealmente, estar dado en porcentajes.

###### TAMAÑOS DE FUNTE
Los tamaños de fuentes deben darse en rems con fallback en pixels. Así se aprovechan los beneficios de accesibilidad de los rems con la robustez de los pixels.

	```css
		$BASEFONT: 16;
		@mixin font-size( $font-size: 16 ) {
			font-size: ($font-size)*1px;
			font-size: ($font-size/$BASEFONT)*1rem;
		}
		html{
			@include font-size($BASEFONT);
		}
		body{
			font-size: 100%;
		}
		.img-random--thumb{
			@include font-size(10);
		}
	```

###### ANIDACION EN PREPROCESADORES
######### MAL
	
	```css
		.header{
			.site-nav{
				li{
					a{ }
				}
			}
		}
	```

######### BIEN

	```css
		.header{}
		.site-nav{
			li{ }
			a{ }
		}
	```