::: {#page .hfeed .site}
[Saltar al
contenido](../../../../../index.html?p=294#content){.skip-link
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
Problema librerías QT en Linux {#problema-librerías-qt-en-linux .entry-title}
==============================

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
]{.screen-reader-text}[09/04/2009](../../../../../index.html?p=294)]{.posted-on}[[[Autor
]{.screen-reader-text}[Ramón
Suárez](../../../../2010/04/30/index.html?author=2){.url .fn
.n}]{.author .vcard}]{.byline}[[Categorías
]{.screen-reader-text}[Informática](../../../../category/informatica/index.html)]{.cat-links}

::: {#disqus_thread}
::: {#dsq-content}
-   ::: {#dsq-comment-518}
    ::: {#dsq-comment-header-518 .dsq-comment-header}
    [Bultza]{#dsq-author-user-518}
    :::

    ::: {#dsq-comment-body-518 .dsq-comment-body}
    ::: {#dsq-comment-message-518 .dsq-comment-message}
    Gracias a ti Ramón por la mención, un abrazo y disfruta de las
    vacaciones :). No soy ningún gurú linuxero, solo un linuxero con la
    experiencia justa para seguir sobreviviendo 🙂
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
anterior:]{.screen-reader-text} [Rap macarra de
Bruselas]{.post-title}](../../../../../index.html?p=293)
:::

::: {.nav-next}
[[Siguiente]{.meta-nav aria-hidden="true"} [Entrada
siguiente:]{.screen-reader-text} [Een dag bij El Bulli (un día en El
Bulli, en flamenco y
olé)]{.post-title}](../../../../../index.html?p=295)
:::
:::
:::
:::
:::

::: {.site-info}
[Creado con WordPress](https://es.wordpress.org/)
:::
:::
