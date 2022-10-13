::: {#page .hfeed .site}
[Saltar al contenido](index.html#content){.skip-link
.screen-reader-text}

::: {#sidebar .sidebar}
::: {.site-branding}
[![](../../wp-content/uploads/2016/04/cropped-Manneken_Pis_Blog_Bruselas_Ricardo_Imbern-248.jpg){.custom-logo
width="248" height="248" sizes="(max-width: 248px) 100vw, 248px"
srcset="../../wp-content/uploads/2016/04/cropped-Manneken_Pis_Blog_Bruselas_Ricardo_Imbern-248.jpg 248w, ../../wp-content/uploads/2016/04/cropped-Manneken_Pis_Blog_Bruselas_Ricardo_Imbern-248-150x150.jpg 150w"}](../../index.html){.custom-logo-link}

[Blog Bruselas en español](../../index.html) {#blog-bruselas-en-español .site-title}
============================================

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
Bélgica](../../wp-content/uploads/2010/04/Hispagenda-250px.gif "Hispagenda, la guía digital de los españoles en Bélgica"){.attachment-medium
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
::: {#primary .content-area}
::: {#main .site-main role="main"}
[¿Encontré la solución a mi problema de RAID en Ubuntu?](../../index.html?p=242) {#encontré-la-solución-a-mi-problema-de-raid-en-ubuntu .entry-title}
--------------------------------------------------------------------------------

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
]{.screen-reader-text}[12/02/2009](../../index.html?p=242)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../blog/2010/04/30/index.html?author=2){.url .fn .n}]{.author
.vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Informática](../../blog/category/informatica/index.html)]{.cat-links}[[[7
comentarios[ en ¿Encontré la solución a mi problema de RAID en
Ubuntu?]{.screen-reader-text}]{.dsq-postid
dsqidentifier="242 http://www.blogbruselas.com/2009/02/%c2%bfencontre-la-solucion-a-mi-problema-de-raid-en-ubuntu.html"}](../../index.html?p=242#comments)]{.comments-link}

[Beta Group el 3 de marzo en la ULB](../../index.html?p=241) {#beta-group-el-3-de-marzo-en-la-ulb .entry-title}
------------------------------------------------------------

::: {.entry-content}
::: {.separator style="clear: both; text-align: center;"}
[![](http://farm4.static.flickr.com/3263/2802091425_e04d1e9ce5.jpg?v=0){width="420"
height="142"}](http://farm4.static.flickr.com/3263/2802091425_e04d1e9ce5.jpg?v=0)
:::

[Vuelvo a la
carga](http://comerhablaramar.blogspot.com/2008/10/start-ups-y-networking-en-bruselas.html)
con el mejor evento que hay ahora mismo en Bruselas para todos aquellos
que tengan un interés en el mundillo empresarial de la red: el [Beta
Group](http://betagroup.be/).

La próxima cita es el 3 de marzo y presentarán:

[1) [Mollom.com](http://www.mollom.com/) by
[Benjamin](http://www.linkedin.com/in/benjaminschrauwen)]{style=";font-family:verdana,geneva;font-size:100%;"}

[2) [yourtour.com](http://www.yourtour.com/) by
[Emmanuel](http://www.linkedin.com/pub/3/222/37b)]{style=";font-family:verdana,geneva;font-size:100%;"}[\
]{style=";font-family:verdana,geneva;font-size:100%;"}

[3) [moodio.tv](http://www.moodio.tv/) by
[Jonathan](http://www.linkedin.com/in/jonathansurinx)]{style=";font-family:verdana,geneva;font-size:100%;"}

[4)
[Extrafoot.be](http://www.extrafoot.be/)]{style=";font-family:verdana,geneva;font-size:100%;"}[
-- [Extravoetbal.be](http://www.extravoetbal.be/) by
[Vincent](http://www.linkedin.com/pub/3/12b/a76)]{style=";font-family:verdana,geneva;font-size:100%;"}

[5) [incloode.com](http://www.incloode.com/) by
[Michael](http://www.linkedin.com/in/michaeldaun)]{style=";font-family:verdana,geneva;font-size:100%;"}[\
]{style=";font-family:verdana,geneva;font-size:100%;"}

Las presentaciones suelen estar bien y siempre es interesante ver las
nuevas ideas en las que está trabajando la gente. Lo mejor de todas
formas es el vinito de después donde se puede hablar fácilmente con un
montón de gente interesante e interesada en los mismos temas que menda,
lo cual es un gustazo (sobre todo teniendo en cuenta que yo de mayor
quiero ser
[geek](http://www.google.be/url?sa=X&start=35&oi=define&q=http://es.wikipedia.org/wiki/Geek&usg=AFQjCNGB3VYeErg8x0J3idN-OTH8mupMfg))

Yo ya he confirmado mi participación. ¿Os apuntáis?

::: {.blogger-post-footer}
Comer, hablar, amar. www.blogbruselas.com
:::
:::

[[Publicado el
]{.screen-reader-text}[12/02/2009](../../index.html?p=241)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../blog/2010/04/30/index.html?author=2){.url .fn .n}]{.author
.vcard}]{.byline}[[Categorías ]{.screen-reader-text}[Comunicación y
marketing](../../blog/category/comunicacion-y-marketing/index.html),
[Emprendedores
Internet](../../blog/category/emprendedores-internet/index.html), [Gran
Bruselas](../../blog/category/gran-bruselas/index.html),
[Informática](../../blog/category/informatica/index.html)]{.cat-links}[[[1
comentario[ en Beta Group el 3 de marzo en la
ULB]{.screen-reader-text}]{.dsq-postid
dsqidentifier="241 http://www.blogbruselas.com/2009/02/beta-group-el-3-de-marzo-en-la-ulb.html"}](../../index.html?p=241#comments)]{.comments-link}

[Se nos van los bloggers](../../index.html?p=240) {#se-nos-van-los-bloggers .entry-title}
-------------------------------------------------

::: {.entry-content}
Una blogger de las nuestras [ha dejado
Bruselas](http://cartasdesdebruselas.blogspot.com/2009/02/el-regalo-final.html)
y otro se está preparando para [cruzar el
charco](http://zugaldia.wordpress.com/). ¿Quién toma el relevo?

::: {.blogger-post-footer}
Comer, hablar, amar. www.blogbruselas.com
:::
:::

[[Publicado el
]{.screen-reader-text}[10/02/2009](../../index.html?p=240)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../blog/2010/04/30/index.html?author=2){.url .fn .n}]{.author
.vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Blogs](../../blog/category/blogs/index.html),
[Gran
Bruselas](../../blog/category/gran-bruselas/index.html)]{.cat-links}[[[1
comentario[ en Se nos van los
bloggers]{.screen-reader-text}]{.dsq-postid
dsqidentifier="240 http://www.blogbruselas.com/2009/02/se-nos-van-los-bloggers.html"}](../../index.html?p=240#comments)]{.comments-link}

[Gilipollismo viral en la Grand Place](../../index.html?p=239) {#gilipollismo-viral-en-la-grand-place .entry-title}
--------------------------------------------------------------

::: {.entry-content}
[![](http://1.bp.blogspot.com/_m9ESRqvSnjc/SZCIRs8EUjI/AAAAAAAAB_A/xDFlO_CxYQQ/s400/Hector+y+Ram%C3%B3n.Gilipollas+2+y+3+de+Bruselas.JPG){#BLOGGER_PHOTO_ID_5300886599117328946}](http://1.bp.blogspot.com/_m9ESRqvSnjc/SZCIRs8EUjI/AAAAAAAAB_A/xDFlO_CxYQQ/s1600-h/Hector+y+Ram%C3%B3n.Gilipollas+2+y+3+de+Bruselas.JPG)\
El fantasma del gilipollismo recorre Europa, y parece que hace especial
mella en Bruselas. Aunque sea con una semanica de retraso, tengo el
placer de anunciar que ya tenemos Gilipollas III de Bélgica (mientras
dure). El honor y la responsabilidad han caído sobre los hombros de
[Hector](http://nosolocoles.blogspot.com/), que estoy seguro sabrá
asumir la carga y además transmitir debidamente el gilipollismo
([Borja](http://entreflamencosybalones.blogspot.com/) está haciendo
méritos para ser el IV).

La [infección](http://www.jabcomics.com/) ha tardado en transmitirse un
poco desde la ya [legendaria
transmisión](http://comerhablaramar.blogspot.com/2008/12/tengo-al-nio-gilipollas-al-menos-el.html)
de Antonio, Gilipollas I, a un humilde servidor. Por lo menos así me he
podido recuperar de las secuelas (las físicas que las mentales no hacen
más que empeorar) del gran catacroc volador .

[![](http://1.bp.blogspot.com/_m9ESRqvSnjc/SZCNmOmGkdI/AAAAAAAAB_M/3MzuT4dh9Ks/s200/Condes+decapitados+por+los+espa%C3%B1oles+en+Bruselas.JPG){#BLOGGER_PHOTO_ID_5300892449307529682}](http://1.bp.blogspot.com/_m9ESRqvSnjc/SZCNmOmGkdI/AAAAAAAAB_M/3MzuT4dh9Ks/s1600-h/Condes+decapitados+por+los+espa%C3%B1oles+en+Bruselas.JPG)Para
esta ocasión, en plena Grand Place, nada mejor que situarnos bajo la
placa de dos [precursores
locales](http://es.wikipedia.org/wiki/Conde_de_Horn) a los que en su
afán por volar en libertad vinieron a ayudar nuestros
hispano-antepasados: cortecico en el cuello y ¡hala, a volar hasta el
cestico!

Después de tan ilustre ocasión e inspirados por la placa de la
decapitación de marras, nos fuimos a degustar unos traguillos al ataud
([Le Cerceuil](http://www.ebru.be/Cafes/CafCercueil.html)). Por cuestión
de decalaje horario no nos atrevimos con las [calaveras
cerveceras](http://www.ebru.be/Cafes/CafePict/CafCercueil3.jpg), pero de
todas formas nos echamos unas risas escuchando heavy comercialón del
viejo y charlando de todas las cosas que nos gustan de Bruselas.

[![](http://3.bp.blogspot.com/_m9ESRqvSnjc/SZCPuMysF5I/AAAAAAAAB_U/0_x0dmL2y0w/s200/Hector+y+Borja+en+Le+Cercueil.JPG){#BLOGGER_PHOTO_ID_5300894785285658514}](http://3.bp.blogspot.com/_m9ESRqvSnjc/SZCPuMysF5I/AAAAAAAAB_U/0_x0dmL2y0w/s1600-h/Hector+y+Borja+en+Le+Cercueil.JPG)Como
este mensaje está destinado para la historia (me salto lo de los
[anales](http://es.wikipedia.org/wiki/Anales) que suele dar lugar a
malentendidos), aprovecho para dejar constancia de esta última
efeméride, con la que al tiempo me despido a la espera de mejorar de lo
mío.

::: {.blogger-post-footer}
Comer, hablar, amar. www.blogbruselas.com
:::
:::

[[Publicado el
]{.screen-reader-text}[09/02/2009](../../index.html?p=239)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../blog/2010/04/30/index.html?author=2){.url .fn .n}]{.author
.vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Artes](../../blog/category/artes/index.html),
[Comunicación y
marketing](../../blog/category/comunicacion-y-marketing/index.html),
[Humor](../../blog/category/humor/index.html)]{.cat-links}[[[12
comentarios[ en Gilipollismo viral en la Grand
Place]{.screen-reader-text}]{.dsq-postid
dsqidentifier="239 http://www.blogbruselas.com/2009/02/gilipollismo-viral-en-la-grand-place.html"}](../../index.html?p=239#comments)]{.comments-link}

[¿Otra huelga en la STIB?](../../index.html?p=238) {#otra-huelga-en-la-stib .entry-title}
--------------------------------------------------

::: {.entry-content}
Después de una semana de locos en la que no me ha dado tiempo ni a
escribir una entrada para el blog, heme aquí dispuesto a darle a la
tecla con renovados ánimos.

Volviendo hoy del [trabajo](http://www.solvay.edu/mba), tras pasar media
horita disfrutando del frío y del aguacero, he escuchado una
conversación de las que tienen miga: el chofer hablando con un
representante sindical y discutiendo la conveniencia o no de hacer una
huelga salvage (textualmente de "grève sauvage", aunque también se
podría traducir por asilvestrada) en la [STIB](http://www.stib.be/).

De lo que no he podido enterarme es del asunto, pero algo han dicho de
los asientos... Con un poco de suerte la hacen un día que no tenga yo
que ir a ningún lado, que con esto de que me está subiendo el verdismo
me dejan más tirado que una paraguaya cada vez que dejan de dar
servicio.

A propósito, [me la ha vuelto a jugar la
máquin](http://comerhablaramar.blogspot.com/2008/12/pesadilla-en-stib-street-mobib.html)a
y se ha quedado sin cargarme los viajes en la tarjeta MOBIB. Lo peor es
que perdí 20 minutos con los agentes de la STIB en la estación para que
al final me dijeran que ellos no podían hacer nada (con el papeleo ya
rellenado). Mantengo mi recomendación de seguir con los billetitos de
papel, que dan menos problemas.

::: {.blogger-post-footer}
Comer, hablar, amar. www.blogbruselas.com
:::
:::

[[Publicado el
]{.screen-reader-text}[09/02/2009](../../index.html?p=238)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../blog/2010/04/30/index.html?author=2){.url .fn .n}]{.author
.vcard}]{.byline}[[Categorías ]{.screen-reader-text}[Gran
Bruselas](../../blog/category/gran-bruselas/index.html)]{.cat-links}[[[1
comentario[ en ¿Otra huelga en la
STIB?]{.screen-reader-text}]{.dsq-postid
dsqidentifier="238 http://www.blogbruselas.com/2009/02/%c2%bfotra-huelga-en-la-stib.html"}](../../index.html?p=238#comments)]{.comments-link}

Navegación de entradas {#navegación-de-entradas .screen-reader-text}
----------------------

::: {.nav-links}
[Página anterior](../93/index.html){.prev .page-numbers} [[Página
]{.meta-nav .screen-reader-text}1](../../index.html){.page-numbers}
[...]{.page-numbers .dots} [[Página ]{.meta-nav
.screen-reader-text}93](../93/index.html){.page-numbers} [[Página
]{.meta-nav .screen-reader-text}94]{.page-numbers .current} [[Página
]{.meta-nav .screen-reader-text}95](../95/index.html){.page-numbers}
[...]{.page-numbers .dots} [[Página ]{.meta-nav
.screen-reader-text}141](../141/index.html){.page-numbers} [Página
siguiente](../95/index.html){.next .page-numbers}
:::
:::
:::
:::

::: {.site-info}
[Creado con WordPress](https://es.wordpress.org/)
:::
:::
