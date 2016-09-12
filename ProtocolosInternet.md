# PRINCIPALES PROTOCOLOS DE INTERNET

------------------------------------

La familia de protocolos de Internet es un conjunto de protocolos de red en la que se basa Internet y que permiten la transmisión de datos entre redes de computadoras. En ocasiones se le denomina conjunto de protocolos TCP/IP, en referencia a los dos protocolos más importantes que la componen: Protocolo de Control de Transmisión (TCP) y Protocolo de Internet (IP), que fueron los dos primeros en definirse, y que son los más utilizados de la familia. 
![alt text][imagen]

[imagen]: http://disenowebakus.net/imagenes/articulos/historia-de-internet.jpg "The Web"

Existen tantos protocolos en este conjunto que llegan a ser más de 100 diferentes, entre ellos se destacan los siguientes:

TCP (Transmission Control Protocol)
-
Este protocolo garantiza que los datos serán entregados en su destino sin errores y en el mismo orden en que se transmitieron. También proporciona un mecanismo para distinguir distintas aplicaciones dentro de una misma máquina, a través del concepto de puerto. En el nivel de aplicación, posibilita la administración de datos que vienen del nivel más bajo del modelo, o van hacia él, (es decir, el protocolo IP). Cuando se proporcionan los datos al protocolo IP, los agrupa en datagramas IP, fijando el campo del protocolo en 6 (para que sepa con anticipación que el protocolo es TCP). Como es un protocolo orientado a conexión permite que dos máquinas que están comunicadas controlen el estado de la transmisión. Las principales características del protocolo TCP son las siguientes:

* Da soporte a muchas de las aplicaciones más populares de Internet, incluidas HTTP, SMTP, SSH y FTP. 
* Permite colocar los datagramas nuevamente en orden cuando vienen del protocolo IP.

TCP multiplexa aplicaciones dentro de una máquina IP. Para cada máquina de IP, TCP soporta (multiplexa) hasta 65.536 puertos (o enchufes), desde el número puerto entre 0 y 65535. Aplicaciones, tales como HTTP o FTP, se ejecutan (o escuchan) en un número determinado de puerto para las solicitudes entrantes. Del puerto 0 a 1023 son pre-asignados a los protocolos populares, el puerto 1024 y superiores están a disposición de los usuarios.

IP (Internet Protocol)
--
El Protocolo de Internet es un protocolo no orientado a conexión usado tanto por el origen como por el destino para la comunicación de datos a través de una red de paquetes conmutados. Los datos en una red basada en IP son enviados en bloques conocidos como paquetes o datagramas. En particular, en IP no se necesita ninguna configuración antes de que un equipo intente enviar paquetes a otro con el que no se había comunicado antes.

El Protocolo de Internet provee un servicio de datagramas no fiable. IP no provee ningún mecanismo para determinar si un paquete alcanza o no su destino y únicamente proporciona seguridad de sus cabeceras y no de los datos transmitidos. Por ejemplo, al no garantizar nada sobre la recepción del paquete, éste podría llegar dañado, en otro orden con respecto a otros paquetes, duplicado o simplemente no llegar. Si se necesita fiabilidad, ésta es proporcionada por los protocolos de la capa de transporte, como TCP. Si la información a transmitir (datagramas) supera el tamaño máximo "negociado" (MTU) en el tramo de red por el que va a circular podrá ser dividida en paquetes más pequeños, y reensamblada luego cuando sea necesario. Estos fragmentos podrán ir cada uno por un camino diferente dependiendo de cómo estén congestionadas las rutas en cada momento. Las cabeceras IP contienen las direcciones de las máquinas de origen y destino (direcciones IP), direcciones que serán usadas por los conmutadores de paquetes (switches) y los enrutadores (routers) para decidir el tramo de red por el que reenviarán los paquetes.

En la siguiente imágen se muestra la forma en que se estructuran algunos de los protocolos que pertenecen al conjunto TCP/IP.

![alt text][imagen2]

