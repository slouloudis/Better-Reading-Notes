
Server Side - Rendering. 

Some terminology. 

Pre-rendering : React sends over a bunch of javascript to the client for it to be rendered -> Next, on the other-hand, only sends the client code that is necessary for the page (competent *hydration*), and everything else is run on the server. 

Two forms of Pre-rendering. S
Static Generation - Static site generation - the HTML is generated at build time, and will be reused on each request. 
Server-side Rendering - The HTML is generated on each request (not recommend)

CDN - How does a CDN work? 
	A content delivery network is a network of servers linked together with the goal of delivering content as quickly, cheaply, reliable and securely as possible. In order to improve speed and connectivity, a CDN will place servers at the exchange points between different networks. 