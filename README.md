# Guía de estudio ISTQB CTFL v4.0

App de estudio autocontenida (un solo `index.html`, sin dependencias externas) para preparar la
certificación **ISTQB® Certified Tester Foundation Level (syllabus v4.0.1)**.

## Contenido

- **Apuntes** de los 6 capítulos del syllabus, con niveles cognitivos K1–K3.
- **Flashcards** de la terminología oficial (voltear, barajar, marcar "me la sé").
- **Simulacros**: práctica por capítulo con corrección al instante y examen cronometrado
  (40 preguntas/60 min o 20/30 min) que baraja preguntas nuevas cada vez y puntúa sobre el
  umbral real del 65%.

Todo funciona en el navegador (HTML/CSS/JS en un único fichero). No necesita servidor de
aplicación: se sirve como estático.

## Ver en local

Abre `index.html` en cualquier navegador, o sirve la carpeta:

```bash
python3 -m http.server 8080
# luego abre http://localhost:8080
```

## Despliegue (servidor propio, nginx)

Está publicada en: **https://38-242-236-14.nip.io/qa/**

El servidor sirve el fichero de forma estática desde un clon de este repo. Para actualizarla tras
un cambio en GitHub:

```bash
ssh root@38.242.236.14 'cd /var/www/qa && git pull'
```

La ruta la sirve nginx con un bloque `location /qa/` (ver `deploy/qa.nginx.conf`).

## Estructura

```
index.html            La app de estudio completa
deploy/qa.nginx.conf  Bloque nginx de referencia para servir /qa/
README.md
```