[imagen2]: http://4.bp.blogspot.com/-yWHalfLXTH4/Vj-f70p9m3I/AAAAAAAAFQ8/ZsBS3Nl8ETA/s1600/img1016.gif "Diagrama"

UDP (User Datagram Protocol)
--

UDP es un protocolo del nivel de transporte basado en el intercambio de datagramas (Encapsulado de capa 4 Modelo OSI). Permite el envío de datagramas a través de la red sin que se haya establecido previamente una conexión, ya que el propio datagrama incorpora suficiente información de direccionamiento en su cabecera. Tampoco tiene confirmación ni control de flujo, por lo que los paquetes pueden adelantarse unos a otros; y tampoco se sabe si ha llegado correctamente, ya que no hay confirmación de entrega o recepción. Su uso principal es para protocolos como DHCP, BOOTP, DNS y demás protocolos en los que el intercambio de paquetes de la conexión/desconexión son mayores, o no son rentables con respecto a la información transmitida, así como para la transmisión de audio y vídeo en real, donde no es posible realizar retransmisiones por los estrictos requisitos de retardo que se tiene en estos casos.

UDP utiliza puertos para permitir la comunicación entre aplicaciones. El campo de puerto tiene una longitud de 16 bits, por lo que el rango de valores válidos va de 0 a 65.535. El puerto 0 está reservado, pero es un valor permitido como puerto origen si el proceso emisor no espera recibir mensajes como respuesta.

HTTP (HyperText Transfer Protocol)
--
**Opera en el puerto 80.**

Desde 1990, el protocolo HTTP es el protocolo más utilizado en Internet. Es el protocolo usado en cada transacción de la Web (WWW). La versión 0.9 sólo tenía la finalidad de transferir los datos a través de Internet (en particular páginas Web escritas en HTML). La versión 1.0 del protocolo (la más utilizada) permite la transferencia de mensajes con encabezados que describen el contenido de los mensajes mediante la codificación MIME. El propósito del protocolo HTTP es permitir la transferencia de archivos (principalmente, en formato HTML) entre un navegador (el cliente) y un servidor web (denominado, entre otros, httpd en equipos UNIX). HTTP define la sintaxis y la semántica que utilizan los elementos software de la arquitectura web (clientes, servidores, proxies) para comunicarse. 
Es un protocolo orientado a transacciones y sigue el esquema petición- respuesta entre un cliente y un servidor. Al cliente que efectúa la petición (un navegador o un spider) se lo conoce como "user agent" (agente del usuario). A la información transmitida se la llama recurso y se la identifica mediante una cadena de caracteres denominada dirección URL. Los recursos pueden ser archivos, el resultado de la ejecución de un programa, una consulta a una basede datos, la traducción automática de un documento, etc.

FTP (File Transfer Protocol)
--
**Opera en el puerto 21.**

Creado en 1971, el protocolo FTP (Protocolo de transferencia de archivos) es, como su nombre lo indica, un protocolo para transferir archivos. Este protocolo define la manera en que los datos deben ser transferidos a través de una red TCP/IP. El objetivo del protocolo FTP es:

* Permitir que equipos remotos puedan compartir archivos.
* Permitir la independencia entre los sistemas de archivo del equipo del cliente y del equipo del servidor.
* Permitir una transferencia de datos eficaz.

SMTP (Simple Mail Transfer Protocol)
--
**Opera en el puerto 25.**

