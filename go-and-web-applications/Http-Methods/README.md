# Request methods
The request method is the first word on the request-line and indicates the action to be done on the resource. HTTP 0.9 had only one method: GET. HTTP 1.0 added POST and HEAD. HTTP 1.1 added another five—PUT, DELETE, OPTIONS, TRACE, and CON- NECT—and opened the possibility for adding more methods (and many promptly did).
Interestingly, HTTP 1.1 specifies that GET and HEAD must always be implemented while all other methods are optional (this means even POST is optional).

■ GET—Tells the server to return the specified resource.

■ HEAD—The same as GET except that the server must not return a message
body. This method is often used to get the response headers without carrying
the weight of the rest of the message body over the network.

■ POST—Tells the server that the data in the message body should be passed to the resource identified by the URI. What the server does with the message body
is up to the server.

■ PUT—Tells the server that the data in the message body should be the resource
at the given URI. If data already exists at the resource identified by the URI, that data is replaced. Otherwise, a new resource is created at the place where the URI is.

■ DELETE—Tells the server to remove the resource identified by the URI.

■ TRACE—Tells the server to return the request. This way, the client can see what
the intermediate servers did to the request.

■ OPTIONS—Tells the server to return a list of HTTP methods that the server sup-
ports.

■ CONNECT—Tells the server to set up a network connection with the client. This
method is used mostly for setting up SSL tunneling (to enable HTTPS).

■ PATCH—Tells the server that the data in the message body modifies the
resource identified by the URI.