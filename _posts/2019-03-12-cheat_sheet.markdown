---
layout: post
title:      "Cheat Sheet"
date:       2019-03-12 17:27:29 +0000
permalink:  cheat_sheet
---


Welcome to my cheat sheet for all things related to the Module 2 Project

**HTTP** - Hyper Text Transfer Protocal, developed by Tim Berners-Lee. A uniform way that browsers are able to parse code. Is a stateless protocol and treats each request as an independent transaction that is unable to sue info from any previous request.

**URI** - Uniform Resource Identifiers  AKA URL

**Protocal** - How we send the request 

* SMTP - EMAILS 
* HTTPS - SECURE REQUESTS 
* FTP - FILE TRANSFERS 

**DOMAIN NAME** - a string of unique characters that identifies the unique location of the web server that hosts a website.

**How the web works!**

client makes a request - request gets sent to the server via HTTP - server compiles the data and then sends back the information back to the client in an ERB view file. 

**Sinatra** is a web application framework - that support the dynamic development of dynamic websites, webb apps and web services and web resources. Sianatra is lightweight and flexible. 

**Rack** - is middleware that bridges the connection between our Ruby app and the Database 

**ERB** - Embeded Ruby 

1. Two different types of tags <%= substitution tags - display results in erb%>
2. <%scripting tag%> evaluates ruby code but does not display it

**The MVC ** Model - Views - Controller

1. The Model - provides object - oriented abstraction - asks for new data and turns it into a new instance for our class
2. View - contains the erb files which displays the information to the user 
3. Controller - Provides the main interface and application logic - what data should be shown from the request the client makes - the chef! 


**Form Basics** 

```
<form method="POST"  action="/food">
<input type= "text" name="foodname">
<input type="submit" value="submit">
</form>
```
**form method** - tells the form what kind of request should be fired to teh server when submit is clicked 
**action** is the specific route the post request should be sent to 

**cookies** - invented to store data on the client side - a hash that is stored in the browser and sent back to the server along with every subsequent request. 

**session** - an object - hash- that stores data describing a client's interaction with a webstie at a given point in time. Lives on the server. 