Creado en 1971, el protocolo SMTP (Protocolo simple de transferencia de correo) es un protocolo de la capa de aplicación. Es un protocolo de red basado en texto utilizado para el intercambio de mensajes de correo electrónico entre computadoras u otros dispositivos (PDA's, teléfonos móviles, etc.). Está definido en el RFC 2821 y es un estándar oficial de Internet que realiza la transferencia de correo de un servidor a otro mediante una conexión punto a punto.
 
SMTP se basa en el modelo cliente-servidor, donde un cliente envía un mensaje a uno o varios receptores. La comunicación entre el cliente y el servidor consiste enteramente en líneas de texto compuestas por caracteres ASCII. El tamaño máximo permitido para estas líneas es de 1000 caracteres. Las respuestas del servidor constan de un código numérico de tres dígitos, seguido de un texto explicativo. El número va dirigido a un procesado automático de la respuesta por autómata, mientras que el texto permite que un humano interprete la respuesta. En el protocolo SMTP todas las órdenes, réplicas o datos son líneas de texto, delimitadas por el carácter <CRLF>. Todas las réplicas tienen un código numérico al comienzo de la línea.

TFTP (Protocol File Trivial Transfer)
--
**Opera en el puerto 69.**

La transferencia de ficheros TCP/IP es una transferencia de datos disco a disco. TFTP es un protocolo extremadamente simple para transferir ficheros. Está implementado sobre UDP y carece de la mayoría de las características de FTP. La única cosa que puede hacer es leer/escribir un fichero de/a un servidor.
No tiene medios para autentificar usuarios: es un protocolo inseguro.
 
 IMAP (Internet Message Access Protocol)
--
**Opera en el puerto 143.**

IMAP fue diseñado como una moderna alternativa a POP por Mark Crispin en el año de 1986. Fundamentalmente, los dos protocolos le permiten a los clientes de correo acceder a los mensajes almacenados en un servidor de correo. Algunas de las características importantes que tiene IMAP y que carece POP3 incluyen:

* **Soporte para los modos de operación connected y disconnected**:  Al utilizar IMAP4, los clientes permanecen conectados el tiempo que su interfaz permanezca activa y descargan los mensajes bajo demanda.
* **Soporte para la conexión de múltiples clientes simultáneos a un mismo destinatario**:  Permite accesos simultáneos a múltiples clientes y proporciona ciertos mecanismos a los clientes para que se detecten los cambios hechos a un mailbox por otro cliente concurrentemente conectado.
* **Soporte para acceso a partes MIME de los mensajes y obtención parcial**: Permite a los clientes obtener separadamente cualquier parte MIME individual así como, obtener porciones de las partes individuales ó los mensajes completos.
* **Soporte para que la información de estado del mensaje se mantenga en el servidor**:  A través de la utilización de banderas definidas se puede vigilar el estado del mensaje, por ejemplo, si el mensaje ha sido o no leído, respondido o eliminado.
* **Soporte para accesar múltiples buzones de correo en el servidor**:  Los clientes pueden crear, renombrar o eliminar correo del servidor, y mover mensajes entre cuentas de correo.
* **Soporte para búsquedas de parte del servidor**: Proporciona un mecanismo para los clientes le pidan al servidor que busque mensajes de acuerdo a una cierta variedad de criterios.
* **Soporte para un mecanismo de extensión definido**: IMAP define un mecanismo explícito mediante el cual puede ser extendido. Se han propuesto muchas extensiones de IMAP4 y son de uso común.

IMAP es utilizado frecuentemente en redes grandes; por ejemplo los sistemas de correo de un campus. IMAP le permite a los usuarios acceder a los nuevos mensajes instantáneamente en sus computadoras, ya que el correo está almacenado en la red. Con POP3 los usuarios tendrían que descargar el email a sus computadoras o accesarlo vía web. 

TELNET (Telecommunication Network)
--
 **Opera en el puerto 23.**
 
El protocolo Telnet es un protocolo de Internet estándar que permite conectar terminales y aplicaciones en Internet. El protocolo proporciona reglas básicas que permiten vincular a un cliente (sistema compuesto de una pantalla y un teclado) con un intérprete de comandos (del lado del servidor). El protocolo Telnet se aplica en una conexión TCP para enviar datos en formato ASCII codificados en 8 bits, entre los cuales se encuentran secuencias de verificación Telnet. Por lo tanto, brinda un sistema de comunicación orientado bidireccional (semidúplex) codificado en 8 bits y fácil de implementar. El protocolo Telnet se basa en tres conceptos básicos:
* El paradigma Terminal virtual de red (NVT);
* El principio de opciones negociadas;
* Las reglas de negociación.

Éste es un protocolo base, al que se le aplican otros protocolos del conjunto TCP/IP (FTP, SMTP, POP3, etc.). El protocolo Telnet no es un protocolo de transferencia de datos seguro, ya que los datos que transmite circulan en la red como texto sin codificar (de manera no cifrada). La transmisión de datos a través de Telnet consiste sólo en transmitir bytes en el flujo TCP (el protocolo Telnet especifica que los datos deben agruparse de manera predeterminada —esto es, si ninguna opción especifica lo contrario— en un búfer antes de enviarse. Específicamente, esto significa que de manera predeterminada los datos se envían línea por línea). Cuando se transmite el byte 255, el byte siguiente debe interpretarse como un comando. Por lo tanto, el byte 255 se denomina IAC (Interpretar como comando).

IRC (Internet Relay Chat)
--
**Opera en el puerto 194.**

El IRC fue creado en 1988, es un protocolo que sirve para mantener conversaciones en tiempo real con otros usuarios utilizando un programa de software especial (llamado cliente) para conectarse con un servidor IRC, que a su vez, se vincula con otros servidores IRC. Todos aquellos conectados al servidor pueden participar del chat en foros públicos o privados utilizando comandos, y obedeciendo a la "etiqueta de la red" correspondiente.

Existen, de hecho, varios tipos distintos de redes IRC, cada una de ellas integrada por un grupo de servidores conectados entre sí. A tales redes se las llama:

    IRCNet
    EFNet
    DALNet

Si desea hablar con alguien en particular, necesitará conectarse al mismo tipo de red. Sin embargo, no necesita conectarse al mismo servidor, aún más, debe conectarse al servidor IRC más cercano, o, al menos, al que provea mejor conexión y, en consecuencia, el mejor tiempo de respuesta posible.

RIP (Routing Information Protocol)
--
**Opera en el puerto 520.**

RIP es un protocolo estándar. Su estado es electivo. Se describe en el RFC 1058, aunque muchas implementaciones RIP preceden este RFC por un número de años. RIP se implementa generalmente con un demonio llamado routed.

RIP se basó en los protocolos de enrutamiento de Xerox PUP y XNS. Se usa ampliamente, así que el código está incorporado en el código de enrutamiento del UNIX BSD de Berkeley que proporciona los fundamentos para muchas implementaciones UNIX.

RIP es una implementación directa del enrutamiento distancia-vector para redes locales. La comunicación RIP usa UDP como protocolo de transporte y opera en uno de los dos modos siguientes: activo (normalmente lo usan los routers) y pasivo (normalmente lo usan los hosts). Los mensajes RIP se envían en datagramas UDP y cada uno contiene 25 parejas de números.

NNTP (Network News Transfer Protocol)
--
 **Opera en el puerto 119**
 
El servicio NNTP se utiliza para intercambiar mensajes de grupos de noticias entre servidores de news. Los diferentes demonios encargados de esta tarea (como in.nntpd o innd) suelen discriminar conexiones en función de la dirección o el nombre de la máquina cliente. Los servidores NNTP son muy vulnerables a cualquier ataque que permita falsear la identidad de la máquina origen, como el IP Spoofing.

Realmente, es muy poco probable que se necesite ofrecer este servicio, por lo que lo más razonable para laseguridad es deshabilitarlo. Generalmente sólo existen servidores de noticias en grandes organizaciones - como las universidades -, y además lo normal es que sólo haya uno por entidad. 

LDAP (Lightweight Directory Access Protocol)
--
 **Opera en el puerto 389.**
 
Es un protocolo estándar que permite administrar directorios, esto es, acceder a bases de información de usuarios de una red mediante protocolos TCP/IP.

Las bases de información generalmente están relacionadas con los usuarios, pero, algunas veces, se utilizan con otros propósitos, como el de administrar el hardware de una compañía.

El objetivo del protocolo LDAP, desarrollado en 1993 en la Universidad de Michigan, fue reemplazar al protocolo DAP (utilizado para acceder a los servicios de directorio X.500 por OSI) integrándolo al TCP/IP.

LDAP le brinda al usuario métodos que le permiten:

* Conectarse
* Desconectarse
* Buscar información
* Comparar información
* Insertar entradas
* Cambiar entradas
* Eliminar entradas 

Asimismo, el protocolo LDAP (en versión 3) ofrece mecanismos de cifrado (SSL, etc.) y autenticación para permitir el acceso seguro a la información almacenada en la base. 

ARP (Address Resolution Protocol)
--
El ARP (Protocolo de resolución de direcciones) es un protocolo de nivel de red responsable de encontrar la dirección hardware (Ethernet MAC) que corresponde a una determinada dirección IP. Para ello se envía un paquete (ARP request) a la dirección de difusión de la red (broadcast (MAC = ff ff ff ff ff ff)) que contiene la dirección IP por la que se pregunta, y se espera a que esa máquina (u otra) responda (ARP reply) con la dirección Ethernet que le corresponde. Cada máquina mantiene una caché con las direcciones traducidas para reducir el retardo y la carga. ARP permite a la dirección de Internet ser independiente de la dirección Ethernet, pero esto sólo funciona si todas las máquinas lo soportan. En Ethernet, la capa de enlace trabaja con direcciones físicas. El protocolo ARP se encarga de traducir las direcciones IP a direcciones MAC (direcciones físicas). Para realizar ésta conversión, el nivel de enlace utiliza las tablas ARP, cada interfaz tiene tanto una dirección IP como una dirección física MAC. ARP se utiliza en 4 casos referentes a la comunicación entre 2 hosts:

* Cuando 2 hosts están en la misma red y uno quiere enviar un paquete a otro.
* Cuando 2 host están sobre redes diferentes y deben usar un gateway/router para alcanzar otro host.
* Cuando un router necesita enviar un paquete a un host a través de otro router.
* Cuando un router necesita enviar un paquete a un host de la misma red.

En este protocolo se necesita mucho tiempo de administración para mantener las tablas importantes en los servidores. Esto se ve reflejado aun más en las grandes redes.

PPP (Point to Point Protocol)
--

PPP es un protocolo de nivel de enlace de datos asociado a la pila TCP/IP de uso en Internet. Comúnmente usado para establecer una conexión directa entre dos nodos de una red de computadoras. Puede proveer:

* Autentificación de conexión.
* Cifrado de transmisión.
* Compresión.

PPP es usado en varios tipos de redes físicas, incluyendo: cable serial, línea telefónica, línea troncal, telefonía celular, especializado en enlace de radio y enlace de fibra óptica como SONET (Synchronous Optical Network). También es utilizado en las conexiones de acceso a Internet (mercadeado como “banda ancha” o “broadband”).

Dos derivados del PPP son:

    Point to Point Protocol over Ethernet (PPPoE),
    Point to Point Protocol over ATM (PPPoA).

Son usados comúnmente por los ISP para establecer una línea de abonado digital (Digital Subscriber Line, DSL) de servicios de Internet para clientes.

NFS (Network File System)
--

El  (Sistema de archivos de red), o NFS, es un protocolo de nivel de aplicación, según el Modelo OSI. Es utilizado para sistemas de archivos distribuido en un entorno de red de computadoras de área local. Posibilita que distintos sistemas conectados a una misma red accedan a ficheros remotos como si se tratara de locales. Originalmente fue desarrollado en 1984 por Sun Microsystems, con el objetivo de que fuera independiente de la máquina, el sistema operativo y el protocolo de transporte, esto fue posible gracias a que está implementado sobre los protocolos XDR (presentación) y ONC RPC (sesión).1 El protocolo NFS está incluido por defecto en los Sistemas Operativos UNIX y la mayoría de distribuciones Linux.

El sistema NFS está dividido al menos en dos partes principales: un servidor y uno o más clientes. Los clientes acceden de forma remota a los datos que se encuentran almacenados en el servidor. Los usuarios no necesitan disponer de un directorio “home” en cada una de las máquinas de la organización. 

**Bibliografía**

* http://www.internetmania.net/int0/int133.htm
* http://www.casdreams.com/auladeinformatica/cet/famprot.htm
* http://www.puertosabiertos.com/es/lista-de-puertos.htm

