---
layout: post
title: Spring Boot 2
date:   2020-06-29 19:15
tags: spring
description: Introducción a Spring Boot 2
---

Spring Boot es un modulo de Spring Framework, provee un **RAD** (Rapid Application Development). El cuál basa su configuración en starter templates.

1. ¿Que son los starter template?

Son un conjunto de templates que contienen todas las dependencias necesarias para una funcionalidad en concreto. Por ejemplo si necesitas crear un proyecto web básico es suficiente con agregar la dependencia `spring-boot-starter-web`, la cual incluye todo lo necesario para empezar, ademas te evitas arreglar conflictos entre las diferentes versiones de las dependencias.

>build.gradle
{:.filename}
{% highlight javascript %}
{% raw %}
dependencies {	
	implementation 'org.springframework.boot:spring-boot-starter-web'	
}
{% endraw %}
{% endhighlight %}


2. Spring boot auto configuración

La auto configuración en Spring Boot se habilita con la anotación `@EnableAutoConfiguration` , la cual escanea el classpath, busca las librerias y realiza la mejor configuración para ellas, finalmente habilitas los respectivos beans dentro del contexto.

>Nota: Auto-configuración es siempre aplicado después de los bean registrados por el usuario. Puedes revisar la lista completa [aquí] (https://docs.spring.io/spring-boot/docs/2.3.1.RELEASE/api/)


3. Servidor embebido 

Spring boot incluye el servidor de aplicaciones [Tomcat](http://tomcat.apache.org). Ésto significa que puedes correr tu aplicación desde la linea de comandos sin la necesidad de configurar una infraestructura compleja.

Tu puedes excluir Tomcat e incluir algun otro servidor si gustas. También puedes excluir por completo el uso de un servidor embebido y desplegarlo de manera tradicional en un archivo war.


4. Configuración de arranque.

Para correr la aplicación es necesario usar la anotación `@SpringBootApplication`. Esta anotación es equivalente a `@Configuration`, `@EnableAutoConfiguration`, y `@ComponentScan` juntas.
Esta anotación inicia el escaneo y configuración de todas las clases, tomando en cuenta el archivo de propiedades **/resources/application.properties**

> Nota: Las anotaciones `@Configuration`, `@EnableAutoConfiguration`, y `@ComponentScan` pertenecen a la primer versión de spring boot.

>MyApplication.java
{:.filename}
{% highlight java %}
{% raw %}
@SpringBootApplication
public class MyApplication 
{
    public static void main(String[] args) 
    {
        SpringApplication.run(Application.class, args);
    }
}
{% endraw %}
{% endhighlight %}

>application.properties
{:.filename}
{% highlight properties %}
{% raw %}
### Server port #########
server.port=8080
  
### Context root ########
server.contextPath=/home
{% endraw %}
{% endhighlight %}


Para correr la aplicación desde linea de comando ejecutar lo siguiente:

{% highlight bash %}
{% raw %}
# java -jar spring-boot-demo.jar
{% endraw %}
{% endhighlight %}