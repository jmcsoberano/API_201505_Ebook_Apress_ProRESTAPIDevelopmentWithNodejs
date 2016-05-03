#Aqui las carpetas que vamos creando y usando

## controllers 
This folder contains the code for our controllers. It also has an index.js
file to handle exporting the contents of the rest of them. There is also a base
controller here, which contains all the generic methods that all controllers should
have; so every new controller can extend this and inherit said methods.

Esta carpeta contiene el código para nuestros controladores. También tiene una index.js
archivo para manejar la exportación de los contenidos del resto de ellos. También hay una base de
controlador de aquí, que contiene todos los métodos genéricos que todos los controladores deben
tener; por lo que cada nuevo controlador puede extender este y heredar dichos métodos.

## lib 
This folder contains the miscellaneous code not big enough to have its own
folder, but required across several different places in our project; for instance,
database access, helper functions, the config files, and so forth.

Esta carpeta contiene el código de varios no lo suficientemente grande como para tener su propio
carpeta, pero requiere la mayoría de lugares diferentes en nuestro proyecto; por ejemplo,
Acceso a la base de datos, funciones de ayuda, los archivos de configuración, y así sucesivamente.

## models
Inside this folder are the model files. Normally when working with
Mongoose, a model’s file has the schema definition, and you return the instantiation
of that schema as your model. In our case, the actual definition is somewhere else, so
this code handles loading that external definition, adding the extra behavior specific
to each model, and then returning it.

Dentro de esta carpeta están los archivos de modelo. Normalmente cuando se trabaja con
Mongoose, el archivo de un modelo tiene la definición de esquema, y se vuelve la creación de instancias
de ese esquema como su modelo. En nuestro caso, la definición real está en otra parte, por lo
Este código controla la carga de esa definición externa, añadiendo el comportamiento adicional específica
para cada modelo y, a continuación, devolverlo.

## request_schemas
Inside this folder are the JSON Schemas used to validate the
different requests.

Dentro de esta carpeta son los esquemas JSON utiliza para validar la
diferentes peticiones.

## schemas 
These are the JSON Schemas of the models, used for the Swagger module
to define the UI for testing and for the Mongoose model’s definition. We will have to
add some code to translate from the first one to the latter, since they don’t use the
same format.

Estos son los JSON esquemas de los modelos, que se utiliza para el módulo Swagger
para definir la interfaz de usuario para la prueba y para la definición del modelo de Mongoose. Tendremos que
añadir algo de código para traducir de la primera a la última, ya que no utilizan el
mismo formato.

## swagger-ui
This folder contains the contents of the Swagger UI project. We’ll
need to do some minor adjustments to the index.html file to make it work as we
expect it.

Esta carpeta contiene los contenidos del proyecto Swagger interfaz de usuario. Bien
que tenga que hacer algunos ajustes menores en el archivo index.html para que funcione como esperamos.
