### Safe Methods

As per HTTP specification, the  **GET and HEAD methods should be used only for retrieval of resource representations**  – and they do not update/delete the resource on server. Both methods are said to be considered “**safe**“.

This allows user agents to represent other methods, such as  **POST, PUT and DELETE**, in a special way, so that the user is made aware of the fact that a possibly unsafe action is being requested – and they can  **update/delete the resource on server**  and so should be used carefully.
