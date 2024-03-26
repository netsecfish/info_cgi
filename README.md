# Exposure of Sensitive Information through Unauthenticated CGI Script Access on D-Link DNS Series

## **Vulnerability Summary**

A vulnerability has been identified in the D-Link DNS series network storage devices, allowing for the exposure of sensitive device information to unauthorized actors. This vulnerability is due to an unauthenticated access flaw in the **`info.cgi`** script, which can be exploited via a simple HTTP GET request, affecting over 920,000 devices on the Internet.

![Untitled](DLINK%20DNS-320%20c1cb5ec7d1e24daf9eef6f423759b36d/Untitled%201.png)

## **Affected Models**

- DNS-327L Version=1.00.0409.2013
- DNS-320L Version=1.02.0329.2013 and Version=1.01.0914.2012
- DNS-320LW Version=1.01.0914.2012

## Exploitation

Launch an HTTP GET request to the target device: http://127.0.0.1/cgi-bin/info.cgi

## Reproduction Details

Several cases on the Internet were randomly selected: 

 [http://175.137.133.113](http://175.137.133.113/)

 [http://114.43.213.53/](http://114.43.213.53/)

[http://89.251.47.20:84/](http://89.251.47.20:84/)

[http://93.191.42.136:8080](http://93.191.42.136:8080/)

[http://89.251.47.20:84](http://89.251.47.20:84/)

[http://91.114.143.193:888](http://91.114.143.193:888/)

## Actual Result

![Untitled](DLINK%20DNS-320%20c1cb5ec7d1e24daf9eef6f423759b36d/Untitled%202.png)

![Untitled](DLINK%20DNS-320%20c1cb5ec7d1e24daf9eef6f423759b36d/Untitled%203.png)

![Untitled](DLINK%20DNS-320%20c1cb5ec7d1e24daf9eef6f423759b36d/Untitled%204.png)

![Untitled](DLINK%20DNS-320%20c1cb5ec7d1e24daf9eef6f423759b36d/Untitled%205.png)

![Untitled](DLINK%20DNS-320%20c1cb5ec7d1e24daf9eef6f423759b36d/Untitled%206.png)

![Untitled](DLINK%20DNS-320%20c1cb5ec7d1e24daf9eef6f423759b36d/Untitled%207.png)

## Fix Recommendation

It is recommended to restrict access to the administrative interfaces of the device to trusted IP addresses only and apply network-level authentication.
