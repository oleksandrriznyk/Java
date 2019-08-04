CONNECT - starts two-way communications with the requested resource. It can be used to open a tunnel.

For example, the CONNECT method can be used to access websites that use SSL (HTTPS). 
The client asks an HTTP Proxy server to tunnel the TCP connection to the desired destination.
The server then proceeds to make the connection on behalf of the client. 
Once the connection has been established by the server, 
the Proxy server continues to proxy the TCP stream to and from the client.

DELETE
GET
HEAD
OPTIONS - returns in Allows header a list of possible http methods (GET POST PUT)
PATCH - Partial PUT
POST
PUT
TRACE - performs a message loop-back test along the path to the target resource, providing a useful debugging mechanism.