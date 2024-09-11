## Examen UF1306

# Análisis, revisión y solución de errores en desarrollo web.

Utilizando la herramienta otorgada por el navegador Chrome “LIGHTHOUSE” detectar errores de rendimiento, carga, velocidad, etc… dentro del proyecto facilitado.

- Previo al rediseño de los puntos siguientes, la comprobación es que el sitio es efectivo, se busca cumplir con algunas recomendaciones,
  pero muchas de ellas van del lado del servidor.

![Primer choque contra Lighthouse](src/images/Lighthouse.png 'LightHouse luego de retoques para cumplir con las consignas del ejercicio.')

# 1- Clonar el repositorio de GitHub: https://github.com/Thibor82/uf1306

Hecho. Estos son los pasos:

```sh

git add .
git commit -m "1er Commit. Ya con fotos para migración de Repo"
git branch -M main
git remote add origin https://github.com/AlejandroCaldi/examen4.git
git push -u origin main

```

- Probar, testear, detectar y anotar errores y posibles mejoras. (Por ejemplo: Redimensionamiento de las imágenes, posteo de mensajes, reescalado, secciones faltantes…)

  - La llamada a scripts está mal:

    ```sh
        <script src="scripts.js"></script>
    ```

    ... se cambia por:

    ```sh
        <script src="script.js"></script>
    ```

  - Reescalado y reorientación de las imagenes.

    El tamaño de las mismas es excesivo y están invertidas. Se arregla por GIMP.

    Esto precisa además, recambio en el código por el cambio de formato del archivo de imagen.
    Así mismo creamos una clase para que las imagenes queden centradas.
    Reducimos a 480 por 480 todas las imagenes.

    ```sh
        .centrado{
            display: flex;
            flex-direction: row;
            justify-content: center;
        }
    ```

    ```sh

        <div class="centrado">
            <img src="product1.webp" alt="Producto 1">
        </div>

    ```

3- Solucionar dichos errores

    + Ver Punto anterior.

4- Añadir secciones legales.

    + Agregado.

5- Rediseño de la pagina

6- Nueva comprobación de rendimiento.

- El rendimiento mejora tras agregar meta con descripción del sitio:

```sh

 <meta name="description" content="B2B de eletrónica. Un sitio pensado para gente que busca artículos de electrónica recomendados
    por influencers y youtubers asociados con el tema.">
```

El resultado es:

![Tras mejorar SEO](Lighthouse2.png 'A Lighthouse parece alcanzarle que agregue el meta a los efectos de SEO.')

- La accesibilidad acusa falta de contraste, pero eso puede o bien ser relativo o bien referirse al banner, o bien ser modificado en el
  restyling del sitio.

- la minificación del código de JAvascript valdría de poco, y en todo caso lo haríamos cuando esté terminado el trabajo en javascript.

* Agregado de target="\_blank" en el link de la política de cookies:

```sh
    href="https://textos-legales.edgartamarit.com/" target="_blank">plantilla de política de cookies web gratis</a>
```

7- Cambiar el proyecto a Astro y comprobar el rendimiento, analizar diferencias de resultados.
