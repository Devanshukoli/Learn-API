# How the Web works?

## Clients and Servers
- Any technical device that is connected to internet are to be called **client** and **servers**.
- **Client**: So Basically, a client is a user that uses internet for accessing anything in that internet world. for example, let say a website that you want to reach out. A video you want to watch or it might be anything.
- **Servers**: Servers are computer that store web-pages, many big data, applications and many more. So, when a client device wants to access the webpage or say anything related on the internet, A **COPY** of that webpage is downloaded from the server into the client machine to be displayed on the client device.

## Now, Not only clients and server are made of the part, 'how  the web works?' There are some othere things as well such as : 
- For better understanding of what I am going to explain, Just have relax and imagine something along with this line : You are sitting in your house, and there is a shop near to your hose, and you went to buy something from that shop, via road, with your bicycle or something.
    1. **Your Internet connection**: This allows you to _send_ and _receive_ data. Just like _road_ between your house and the shop.
    2. **TCP/IP**: Transmission Control Protocol and Internet Protocol are communication protocols that define how data should travel across the internet. Think of it as transport mechanism.
    3. **DNS**: Domain Name System is like _address book_ for websits. When you wriet a website name in your browser, the browser looks at the DNS to find the websit's IP address before it can retrieve the data. 
        - The Browser needs to find out which server the website lives on, so it can send HTTP messages to the right place.
        - This is like finding the address of the shop that you want to visit.
    4. **HTTP**: Hypertext Transfer Protocol is transfer protocol that defines language between clients and server to communicate. This is like how you place order or buy in the shop.
    5. **Component Files**: A website is made up of many different files, which the browser has to download and put together to display the website. These files include HTML, CSS, JavaScript, images, and video files. This is like the items you buy from the shop.

## Well, These are the parts that we just listed above, and understood little bit of how this works. But We Still do not understand how the process follow along with all this listed parts.
1. So, first browser goes to DNS server and find the Real Address of that server in which the website lives on.
2. The browser sends and HTTP request to the server, asking it to send copy of the webiste that we want to visit. Here, note that this message and all the other stuff(data) that we sent to the server using your internet connection using TCP/IP.
3. If the server accepts clients request, the server send "200 OK" message, and then send all the files of that webiste to clients machine. Like here it is~!~. And started sending files in the formate of chunks called data packets.
4. The browser in your local machine then assembles all the data packets and displays as it from the actual website.

## Ok, so this is how  things works behind the scene. But wait here the HTML, CSS, JavaScript. Are those just randomly send to client machine and browser then build those things whatever way that it wants. NO. Let see how this works.
- So, basically those are _component files_. And when client send request to server then it gives this files in response. But it also contains some **reference links** like _css_ and _javascript_. `How browser load them exactly?`.
    - So, The browser parses **HTML** first. And now that leads to finding any `<link>` or `<script>` tags in the files that points to external references.
    - Now, if browser finds nay of those above mentioned like `<link>` or `<script>` tags, then it sends request back to the server for this files.
    - Then, browser generate in-memory **DOM** tree from the parsed HTML, and **CSSOM** tree form parced CSS, and **compile and execute** the javascript code.
    - When all the listed above things are done, then the visual representations of the webiste is displayedon the screen and we are able to interact with it.

## Little about DNS.
- Well acutal web address are not that easy, they are strings of numbers that hard to memorize unlinke the 'name' of particular website. for example, the look like this : **github.com**: `192.30.255.112`.
- Now, this is called _IP Address_ and it represents _unique location_ on the web. But really it's not easy to remember this IP address. such that **DNS** was invented.

## Packets.
- In above some of the lines, we used the term called **packets**. which is form in which data is sent from server to client.
-  Basically, the data is sent in thousands of small chunks. And there are multiple reasons why data is sent in small packets like this.
- They are sometimes _dropped_ or _corrputed_ in the middle of the transmission. And if they are in small packets then it is easier to replace them, NO?
- To add more, the packets can be routed along different paths, making exchange faster and allowing many different users to download the same websites at the same time. If each webiste was sent as single big chunk, only one user could download it at a time, whihc obviously is not good.