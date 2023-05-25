# Sobre el TP

Este repositorio corresponde a un Trabajo Practico integrador de la materia Desarrollo de Sistemas de Información Orientados a la Gestión y Apoyo a las Decisiones, también llamada PPII (Práctica Profesional II). Se desarrolló en 3 partes pero fuimos dando continuidad a la idea de mostrar datos de forma gráfica mediante una página web. Empezamos con una Landing Page estática, de diseño minimalista, que corre sobre Github Pages, mostrando una serie de gráficos generados con Tableau referidos a la pandemia Covid-19. Luego avanzamos para integrarle al proyecto una instancia de Grafana y fuimos haciendo el setup de distintas partes del sistema, dejando de lado la temática inicial y enfocándonos en brindar un espacio de experimentación para el usuario.

---

## Parte I

Análisis de datos con Dataset elegido entre varias opciones. 

- Software de Data Analysis elegido: Tableau.
- Dataset elegido: Covid-19. Link a [datos abiertos](https://data.buenosaires.gob.ar/dataset/casos-covid-19)

## Introducción

En el año 2020, la infección por el virus Covid-19 es declarado pandemia por la OMS. Nuestro país no es ajeno a la situación y comienzan a aumentar los casos. CABA, una de las provincias con mayor cantidad de población, fue una de las más afectadas en cantidad de contagios. Nos enfocaremos en analizar el número de infectados en los distintos barrios de la Ciudad.

## Objetivo

Apuntamos a realizar una comparativa de la cantidad de casos de Covid-19 en el año 2020 y 2023. Nos enfocaremos en mostrar la evolución de los casos en los distintos barrios de CABA a través del tiempo. Algunos datos para destacar en la investigación:

- Casos positivos
- Muertes
- Cantidad de casos por barrio / comuna
- Cantidad de casos por mes
- Promedio de edad de infectados
- Porcentaje de casos por género

## Desarrollo

Utilizaremos [Tableau](https://www.tableau.com/es-es) para el análisis de datos y la generación de gráficos. ~~Todo esto se verá plasmado [en una landing page (work in progress)](https://kaenovsky.github.io/enigma-dss/src/).~~

Finalmente este reporte quedó subido tanto [en Github pages](https://kaenovsky.github.io/enigma-dss/src/) como [en un subdominio](https://covid.altadata.ar) dentro de la VPS. Aclaramos que los datos del dataset no son del todo confiables ni están debidamente procesados por lo que los números finales del reporte deben ser tomados con precaución.

:: Checkpoints Parte I ::

[✅] Planificación y presentación de propuesta

[✅] Generar y exportar datos con Tableau

[✅] Setup Landing Page estática

[✅] Redacción reporte + upload

## Parte II

~~En una siguiente etapa (TP N°3), vamos a permitir al usuario interactuar con la información del dataset a través de una instancia de [Grafana](https://grafana.com/) corriendo en un servidor web.~~

🚀 Update: Quedó corriendo una primera versión demo en una VPS (Digital Ocean). La instancia es pequeña, apenas 2gb de ram. Instalamos Ubuntu server y configuramos el hardening de la misma para conectarnos por SSH. Más adelante, utilizando [nginx](https://nginx.org/en/) para el web server y redireccionamiento del tráfico, junto a la configurando los DNS desde el manager de Digital Ocean, logramos tener disponibles distintos subdominios para cada parte del proyecto. Así fue que dejamos seteada la siguiente configuración:

- Landing page general: https://altadata.ar
- Landing page covid: https://covid.altadata.ar
- Instancia grafana: https://graf.altadata.ar (con docker 🐳)

![Instancia de Grafana corriendo en VPS](./demo-grafana.png)

:: Checkpoints Parte II ::

[✅] Setup dominio

[✅] Setup VPS

[✅] Setup entorno del web server con nginx

[✅] Setup Grafana con Docker

---

Presentamos el proyecto en clase y obtuvimos el feedback para seguir mejorando:

:: Últimos checkpoints vistos en clase ::

[✅] Agregar TLS/SSL para https

[✅] Permitir Sing Up / Sign In

[✅] Mejorar dashboard de datos (demo)

---

💡 **Idea nueva:** permitir al usuario hacer su propio Dashboard.

Para lograr esto necesitamos un mini tutorial que guíe al usuario con info y datos de prueba. También es necesario dar permisos de edición a los dasboards. Agregamos items al to-do:

[✅] Permitir edición por usuario

[x] Linkear video intro a Grafana

[x] Redactar mini tutorial

[x] Actualizar landing con info para el usuario

[x] Tomar y elegir screenshots

[x] Maquetar y pushear el código 