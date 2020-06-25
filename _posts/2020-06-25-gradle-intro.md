---
layout: post
title: Gradle
date:   2020-06-25 02:02
tags: build tools
description: Instalación y ejemplo
---

Gradle es una herramienta de construcción automática, generalmente usada para construir proyectos Java y definir sus dependencias. En este tutorial aprenderemos a instalar Gradle, realizaremos un sencillo ejemplo y lo ejecutaremos para validar su funcionamiento.

## Instalación

1. Como pre-requisito para la versión actual de Gradle (6.5) es necesario contar con Java JDK o JRE versión 8 o superior. Esto lo puedes validar con el comando `java -version`

{% highlight bash %}
{% raw %}
#java -version
java version "1.8.0_221"
Java(TM) SE Runtime Environment (build 1.8.0_221-b11)
Java HotSpot(TM) 64-Bit Server VM (build 25.221-b11, mixed mode)
{% endraw %}
{% endhighlight %}

2. Descargar la distribución directamente de la pagina oficial de [Gradle](https://gradle.org/releases/). La distribución incluirá: source, binarios, documentación y ejemplos.

3. Extraer el archivo **zip**, colocarlo dentro de una ruta especifica, setear la variable de entorno `GRADLE_HOME` apuntando a la ruta donde colocamos **Gradle.**

4. Agregar **%GRADLE_HOME%/bin** a la variable de entorno `PATH`

>Nota: Para validar la correcta instalación puedes ejecutar el comando `gradle -v`
{: .note}

{% highlight bash %}
{% raw %}
#gradle -v                                                                                            
------------------------------------------------------------
Gradle 6.5
------------------------------------------------------------

Build time:   2020-06-02 20:46:21 UTC
Revision:     a27f41e4ae5e8a41ab9b19f8dd6d86d7b384dad4

Kotlin:       1.3.72
Groovy:       2.5.11
Ant:          Apache Ant(TM) version 1.10.7 compiled on September 1 2019
JVM:          1.8.0_221 (Oracle Corporation 25.221-b11)
OS:           Windows 10 10.0 amd64
{% endraw %}
{% endhighlight %}