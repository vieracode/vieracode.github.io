---
layout: post
title: Gradle
date:   2020-06-25 02:02
description: Instalación y ejemplo
toc: false
comments: false
---

Gradle es una herramienta de construcción automática, generalmente usada para construir proyectos de Software y definir sus dependencias. En este tutorial aprenderemos a instalar Gradle, realizaremos un sencillo ejemplo y lo ejecutaremos para validar su funcionamiento.

Instalación

1. Como pre-requisito para la versión actual de Gradle (6.5) es necesario contar con Java JDK o JRE versión 8 o superior. Esto lo puedes validar con el comando java -version

2. Descargar la distribución directamente de la pagina oficial de Gradle (https://gradle.org/releases/). La distribución incluirá: source, binarios, documentación y ejemplos.

3. Extraer el archivo zip, colocarlo dentro de una ruta especifica, setear la variable de entorno GRADLE_HOME apuntando a la ruta donde colocamos Gradle.

4. Agregar GRADLE_HOME/bin a la variable de entorno PATH.

>Nota: Para validar la correcta instalación puedes ejecutar el comando gradle -v lo cual debería mostrar algo parecido a esto: