::: {#page .hfeed .site}
[Saltar al contenido](index.html#content){.skip-link
.screen-reader-text}

::: {#sidebar .sidebar}
::: {.site-branding}
[![](../../../../../wp-content/uploads/2016/04/cropped-Manneken_Pis_Blog_Bruselas_Ricardo_Imbern-248.jpg){.custom-logo
width="248" height="248" sizes="(max-width: 248px) 100vw, 248px"
srcset="../../../../../wp-content/uploads/2016/04/cropped-Manneken_Pis_Blog_Bruselas_Ricardo_Imbern-248.jpg 248w, ../../../../../wp-content/uploads/2016/04/cropped-Manneken_Pis_Blog_Bruselas_Ricardo_Imbern-248-150x150.jpg 150w"}](../../../../../index.html){.custom-logo-link}

[Blog Bruselas en español](../../../../../index.html)

El blog-guía escrito por españoles en Bruselas para los hispanoparlantes
que viven aquí y para los turistas que aprovechan los vuelos baratos
para descubrir el chocolate, la cerveza, la Grand Place y tantas otras
cosas buenas.

Menú y widgets
:::

::: {#secondary .secondary}
::: {#widget-area .widget-area role="complementary"}
Blog Bruselas es {#blog-bruselas-es .widget-title}
----------------

::: {.textwidget}
Un **blog en español escrito en Bruselas** por unos enamorados de la
capital de Bélgica, corazón mágico de Europa. Una ciudad pequeña y
grande, llena de gente, comida, eventos y rincones encantadores; para
descubrir y disfrutar sin dejarse aguar la fiesta por el tiempo (no es
tan malo).

Para quienes pasan por Bruselas, porque vienen de visita, de turismo o
tienen la suerte de vivir aquí. Sí quieres conocer más que los hoteles
en Bruselas, aprovecha los vuelos baratos y **vive la ciudad**.

Blog Bruselas es el bebé de [Ramón Suárez](http://www.ramonsuarez.com),
bruseleño convencido desde 2003.
:::

Espacios de trabajo compartido {#espacios-de-trabajo-compartido .widget-title}
------------------------------

::: {.textwidget}
[Betacowork Coworking Bruselas](http://www.betacowork.com) [Mapa de
espacios de coworking en Bélgica](http://coworkingbelgium.com)
:::

Último vídeo {#último-vídeo .widget-title}
------------

Asociados con Hispagenda, la guía digital de los españoles en Bélgica {#asociados-con-hispagenda-la-guía-digital-de-los-españoles-en-bélgica .widget-title}
---------------------------------------------------------------------

::: {.textwidget}
[![Hispagenda,la guía digital de los españoles en
Bélgica](../../../../../wp-content/uploads/2010/04/Hispagenda-250px.gif "Hispagenda, la guía digital de los españoles en Bélgica"){.attachment-medium
width="250" height="100"}](http://www.hispagenda.com)
:::

Más sobre Bruselas en otros idiomas {#más-sobre-bruselas-en-otros-idiomas .widget-title}
-----------------------------------

::: {.textwidget}
[Agenda.be](http://www.agenda.be) FR NL\
[Bruxelles Blog](http://www.bxlblog.be/) FR\
[Eventos para emprendedores y freelance en
Bruselas](http://www.betacowork.com/events/)\
[The Network
Brussels](http://groups.yahoo.com/group/TheNetworkBrussels/) EN\
[What\'s up in Belgium](http://www.whatsupin.be/) EN
:::

Más sobre Bélgica en Español {#más-sobre-bélgica-en-español .widget-title}
----------------------------

::: {.textwidget}
[Spaniards en Bélgica](http://www.spaniards.es/paises/belgica)
:::
:::
:::
:::

::: {#content .site-content}
::: {#primary .section .content-area}
::: {#main .site-main role="main"}
Categoría: Informática {#categoría-informática .page-title}
======================

::: {.taxonomy-description}
Algunos somos *geeks* (pronunciado guics), nos gustan la informática,
cacharrear y solucionar los problemas informáticos con los que nos
encontramos. La solución siempre es más fácil de lo que parece, aunque
para la mayoría esta sección es un auténtico coñazo. Pobrecill\@s.
:::

[Problema librerías QT en Linux](../../../../../index.html?p=294) {#problema-librerías-qt-en-linux .entry-title}
-----------------------------------------------------------------

::: {.entry-content}
Lo reconozco: enredo mucho con el ordenador, y claro, pasa lo que pasa,
que me voy cargando cosillas (o cosazas) cada poco. ¡Soy peligroso! Por
suerte la mayoría las consigo arreglar.

Esta vez tuve un problema con las librerías QT (no tengo ni idea de que
lo ocasionó pero intuyo que fue la instalación de Adobe Air) que me
impedía utilizar [Skype](http://www.skype.com/),
[Last.fm](http://www.last.fm/) y
[VirtualBox](http://www.virtualbox.org/). Lancé un par de peticiones de
ayuda en internet
([uno](https://bugs.launchpad.net/ubuntu/+source/qt4-x11/+bug/115970) y
[dos](https://bugs.launchpad.net/ubuntu/+source/qt4-x11/+bug/340252)).

La solución fue sencilla (gracias a
[Terence](https://bugs.launchpad.net/%7Etsimpson)): borrar las librerías
QT que había en el directorio
[/usr/local/lib]{style="font-style: italic;"}. ¡Bingo!

Además mandé una petición de socorro a
[Aitor](http://vueltaabruselas.blogspot.com/), mi nuevo gurú linuxero en
Bruselas, que me correspondió con todo un curso de iniciación a Linux
que no se puede desperdiciar y que publicaré resumido bien pronto.

He aquí su explicación de mi problema y de lo que son las librerías:

> El problema que tuviste tu fue equivalente al problema de "dll hell"
> en windows. Seguro que conoces los archivos ".dll" de windows aunque
> te resulte difusa y oscura la razón de su existencia, bueno los
> equivalentes a .dll de windows en linux son los archivos ".so". Todos
> los programas ejecutables de windows usan dlls aunque no venga ninguna
> instalada en el programa hacen uso de las que tienes presentes en
> windows/system32.
>
> Las dll son exactamente iguales que un ejecutable .exe, solo que
> carecen de una función de arranque y por tanto no pueden ser
> inicializadas haciendo click sobre ellas, los dll son librerías
> dinámicas de funciones que ayudan a muchas cosas y a no tener que
> reinventar la rueda con cada programa que hacemos. El problema es que
> cuando tienes dos dll o dos so que se llaman igual y encima son de
> versiones diferentes pueden tener funciones diferentes dentro y
> provocar que programas se bloqueen y acaben en error como te pasaba a
> ti que buscaba una función que no existia en tu libreria .so En tu
> caso el problema que tenías era que skype hacía uso de una librería
> .so que debía de ser antigua y que fue instalada por el adobe air o
> eso.
>
> El comando ldd sobre cualquier ejecutable te da que librerías
> dinámicas utiliza (.so), en Windows hay algun comando equivalente pero
> creo que no viene en la instalación de Windows sino con algún paquete
> de desarrollo de microsoft, yo suelo usar éste:
> <http://www.dependencywalker.com/> cuando me apetece echar un vistazo
> a un exe y ver que dlls utiliza.

¡Gracias o oráculo linuxero bruselero! 🙂

::: {.blogger-post-footer}
Comer, hablar, amar. www.blogbruselas.com
:::
:::

[[Publicado el
]{.screen-reader-text}[09/04/2009](../../../../../index.html?p=294)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../../../2010/04/30/index.html?author=2){.url .fn
.n}]{.author .vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Informática](../../index.html)]{.cat-links}[[[1
comentario[ en Problema librerías QT en
Linux]{.screen-reader-text}]{.dsq-postid
dsqidentifier="294 http://www.blogbruselas.com/2009/04/problema-librerias-qt-en-linux.html"}](../../../../../index.html?p=294#comments)]{.comments-link}

[Quedada con bloggers belgas esta tarde](../../../../../index.html?p=286) {#quedada-con-bloggers-belgas-esta-tarde .entry-title}
-------------------------------------------------------------------------

::: {.entry-content}
Como ya os comenté [hace un
tiempo](http://comerhablaramar.blogspot.com/2009/03/yulbiz-conoce-bloggers-belgas.html),
esta tarde hay [Yulbiz en
Bruselas](http://www.vinch.be/blog/2009/03/10/yulbiz-bruxelles-6-au-wax-club/).
Es la ocasión perfecta para tomarse unas cerves tranquilamente y conocer
a unos cuantos bloggers belgas 🙂 A diferencia del [Beta
Group](http://betagroup9.eventbrite.com/), en esta ocasión no hay
presentaciones de empresas, tan solo gente conociendo a gente.\
Lo que sí habrá es un [experimento de usabilidad
[guerrilero]{style="font-style: italic;"}](http://www.vinch.be/blog/2009/03/13/guerilla-test-dergonomie-a-yulbiz-bruxelles-6/)
usando Silverback para evaluar la página de Skilto (no pongo el enlace
para no caer en la tentación de mirar la página antes de esta noche):
¡podremos ser cobayas!. Como de mayor quiero ser geek, no puedo perder
la oportunidad, aunque haya que hacerlo sobre un Mac con el teclado en
[Azerty](http://comerhablaramar.blogspot.com/2008/12/azerty.html).

::: {style="text-align: center;"}
:::

La cita: desde las 18h30 en [The Wax
Club](http://comerhablaramar.blogspot.com/2007/04/wax-club-la-mejor-msica-electrnica-de.html)
(Bvd Anspach 66). Y a partir de las 21h curso gratis de salsa, para
sacarle brillo a los bajos del blog.

::: {style="text-align: center;"}
:::

¿Donde se ha dejado el 4?

::: {.blogger-post-footer}
Comer, hablar, amar. www.blogbruselas.com
:::
:::

[[Publicado el
]{.screen-reader-text}[26/03/2009](../../../../../index.html?p=286)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../../../2010/04/30/index.html?author=2){.url .fn
.n}]{.author .vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Blogs](../../../blogs/index.html), [Emprendedores
Internet](../../../emprendedores-internet/index.html), [Gran
Bruselas](../../../gran-bruselas/index.html),
[Informática](../../index.html)]{.cat-links}[[[6 comentarios[ en Quedada
con bloggers belgas esta tarde]{.screen-reader-text}]{.dsq-postid
dsqidentifier="286 http://www.blogbruselas.com/2009/03/quedada-con-bloggers-belgas-esta-tarde.html"}](../../../../../index.html?p=286#comments)]{.comments-link}

[Como importar tu correo electrónico a Gmail desde cualquier programa (Outlook, Thunderbird, Apple...)](../../../../../index.html?p=250) {#como-importar-tu-correo-electrónico-a-gmail-desde-cualquier-programa-outlook-thunderbird-apple .entry-title}
----------------------------------------------------------------------------------------------------------------------------------------

::: {.entry-content}
1.- Configura el cliente de correo electrónico en el que tienes los
email que quieres importar para que se conecte por [IMAP a
Gmail](http://mail.google.com/support/bin/answer.py?answer=75726) (los
enlaces dirigen directamente a la ayuda de Gmail para cada programa):

-   [Outlook
    Express](http://mail.google.com/support/bin/answer.py?answer=77659)
    (Windows)
-   [Outlook
    2003](http://mail.google.com/support/bin/answer.py?answer=77661)
    (Windows)
-   [Outlook
    2007](http://mail.google.com/support/bin/answer.py?answer=77689)
    (Windows)
-   [Apple
    Mail](http://mail.google.com/support/bin/answer.py?answer=77663)
-   [Apple Mail 3.0
    (Leopard)](http://mail.google.com/support/bin/answer.py?answer=81379)
-   [Windows
    Mail](http://mail.google.com/support/bin/answer.py?answer=77696)
-   [Thunderbird
    2.0](http://mail.google.com/support/bin/answer.py?answer=77662)
-   [Otros](http://mail.google.com/support/bin/answer.py?answer=78799)\*

> **Dispositivos inalámbricos**
>
> -   [iPhone](https://mail.google.com/support/bin/answer.py?answer=77702)
> -   [Blackberry](https://mail.google.com/support/bin/answer.py?answer=78882)\*
> -   [Symbian](https://mail.google.com/support/bin/answer.py?answer=78887)\*
> -   [Windows Mobile
>     5](https://mail.google.com/support/bin/answer.py?answer=10149)\*
> -   [Windows Mobile
>     6](https://mail.google.com/support/bin/answer.py?answer=78886)\*
> -   [SnapperMail](https://mail.google.com/support/bin/answer.py?answer=80802)\*

2.- Arrastra el correo o las carpetas que quieras copiar de tu cuenta a
la que acabas de abrir en Gmail, teniendo en cuenta que:

-   Pinchar y arrastrar normalmente mueve los archivos (se borran del
    origen y quedarán únicamente en destino) pero copia las carpetas (no
    se borran en origen). Para copiar los archivos, pulsa la tecla
    Control al mismo tiempo que arrastras los archivos o selecciona
    copiar del menu que sale al pinchar con el botón derecho del ratón.
-   El sistema de carpetas/conversaciones de GMail es diferente al de la
    gran mayoría de programas: [Gmail usa
    etiquetas](http://mail.google.com/support/bin/answer.py?answer=10708&topic=13284)
    (como las de los blogs) en lugar de usar subcarpetas.
-   Las carpetas solo se pueden copiar una a una.
-   Sí arrastras las carpetas a la bandeja de entrada (o
    [Inbox]{style="font-style: italic;"}) se te van a marcar con la
    etiqueta: [/Inbox/Carpeta]{style="font-style: italic;"}. Es mejor
    arrastrarlas directamente sobre el nombre de la cuenta de
    IMAP-Gmail.
-   Si tienes muchos correos en cada carpeta o si son muy pesados [va a
    tardar]{style="font-weight: bold;"} un buen rato cada vez.
-   Se te va a saturar la conexión a internet mientras está haciendo la
    sincronización, sobre todo al principio de cada tanda de correos.
-   Puede que se interrumpa el proceso (parece que a Google no le debe
    gustar que utilicemos todos esos megas de almacenamiento gratuito):
    cuando se interrumpa coje los correos que queden y arrástralos a la
    carpeta correspondiente en la cuenta de Gmail.
-   Puedes seguir trabajando desde tu cuenta de Gmail en línea, pero
    mejor hacerlo desde otro ordenador porque a veces con la carga de
    los correos se ralentiza mucho la conexión a internet.

Con este método, a diferencia de lo que sucede al usar programas como
[GML](http://marklyon.org/gmail/default.htm), se conservan las fechas
originales de los mensajes, el remitente y el estado de leído/no leído
que tengas marcado. Al no tener que instalar ningún programa, es muy
útil y sencillo para hacer copias de seguridad del correo electrónico y
normalmente se puede utilizar en casi cualquier ordenador (excepto en
algunas empresas donde limitan la creación de cuentas).

Yo he hecho la prueba con Evolution ([hace un montón de
tiempo](http://comerhablaramar.blogspot.com/2008/04/pero-que-contento-estoooy.html))
y con Thunderbird y me ha ido pero que muy bien.

A ti, ¿qué tal te funciona?

[Actualización]{style="font-weight: bold;"}: Por supuesto, este método
también es aplicable en caso de que quieras mover o copiar tu correo
electrónico entre dos cuentas de Gmail. Para ello tan solo hay que abrir
las dos cuentas en IMAP con cualquier programa de correo y arrastrar los
archivos que te interesen a la cuenta de Gmail que prefieras.

::: {.blogger-post-footer}
Comer, hablar, amar. www.blogbruselas.com
:::
:::

[[Publicado el
]{.screen-reader-text}[25/02/2009](../../../../../index.html?p=250)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../../../2010/04/30/index.html?author=2){.url .fn
.n}]{.author .vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Informática](../../index.html)]{.cat-links}[[[3
comentarios[ en Como importar tu correo electrónico a Gmail desde
cualquier programa (Outlook, Thunderbird,
Apple...)]{.screen-reader-text}]{.dsq-postid
dsqidentifier="250 http://www.blogbruselas.com/2009/02/como-importar-tu-correo-electronico-a-gmail-desde-cualquier-programa-outlook-thunderbird-apple.html"}](../../../../../index.html?p=250#comments)]{.comments-link}

[Tacos en Facebook](../../../../../index.html?p=247) {#tacos-en-facebook .entry-title}
----------------------------------------------------

::: {.entry-content}
Hay que ver lo malhablados que podemos ser:

[![](http://3.bp.blogspot.com/_m9ESRqvSnjc/SZ6vq4hzUPI/AAAAAAAAB_s/wrhBRkfEhnU/s400/Tacos+y+palabrotas+en+facebook.png){#BLOGGER_PHOTO_ID_5304870562352550130}](http://3.bp.blogspot.com/_m9ESRqvSnjc/SZ6vq4hzUPI/AAAAAAAAB_s/wrhBRkfEhnU/s1600-h/Tacos+y+palabrotas+en+facebook.png)\
Esta y otras [joyas de la
lengua](http://es.wikipedia.org/wiki/Decir_tacos) en el
[Lexicon](http://www.facebook.com/lexicon/), la herramienta para ver de
que se está hablando en [Facebook](http://www.facebook.com/).

Y ya que estás allí, puede ser un buen momento para hacerte [fan de
Comer, hablar, amar en
Facebook](http://www.facebook.com/pages/Comer-hablar-amar-vivir-al-fin-y-al-cabo/14471236332?ref=ts).

::: {.blogger-post-footer}
Comer, hablar, amar. www.blogbruselas.com
:::
:::

[[Publicado el
]{.screen-reader-text}[22/02/2009](../../../../../index.html?p=247)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../../../2010/04/30/index.html?author=2){.url .fn
.n}]{.author .vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Humor](../../../humor/index.html),
[Informática](../../index.html)]{.cat-links}

[¿Encontré la solución a mi problema de RAID en Ubuntu?](../../../../../index.html?p=242) {#encontré-la-solución-a-mi-problema-de-raid-en-ubuntu .entry-title}
-----------------------------------------------------------------------------------------

::: {.entry-content}
[AVISO]{style="font-weight: bold;"}: MENSAJE COÑAZO, SOLO PARA GENTE
INTERESADA EN TEMAS INFORMÁTICOS (y el que avisa no es traidor)

[![](http://farm1.static.flickr.com/46/152611490_c18ff8e48a_o_d.jpg)](http://farm1.static.flickr.com/46/152611490_c18ff8e48a_o_d.jpg)\
Estas navidades me regalé entre otras cosas un ordenador nuevo. Mi gran
preocupación después de [la muerte del disco duro de mi
portatil](http://comerhablaramar.blogspot.com/2008/10/ordenadores-y-piezas-nuevos-y-de.html)
es la salvaguarda de mis datos. Además de hacer copias de seguridad
regularmente, quería tener un ordenador con dos discos duros pero que
actuasen como uno solo, siendo una réplica exacta por si falla uno poder
recuperar los datos fácilmente del otro y seguir trabajando sin
problema. Vamos, instalando un [RAID
1](http://www.google.be/search?q=define:raid+1&num=50&hl=en&safe=off&client=firefox-a&rls=com.ubuntu:en-US:unofficial&hs=jMf&oi=definel&defl=es).

Así que me instalé [Ubuntu
8.04](http://www.ubuntu.com/getubuntu/download) siguiendo las magníficas
instrucciones del blog de [Bobby
Allen](http://comerhablaramar.blogspot.com/2008/10/ordenadores-y-piezas-nuevos-y-de.html).
Ningún problema y facilísimo. Todo instalado y funcionando... hasta que
paré la máquina y volví a encenderla al día siguiente: mi
[bios](http://www.google.be/search?q=define:bios&num=50&hl=en&safe=off&client=firefox-a&rls=com.ubuntu:en-US:unofficial&hs=5wz&oi=definel&defl=es)
ya no reconocía mis discos y me daba un error [Offline
Member]{style="font-style: italic;"}, que se traducía en que no los
reconocía y decía que no había sistema operativo.

Para hacer las cosas más raras todavía, si arrancaba el sistema con el
[Live CD de Ubuntu](https://help.ubuntu.com/community/LiveCD) y lo
reiniciaba después, el ordenador cargaba el sistema operativo sin
problemas y con el RAID funcionando... hasta que paraba el ordenador
(parar, que si reiniciaba todo iba de maravilla).

Tras dar muchas vueltas por la red y hacer multitud de experimentos, mi
intuición me ha llevado a fijarme en la
[bios]{style="font-style: italic;"} de la placa base (una [Gigabyte
EP35C-DS3R](http://www.gigabyte.com.tw/Products/Motherboard/Products_Overview.aspx?ProductID=2740)).
Me da en la nariz que lo que pasa es que ella y Ubuntu no ven los discos
duros de la misma manera: la [bios]{style="font-style: italic;"} da un
tamaño menor de disco.

Pues nada, urgando, urgando he decidido cambiar la opción del disco en
la [bios]{style="font-style: italic;"} de RAID a AHCI y ¡bingo! El
ordenador ha arrancado sin problemas y encima parece que el RAID sigue
funcionando.

Ejecutando [sudo mdadm --detail /dev/md\*]{style="font-style: italic;"}
para ver el estado de mis discos, me encuentro con esto:

> /dev/md0:\
> Version : 00.90.03\
> Creation Time : Fri Jan 30 19:07:05 2009\
> Raid Level : raid1\
> Array Size : 19631296 (18.72 GiB 20.10 GB)\
> Used Dev Size : 19631296 (18.72 GiB 20.10 GB)\
> Raid Devices : 2\
> Total Devices : 2\
> Preferred Minor : 0\
> Persistence : Superblock is persistent
>
> Update Time : Thu Feb 12 18:31:45 2009\
> State : active\
> Active Devices : 2\
> Working Devices : 2\
> Failed Devices : 0\
> Spare Devices : 0
>
> UUID : c031503c:a0481358:c9c7cb55:8db4e538\
> Events : 0.9
>
> Number Major Minor RaidDevice State\
> 0 8 1 0 active sync /dev/sda1\
> 1 8 17 1 active sync /dev/sdb1\
> /dev/md1:\
> Version : 00.90.03\
> Creation Time : Fri Jan 30 19:07:46 2009\
> Raid Level : raid1\
> Array Size : 390628416 (372.53 GiB 400.00 GB)\
> Used Dev Size : 390628416 (372.53 GiB 400.00 GB)\
> Raid Devices : 2\
> Total Devices : 2\
> Preferred Minor : 1\
> Persistence : Superblock is persistent
>
> Update Time : Thu Feb 12 18:31:43 2009\
> State : clean, recovering\
> Active Devices : 2\
> Working Devices : 2\
> Failed Devices : 0\
> Spare Devices : 0
>
> Rebuild Status : 94% complete
>
> UUID : 9a5262b1:3ee23754:a09c7648:1aacb58d\
> Events : 0.20
>
> Number Major Minor RaidDevice State\
> 0 8 2 0 active sync /dev/sda2\
> 1 8 18 1 active sync /dev/sdb2\
> /dev/md2:\
> Version : 00.90.03\
> Creation Time : Fri Jan 30 19:08:06 2009\
> Raid Level : raid1\
> Array Size : 69039232 (65.84 GiB 70.70 GB)\
> Used Dev Size : 69039232 (65.84 GiB 70.70 GB)\
> Raid Devices : 2\
> Total Devices : 2\
> Preferred Minor : 2\
> Persistence : Superblock is persistent
>
> Update Time : Thu Feb 12 17:49:59 2009\
> State : clean\
> Active Devices : 2\
> Working Devices : 2\
> Failed Devices : 0\
> Spare Devices : 0
>
> UUID : 4417b9b7:8171282f:4c4da224:3c9d7028\
> Events : 0.8
>
> Number Major Minor RaidDevice State\
> 0 8 3 0 active sync /dev/sda3\
> 1 8 19 1 active sync /dev/sdb3\
> /dev/md3:\
> Version : 00.90.03\
> Creation Time : Fri Jan 30 19:08:19 2009\
> Raid Level : raid1\
> Array Size : 9084672 (8.66 GiB 9.30 GB)\
> Used Dev Size : 9084672 (8.66 GiB 9.30 GB)\
> Raid Devices : 2\
> Total Devices : 2\
> Preferred Minor : 3\
> Persistence : Superblock is persistent
>
> Update Time : Thu Feb 12 17:49:59 2009\
> State : clean\
> Active Devices : 2\
> Working Devices : 2\
> Failed Devices : 0\
> Spare Devices : 0
>
> UUID : 695daa0c:50b26d73:23bcfd41:67ef2725\
> Events : 0.10
>
> Number Major Minor RaidDevice State\
> 0 8 4 0 active sync /dev/sda4\
> 1 8 20 1 active sync /dev/sdb4

Con lo que parece que todo está OK (incluso el mensaje de recuperación,
que hoy han saltado los plomos de mi edificio mientras estaba el
ordenador funcionando).

¿Lo habré solucionado o estaré viviendo un sueño, una mera ilusión?

::: {.blogger-post-footer}
Comer, hablar, amar. www.blogbruselas.com
:::
:::

[[Publicado el
]{.screen-reader-text}[12/02/2009](../../../../../index.html?p=242)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../../../2010/04/30/index.html?author=2){.url .fn
.n}]{.author .vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Informática](../../index.html)]{.cat-links}[[[7
comentarios[ en ¿Encontré la solución a mi problema de RAID en
Ubuntu?]{.screen-reader-text}]{.dsq-postid
dsqidentifier="242 http://www.blogbruselas.com/2009/02/%c2%bfencontre-la-solucion-a-mi-problema-de-raid-en-ubuntu.html"}](../../../../../index.html?p=242#comments)]{.comments-link}

Navegación de entradas {#navegación-de-entradas .screen-reader-text}
----------------------

::: {.nav-links}
[Página anterior](../4/index.html){.prev .page-numbers} [[Página
]{.meta-nav .screen-reader-text}1](../../index.html){.page-numbers}
[...]{.page-numbers .dots} [[Página ]{.meta-nav
.screen-reader-text}4](../4/index.html){.page-numbers} [[Página
]{.meta-nav .screen-reader-text}5]{.page-numbers .current} [[Página
]{.meta-nav .screen-reader-text}6](../6/index.html){.page-numbers}
[...]{.page-numbers .dots} [[Página ]{.meta-nav
.screen-reader-text}16](../16/index.html){.page-numbers} [Página
siguiente](../6/index.html){.next .page-numbers}
:::
:::
:::
:::

::: {.site-info}
[Creado con WordPress](https://es.wordpress.org/)
:::
:::
