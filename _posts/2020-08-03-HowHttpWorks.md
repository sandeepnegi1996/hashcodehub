---
layout: post
title: How HTTP Works!
---

# How Internet Works:

1. URL Building :- When we type in the browser **hashcodehub.com** the browser will prepend HTTP:// 
2. DNS Lookup : Out browser now has the domain name but this is not the the way things communicate and identify over internet
   for that we need if address of the server that is hosting our files, 
    1. DNS Local Cache :- it the domain is already resolved it will in the DNS Local cache of the browser.
    2. DNS Resolver :- If the host is not in the DNS local Cache the browser will use the DNS resolver using gethostbyname POSIX systemcall
    3. Host File :- gethostbyname will first look in the host file stored in our system, if still we are not able to resolve the domain name 
    4. DNS Server :-the system makes a request to the DNS server such as Google DNS server 8.8.8.8 ,The DNS Server might have the 
                   1. domain IP in the cache If not it will give the ip of Top-level DNS resolver. like .com,.in,.org


3. TCP request handshaking :- After finding the ip adress of the domain name then we make a TCP request handshaking.
4. SEnding the Request :-  it has 3 parts
                           1. the request line 
                           2. the request header
                           3. the request body


5. The Request line is having the method name ,resource location and protocol veriosn:- 
   1. Ex :- GET / HTTP/1.1
   
6. The Request Header:- it will have field:value in pairs.
   1. There are two mandatory fields 
   2. host and connection

7. Request Body :- it will be used in case of post request to send data.
8. The Response :- once the request is send and server processed the request it sends back the response 
                    1. It contains status code and message
                    2. 200 OK
9. Now browser will receive the pages and start rendering it, this process will be repeated for each request.