This folder contains the JSON Schemas that will be used to validate the requests. They need to describe an
object and its properties. We should be able to validate against the request object attribute that contains the
parameters (normally request.params , but potentially something else, such as request.body ).

Due to the type of attributes we defined for our endpoints, there is really only one endpoint that we
would want to validate: the getBookSales (GET /booksales ) endpoint. It receives two date parameters, and
we probably want to validate their format to be 100% certain that the dates are valid.

Again, to provide the simplicity of usage that “convention over configuration” provides, our schema files
must follow a very specific format, which is then used by the validator that we saw earlier:

/request_schemas/[CONTROLLER NAME].js

module.exports = {
    
    [ENDPOINT NICKNAME] : {
        
            validate : [TYPE ],
            
            schema : [JSON SCHEMA]
            
        }
        
    }
    

There are several pieces that need to be explained in the preceding code:
- CONTROLLER NAME: This means that the file for the schema needs to have the
same name as the controller, all lowercase. And since we already did that for our
controllers’ files, this mean the schemas for each controller will have to have the
same name as each controller’s file.
- ENDPOINT NICKNAME: This should be the nickname given to the action when
adding it to the controller (using the addAction method).
- TYPE: The type of object to validate. The only value supported right now is params ,
which references the query and path parameters received. This could be extended to
support other objects.
- JSON SCHEMA: This is where we add the actual JSON Schema defining the request
parameters.

Here is the actual code defining the validation for the getBookSales action.
