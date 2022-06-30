-> What happens when we access a webpage?

The CLIENT (e.g. browser) sends a request to the SERVER and the server sends a response back.
This process is called *Request-response model* or *Client-server architecture*.

1. The client makes a request to the DNS with the URL. The DNS matches the adress we type in the browser (e.g. https://www.google.com/maps) to the server's real IP address (e.g. https://216.58.211.206:443). This happens through the internet service provider. 

2. A *TCP/IP socket connection* is established between the server and the client. This connection is typically kept open until all the files have been transferred.

TCP: Transmission control protocol.
IP: Internet protocol.
TCP/IP: Are comunication protocols that define exactly how data travels across the web.

3. Client sends an *HTTP request*. HTTP stands for Hypertext Transfer Protocol, its another comunication protocol.

HTTP Request example:
    
    GET /maps HTTP/1.1  // HTTP method + request target + HTTP version
    
    Host: www.google.com // HTTP request headers (many different possibilities)
    User-Agent: Mozilla/5.0 //
    Accept-Language: en-US //

    <BODY> // Request body (only when sending data to server, e.g. POST)

4. Server sends an *HTTP response*

    HTTP/1.1 200 OK // HTTP version + status code + status message

    Date: Fri, 18 Jan 2021 // HTTP request headers (many different possibilities)
    Content-Type: text/html //
    Transfer-Encoding: chunked //

    <BODY> // Response body (most responses)

5. The website is rendered in the browser. 
  - index.html is the first to be loaded
  - Scanned for assets: JS, CSS, images
  - Process is reapeated for each file