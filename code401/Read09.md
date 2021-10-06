# ***WRRC and Java***

## ***The HTTP Request Lifecycle***

![IMG](https://www.cdnfinder.com/wp-content/uploads/2018/12/HTTP-Request-and-Response-Over-Web-1.png)


*HyperText Transfer Protocol The communications protocol used to connect to Web servers on the Internet or on a local network (intranet). The primary function of HTTP is to establish a connection with the server and send HTML pages back to the user's browser. It is also used to download data from the server either to the browser or to any requesting application that uses HTTP.*

* *The HTTP Request Lifecycle*

    * Step 1: Local Processing

       *browser extracts the `"scheme"/protocol` (we have established
        that this will be HTTP), host (www.example.com),
        and optional port number, resource path, and query strings that are specified in the form*

        ```
        <protocol>://<host><:optional port>/<path/to/resource><?query>` . An example is `|http|://|www.example.com||:5000||/mainpage||?query=param&query2=param2|
        ```

        *then that the browser has the intended hostname for the request, it needs to resolve an IP address1. The browser will then look through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache.*

    * Step 2: Resolve an IP

        *If the cache lookup fails the browser will fire off DNS request by UDP .*
        *Whenever the packet hits a piece of networking equipment, the device uses a routing table to determine which other device it is connected to that is most likely situated along the shortest path to the destination.*
        *Once your request arrives at your configured DNS server, the server looks for the address associated with the requested hostname.*

    * Step 3: Establish a TCP Connection

        *Before the server can accept a three-way handshake, the client must first create a TCP connection. The server must be listening on a port and executing a passive open, after which the client can conduct an active open and the client-server connection will be recognized. This allows the receiver to restore the original order of received packets and the sender to restore the original order of sent packets.*


    * Step 4: Send an HTTP Request

        *Use the HTTP Request Step to perform a single HTTP(S) request. After successful execution this Step will create the following Variables: Body, Headers, StatusCode, ResponseTime, ReasonPhrase. This Step supports Verifications to make sure the HTTP Response is the same as the expected.*

    
    * Step 5: Tearing Down and Cleaning Up
    
        *After receiving the response, the client sends a TCP FIN packet, to which the server answers with an ACK, and then sends its own FIN, to which the client responds with its own ACK signal. Then there will be a timeout. The four-way handshake is what it's called. The browser begins to process the information it has received and then exits.*



## ***Java HTTP Request example***

![IMG](https://1.bp.blogspot.com/-nb4AD94YiMs/XOu82c2kCKI/AAAAAAAAGBU/BgaOEOGT8HANzbnjJ8r4S46p6IliOROqACEwYBhgL/w1200-h630-p-k-no-nu/okhttp-get.PNG)



1. **Overview**

*way of performing HTTP requests in Java*

2. **HttpUrlConnection**

*is aclass allows us to perform basic HTTP requests without the use of any additional libraries , is part of the `java.net` package.*

3. **Creating a Request**

 *creates a connection object by create an HttpUrlConnection instance using the openConnection() method of the URL class*

* example:
```
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
```

4. **Adding Request Parameters**

*we have to set the doOutput property to true, then write a String of the form*

5. **Setting Request Headers**

*can be achieved by using the setRequestProperty() method*

6. **Configuring Timeouts**

7. **Handling Cookies**

8. **Handling Redirects**

9. **Reading the Response**

10. **Reading the Response on Failed Requests**

11. **Building the Full Response**


