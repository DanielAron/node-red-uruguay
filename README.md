# Ejercicio node-red & NLU
## Prerrequisitos
* Crear una instancia de [node-red starter de bluemix] (https://console.bluemix.net/docs/starters/Node-RED/nodered.html)
* Crear el servicio [nlu] (https://console.bluemix.net/catalog/services/natural-language-understanding)
* Conectar la aplicación de Cloud Foundury al servicio de NLU
	* node-red app
	* Connections
	* Connect exisiting
	* Natural Language Classifier


## Instalación
* Abrir el archivo node-red-flow.txt y copiar el texto
* Abrir el navegador en node-red y seleccionar import --> clipboard
![clipboard](/img/clipboard.png)

* Pegar el código y guardar (OK)
* Verificar que sea el siguiente el flow agregado:
![FLow](/img/flow.png)

## Ver
Navegar a http://[url del node red]/signup

# Nota
El NLU devuelve un array con el texto ingresado y features. En Features tenemos usage, semantic_roles, keywords, ettities, concepts, categories y warnings.

Las entities vienen en un array con los siguietnes parametros: type, text, relevance y count:
![FLow](/img/nlu.png)

Para mostrar la tabla se itera en las entidades usando mustache:
![FLow](/img/html.png)


## Referencias:
* [node-red-labs ejemplo nlu] (https://github.com/watson-developer-cloud/node-red-labs/tree/master/basic_examples/natural_language_understanding)
