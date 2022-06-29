-> What happens when we access a webpage?

The CLIENT (e.g. browser) sends a request to the SERVER and the server sends a response back.
This process is called *Request-response model* or *Client-server architecture*.

1. The client makes a request to the DNS with the URL. The DNS matches the adress we type in the browser (e.g. https://www.google.com/maps) to the server's real IP address (e.g. https://216.58.211.206:443). This happens through the internet service provider. 

2. A TCP/IP socket connection is established between the server and the client. This connection is typically kept open until all the files have been transferred.

TCP: Transmission control protocol.
IP: Internet protocol.
TCP/IP: Are comunication protocols that define exactly how data travels across the web.

3. Client sends an *HTTP request*, 