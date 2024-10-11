# INSTALACION DE ZONAS PRIMARIAS

### 1- Instala o servidor BIND9 no equipo darthvader. Comproba que xa funciona coma servidor DNS caché pegando no documento de entrega a saída deste comando dig @localhost www.edu.xunta.es

**COMPROBACION DE FICHEROS DE CONFIGURACION Y ZONAS**
![Captura_checkconfig](imagenes/checkconf_checkzone.png)

**Salida ejercicio 1**
<<<<<<< HEAD

![captura1-dig](dig-xunta.edu2.png)
=======
![captura1-dig](imagenes/dig-xunta.edu2.png)
>>>>>>> 8634a01 (bind9)

### 2- Configura o servidor BIND9 para que empregue como reenviador 8.8.8.8. pegando no documento de entrega contido do ficheiro /etc/bind/named.conf.options e a saída deste comando: dig @localhost www.mecd.gob.es 

**Cambios en /etc/bind/named.conf.options**
![named.conf.options](imagenes/named.conf.options.png)

**Salida del comando del fichero**
<<<<<<< HEAD

![gov](gov.png)
=======
![gov](imagenes/gov.png)
>>>>>>> 8634a01 (bind9)

### 3- Instala unha zona primaria de resolución directa chamada "starwars.lan" e engade os seguintes rexistros de recursos (a maiores dos rexistros NS e SOA imprescindibles):

####   Tipo A: darthvader con IP 192.168.20.103
####     Tipo A: skywalker con IP 192.168.20.101
####     Tipo A: skywalker con IP 192.168.20.111
####     Tipo A: luke con IP 192.168.20.22
####     Tipo A: darthsidious con IP 192.168.20.11
####     Tipo A: yoda con IP 192.168.20.24 e 192.168.20.25
####     Tipo A: c3p0 con IP 192.168.20.26
####     Tipo CNAME palpatine a darthsidious
####     TIPO MX con prioridade 10 sobre o equipo c3po
####     TIPO TXT "lenda" con "Que a forza te acompanhe"
####     TIPO NS con darthsidious

###  Pega no documento de entrega o contido do arquivo de zona, e do arquivo /etc/bind/named.conf.local

#### NAMED.CONF.LOCAL
![named.conf.local](imagenes/named.conf.local.png)

#### ZONA DIRECTA
![db.starwars.lan](imagenes/db.starwars.lan.png)

### 4- Instala unha zona de resolución inversa que teña que ver co enderezo do equipo darthvader, e engade rexistros PTR para os rexistros tipo A do exercicio anterior. Pega no documento de entrega o contido do arquivo de zona, e do arquivo /etc/bind/named.conf.local

#### ZONA INVERSA
![db.192.168.20](imagenes/db.192.168.20.png)

### 5-     Comproba que podes resolver os distintos rexistros de recursos. Pega no documento de entrega a saída dos comandos:

#### nslookup darthvader.starwars.lan localhost
![imagen_1](imagenes/nslookup_darthvader.starwars.lan.png)

#### nslookup skywalker.starwars.lan localhost
![imagen_2](imagenes/nslookup_skywalker.starwars.lan.png)

#### nslookup starwars.lan localhost
![imagen_3](imagenes/nslookup_starwars.lan.png)

#### nslookup -q=mx starwars.lan localhost
![imagen_4](imagenes/nslookup-q=mx_starwars.lan.png)

#### nslookup -q=ns starwars.lan localhost
![imagen_5](imagenes/nslookup-q=ns_starwars.lan.png)

#### nslookup -q=soa starwars.lan localhost
![imagen:_6](imagenes/nslookup-q=soa_starwars.lan.png)

#### nslookup -q=txt lenda.starwars.lan localhost
![imagen_7](imagenes/nslookup-q=txt_lenda.starwars.lan.png)

#### nslookup 192.168.20.11 localhost
![imagen_8](imagenes/nslookup_192.168.20.11.png)






