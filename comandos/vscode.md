https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf
 
 __<span style="color: green;">➤ VsCode  </span>__    
```sh
Archivo
  Preferencias
    -format on save  (Dale Check de Permitir (Por defecto sale desactivado) ) es para que tu texto se ordene
    -Word Wrap -> Controla como debe ejecutarse la linea (Se achican los parrafos)
    -Keyboard shortcuts

``` 
 __<span style="color: green;">➤ Ver Previews de los Markdown(.md) en VsCode </span>__
```sh
   CTRL + SHIFT + P    =  Markdown Open Preview
                          Markdown Open Preview to the side

``` 
 
 __<span style="color: green;">➤ Extensiones de VsCode  </span>__    
```sh
#Extensiones o Puglins
-Flatland Monokai Theme
-Vscode-Icons
-SPanish Languaje pack para Visual COde
-Bookmarks
-Bracket Pair Colorizer 2
-Color Highlight
-Liveserver
-Material Icon Theme
-Material Theme
-Paste JSON as Code
-TODO Highlight
-TODO Tree
``` 

 __<span style="color: green;">➤ Atajos  </span>__    
```sh
ctrl+shift+p (abre propiedades) 

#Comentar en Linux
 CTRL + SHIFT + A    (multiline /* ejemplo */ ) 
 Ctrl+K Ctrl+C - Añadir línea comentario.
 Ctrl+K Ctrl+U - Eliminar línea comentario.
 CTRL + SHIFT + 7 (Comentar en etiquetas HTML)

#Comentar en Windows
 CTRL + ALT + A     (multiline /* ejemplo */ ) 

#Como eliminar de una sola
 Ctrl + Shit + L # Seleccionar todas las ocurrencias de la selección
 Ctrl + Shift + K

#Buscar la linea ejemplo (Linea 4443)
 Ctrl + G    

#Poner las letras Mayusculas
 Ctrl + Shift + U
#Poner las letras Minusculas
 Ctrl + Shift +l
#Ocultar la barra de SideBar
 Ctrl + B
  
#Selecionar un archivo especifico
 Ctrl + P
    
#Deshacer y rehacer el código
 Ctrl +Z
 Ctrl + Shift + Z

#Cerrar tab
 Ctrl + W       
#Cerrar todas las ventanas de trabajo
 Ctrl + K  Ctrl + W 

#Reabrir anterior ventana
 Ctrl + Shift + T   

#Cambiar de ventana
 Ctrl + TAB        

#Usar
 Ctrl + Shift + flechas.arriba o flechas.abajo
 Ctrl + Shift + flechas.a.los.costados
 Alt + flechas.arriba o flechas.abajo
 
#Buscar una palabra
 CTRL + SHIFT + F #seleccionas primero la palabra para que apretes ese comando)

#Remplazar una palabra de la clase y que afecte a todo lo que utilize con el
 F2     #seleccionas primero la palabra para que apretes ese comando y luego replanzas
 
``` 

__<span style="color: green;">➤ Crear Snippets  </span>__   
```sh
 #Crear Snippets (Sirve para completar automaticamentes o construya comando rapidos)
   Ir a preferences  > User Snippets > Elige el lenguaje de programacion para poder crear un comando por defecto para eso
    "Mostrar Consola":{
   "prefix": "cls",
   "body": [
     "console.log('Ok');"
   ],
   "description": "Mostrar un console.log en VsCode..."
  }
  
	// "Print to console": {
	// 	"prefix": "log",
	// 	"body": [
	// 		"console.log('$1');",
	// 		"$2"
	// 	],
	// 	"description": "Log output to console"
	// }
 
 	"Generar Clase":	{
		"prefix": "clase",
		"body": [
							"export class ${1:NombreClase} {",
							"",
							"   constructor() { ",
							"          $2",
							"     }",
							"}"
		],
		"description": "Creando Clase automaticamente"
	}
 
``` 

#### Building for source
For production release:
```sh
$ gulp build --prod
```
