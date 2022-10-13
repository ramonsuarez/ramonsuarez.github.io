::: {#page .hfeed .site}
[Saltar al
contenido](../../../../../index.html?p=242#content){.skip-link
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
::: {#primary .content-area}
::: {#main .site-main role="main"}
¿Encontré la solución a mi problema de RAID en Ubuntu? {#encontré-la-solución-a-mi-problema-de-raid-en-ubuntu .entry-title}
======================================================

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

::: {.yarpp-related .yarpp-related-none}
Parece que no hay ningún artículo relacionado en Blog Bruselas
:::
:::

::: {.author-info}
Publicado por {#publicado-por .author-heading}
-------------

::: {.author-avatar}
![](http://1.gravatar.com/avatar/df8036046c12f28446f55958f197ed7d?s=56&d=blank&r=pg){.avatar
.avatar-56 .photo width="56" height="56"
srcset="http://1.gravatar.com/avatar/df8036046c12f28446f55958f197ed7d?s=112&d=blank&r=pg 2x"}
:::

::: {.author-description}
### Ramón Suárez {#ramón-suárez .author-title}

Soy un español que tiene la suerte de llevar disfrutando Bruselas desde
septiembre de 2003. Llegué para un trabajo temporal, como tantos, y
acabé quedándome. Este blog comenzó como una aventura personal para ir
transformándose poco a poco en una especie de diario o [guía de
Bruselas](../../../../../index.html), abierta a otros autores y en la
que tratamos de mostrar cosas que hacer y ver en esta pequeña gran
ciudad, cada uno con nuestra visión personal. En los ratos ocupados soy
un profesional del marketing y la estrategia de negocios en Internet.
Como no, también he comenzado un blog profesional sobre temas de
[marketing y empresariado en Internet](http://ramonsuarez.com). Podéis
encontrarme en Twitter con estas dos cuentas que muestran dos perfiles
perfiles: [\@blogbruselas](http://twitter.com/blogbruselas) y
[\@ramonsuarez](http://twitter.com/ramonsuarez). **Sí tienes preguntas
sobre Bruselas es mejor que las hagas en la página de [Blog Bruselas en
Facebook](http://www.facebook.com/blogbruselas)**. Somos más de mil y
tendrás muchas más personas que podrán ayudarte. Si quieres ponerte en
contacto conmigo para colaborar con el blog, enviar información o
hacerte esponsor de [Blog Bruselas](../../../../../index.html), manda un
correo electrónico a blogbruselas arrobado en gmail con un puntito com.
[Ver todas las entradas de Ramón
Suárez](../../../../2010/04/30/index.html?author=2){.author-link}
:::
:::

[[Publicado el
]{.screen-reader-text}[12/02/2009](../../../../../index.html?p=242)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../../../2010/04/30/index.html?author=2){.url .fn
.n}]{.author .vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Informática](../../../../category/informatica/index.html)]{.cat-links}

::: {#disqus_thread}
::: {#dsq-content}
-   ::: {#dsq-comment-322}
    ::: {#dsq-comment-header-322 .dsq-comment-header}
    [Héctor]{#dsq-author-user-322}
    :::

    ::: {#dsq-comment-body-322 .dsq-comment-body}
    ::: {#dsq-comment-message-322 .dsq-comment-message}
    Ya te tenia preocupado ya 😀\
    Y ahora hasta que encuentres otro problema y vuelta a empezar!
    :::
    :::
    :::

-   ::: {#dsq-comment-323}
    ::: {#dsq-comment-header-323 .dsq-comment-header}
    [dragonfly]{#dsq-author-user-323}
    :::

    ::: {#dsq-comment-body-323 .dsq-comment-body}
    ::: {#dsq-comment-message-323 .dsq-comment-message}
    No he entendido mucho pero eso de tener dos discos en espejo me
    parece una buenísima idea
    :::
    :::
    :::

-   ::: {#dsq-comment-324}
    ::: {#dsq-comment-header-324 .dsq-comment-header}
    [Comer, hablar, amar]{#dsq-author-user-324}
    :::

    ::: {#dsq-comment-body-324 .dsq-comment-body}
    ::: {#dsq-comment-message-324 .dsq-comment-message}
    \@Hector: pues no he tardado ni un día y ya tengo más de uno.

    \@dragonfly: en teoría sí, en la práctica todavía no te puedo
    decir...
    :::
    :::
    :::

-   ::: {#dsq-comment-325}
    ::: {#dsq-comment-header-325 .dsq-comment-header}
    [Sandel]{#dsq-author-user-325}
    :::

    ::: {#dsq-comment-body-325 .dsq-comment-body}
    ::: {#dsq-comment-message-325 .dsq-comment-message}
    Cómo aprendo de expresiones hispano-españolas aquí 🙂 Por qué no
    creas un tag "coñ ..." para encontrarlos más fácilmente? Me imagino
    la gente que aterriza por aquí buscando que comer en Bruselas!!
    :::
    :::
    :::

-   ::: {#dsq-comment-326}
    ::: {#dsq-comment-header-326 .dsq-comment-header}
    [Charlotte Harris]{#dsq-author-user-326}
    :::

    ::: {#dsq-comment-body-326 .dsq-comment-body}
    ::: {#dsq-comment-message-326 .dsq-comment-message}
    Creo que entendi más el Polaco, que tu entrada, pero bueno...\
    Pero a mi me sacas del windows Xp, y me pierdo!
    :::
    :::
    :::

-   ::: {#dsq-comment-327}
    ::: {#dsq-comment-header-327 .dsq-comment-header}
    [Comer, hablar, amar]{#dsq-author-user-327}
    :::

    ::: {#dsq-comment-body-327 .dsq-comment-body}
    ::: {#dsq-comment-message-327 .dsq-comment-message}
    A las pruebas me remito: está solucionado 🙂
    :::
    :::
    :::

-   ::: {#dsq-comment-1677}
    ::: {#dsq-comment-header-1677 .dsq-comment-header}
    [hellboy]{#dsq-author-user-1677}
    :::

    ::: {#dsq-comment-body-1677 .dsq-comment-body}
    ::: {#dsq-comment-message-1677 .dsq-comment-message}
    Ante la muerte de un disco hay que recordar que se tiene un ultimo
    recurso antes de darse por vencido: mandar el dispositivo a
    recuperar a una empresa especializada.

    En estos momentos las que estan trabajando mejor y con precios muy
    competitivos son ONDATA y ONRETRIEVAL.

    Son rapidos y eficaces. Una garantia...
    :::
    :::
    :::
:::
:::

Navegación de entradas {#navegación-de-entradas .screen-reader-text}
----------------------

::: {.nav-links}
::: {.nav-previous}
[[Anterior]{.meta-nav aria-hidden="true"} [Entrada
anterior:]{.screen-reader-text} [Beta Group el 3 de marzo en la
ULB]{.post-title}](../../../../../index.html?p=241)
:::

::: {.nav-next}
[[Siguiente]{.meta-nav aria-hidden="true"} [Entrada
siguiente:]{.screen-reader-text} [¿Gran quedada
bloggero-bruselo-hispano-belga?]{.post-title}](../../../../../index.html?p=243)
:::
:::
:::
:::
:::

::: {.site-info}
[Creado con WordPress](https://es.wordpress.org/)
:::
:::
