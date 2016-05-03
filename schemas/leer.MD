This folder contains the JSON Schema definitions of our resources, which also translate into the Mongoose
Schemas when initializing our models.

The level of detail provided in these files is very important, because it also translates into the actual
Mongoose model. This means that we could define things such as ranges of values and format patterns,
which would be validated by Mongoose when creating the new resources.

For instance, let’s take a look at ClientReview, a schema that makes use of such capability.

Esta carpeta contiene las definiciones de esquema JSON de nuestros recursos, que también se traducen en la Mongoose
Los esquemas en la inicialización de nuestros modelos.

El nivel de detalle de estos archivos es muy importante, ya que también se traduce en el actual
modelo de la mangosta. Esto significa que podríamos definir cosas como intervalos de valores y patrones de formato,
los cuales serían validados por Mongoose al crear los nuevos recursos.

Por ejemplo, vamos a echar un vistazo a ClientReview, un esquema que hace uso de esa capacidad.
