# Sobre el TP

Este repositorio corresponde a un Trabajo Practico integrador de la materia Desarrollo de Sistemas de Información Orientados a la Gestión y Apoyo a las Decisiones, también llamada PPII (Práctica Profesional II). Se desarrolló en 3 partes pero fuimos dando continuidad a la idea de mostrar datos en una página web. Empezamos con una landing minimalista corriendo en un Github Pages, mostrando una serie de gráficos generados con Tableau. Luego avanzamos para integrar también una instancia de Grafana y fuimos haciendo el setup de distintas partes del sistema, dejando de lado la temática inicial y enfocándonos en brindar un espacio de experimentación para el usuario.

---

## Parte I

Análisis de datos con Dataset elegido entre varias opciones. 

- Software de Data Analysis elegido: Tableau.
- Dataset elegido: COVID19. Link a [datos abiertos](https://data.buenosaires.gob.ar/dataset/casos-covid-19)

## Introducción

En el año 2020, la infección por el virus COVID-19 es declarado pandemia por la OMS. Nuestro país no es ajeno a la situación y comienzan a aumentar los casos. CABA, una de las provincias con mayor cantidad de población, fue una de las más afectadas en cantidad de contagios. Nos enfocaremos en analizar el número de infectados en los distintos barrios de la Ciudad.

## Objetivo

Apuntamos a realizar una comparativa de la cantidad de casos de COVID-19 en el año 2020 y 2023. Nos enfocaremos en mostrar la evolución de los casos en los distintos barrios de CABA a través del tiempo. Algunos datos para destacar en la investigación:

- Casos positivos
- Muertes
- Cantidad de casos por barrio / comuna
- Cantidad de casos por mes
- Promedio de edad de infectados
- Porcentaje de casos por género

## Desarrollo

Utilizaremos [Tableau](https://www.tableau.com/es-es) para el análisis de datos y gráficos. ~~Todo esto se verá plasmado [en una landing page (work in progress)](https://kaenovsky.github.io/enigma-dss/src/).~~

Finalmente la landing que quedó subida tanto [en Github pages](https://kaenovsky.github.io/enigma-dss/src/) como [en un subdominio](https://covid.altadata.ar) dentro de la VPS.

:: Checkpoints Parte I ::

[✅] Planificación y presentación de propuesta

[✅] Generar y exportar datos con Tableau

[✅] Setup Landing Page estática

[✅] Redacción reporte + upload

## Parte II

~~En una siguiente etapa (TP N°3), vamos a permitir al usuario interactuar con la información del dataset a través de una instancia de [Grafana](https://grafana.com/) corriendo en un servidor web.~~

🚀 Update: Quedó corriendo una primera versión demo en una VPS (Digital Ocean). Utilizando ngnix y configurando los DNS desde el manager de DO para tener distintos subdominios, dejamos seteada la siguiente configuración:

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

:: Últimos checkpoints vistos en clase ::

[✅] Agregar TSL/SSL para https

[✅] Permitir Sing Up / Sign in

[✅] Mejorar dashboard de datos

---

💡 Idea nueva: permitir al usuario hacer su panel:

Para lograr esto necesitamos un mini tutorial que guíe al usuario con info y datos de prueba. También es necesario dar permisos de edición a los dasboards. Agregamos items al to-do:

[✅] Permitir edición por usuario

[x] Linkear video intro a Grafana

[x] Redactar mini tutorial

[x] Actualizar landing con info para el usuario

[x] Tomar y elegir screenshots

[x] Maquetar y pushear el código 