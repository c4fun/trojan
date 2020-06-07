## Reference doc

https://amos-x.com/index.php/amos/archives/centos7-trojan/

## FAQ

1. I followed the instruction, but when I tried to start the trojan-gfw server, it says that the bind address is already in use. 
Why and how to solve?

A1: Because I use [Certbot](https://certbot.eff.org/lets-encrypt/centosrhel7-nginx) to generate the ssl certification.
By default, certbot will configure the 443 port for you, which should be used by Trojan-gfw. Hence the error

Takeaway:
The http server (nginx/httpd) will use the 80 port;
while the trojan use the 443 port. 
You can use certbot to get a free ssl certification, but you don't want it to configure 443 for you.


2. Where can the client get the cert?

A2: This cert should be the same file (usually pem) as the server.

3. What is Trojan-gfw's theory?

A3: https://github.com/johnrosen1/vpstoolbox
