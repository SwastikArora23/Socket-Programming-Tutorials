Welcome to a tutorial on sockets with Python 3. We have a lot to cover, so let's just jump right in. The socket library is a part of the standard library, so you already have it.

The s variable is our TCP/IP socket. The AF_INET is in reference to th family or domain, it means ipv4, as opposed to ipv6 with AF_INET6. The SOCK_STREAM means it will be a TCP socket, which is our type of socket. TCP means it will be connection-oriented, as opposed to connectionless.

Okay, so what is a socket? The socket itself is just one of the endpoints in a communication between programs on some network.

A socket will be tied to some port on some host. In general, you will have either a client or a server type of entity or program.

In the case of the server, you will bind a socket to some port on the server (localhost). In the case of a client, you will connect a socket to that server, on the same port that the server-side code is using.

For IP sockets, the address that we bind to is a tuple of the hostname and the port number.

Now that we've done that, let's listen for incoming connections. We can only handle one connection at a given time, so we want to allow for some sort of a queue, just incase we get a slight burst. If someone attempts to connect while the queue is full, they will be denied.

