# PUSH Y COMMIT

Luego de correr la *branch* de un proyecto en local y de haber realizado los cambios en el mismo, habrá que subir los cambios de dicha *branch* a la **branch de la nube** (github).

En el siguente ejemplo se cambiarán las imágenes de fondo de una sección en una página web.

* 1. Se optimizan las imágenes con un *script* de [Python]() para que cargue rápido la página sin perder calidad.
* 2. Se suben las imágenes a un CDN de **DigitalOcean** para que los recursos carguen sin que la página pese cada vez más.
* 3. Se agregan las rutas en variables dentro del archivo correspondiente de donde la página accede a los recursos: urlimages.js.
* * <img width="399" alt="image" src="https://user-images.githubusercontent.com/92232878/218879428-4eb48c8e-b167-416d-9462-6dd6a9208db0.png">
* 4. Nos vamos al archivo **B2CHero.jsx** (correspondiente a la sección de la página) y llamamos a las imagenes por medio del archivo anterior (urlimages.js), el código comentado es como estaba el archivo antes del cambio, debajo están invocadas las imagenes por medio del archivo **.js**.
* * <img width="513" alt="image" src="https://user-images.githubusercontent.com/92232878/218880425-d31bcb8b-d844-4f63-9515-e193fc0704f0.png">
* 5. Para cambiar el estilo y demás propiedades en la sección, nos vamos al archivo **.scss** correspondiente:
* * <img width="309" alt="image" src="https://user-images.githubusercontent.com/92232878/218881880-fbd7211f-3b94-4bc2-aa33-74fe80591402.png"> 
* * Notamos que la función se llama **B2C-Hero-test** (dentro del archivo **B2CHero.jsx**), nos vamos al archivo **b2c.scss** y ubicamos la referencia de mismo nombre:
* * <img width="193" alt="image" src="https://user-images.githubusercontent.com/92232878/218882054-90fa21f1-d94d-414d-8aed-348f8e81e7f3.png">
* * En la función *overlay* (má abajo) ponemos la propiedad **background**:
* * <img width="210" alt="image" src="https://user-images.githubusercontent.com/92232878/218882224-9f0e1a65-4435-41a8-afe1-e999820c76eb.png">
## Actualizar en github
* Con **git status** comprobamos los cambios realizados:
<img width="617" alt="image" src="https://user-images.githubusercontent.com/92232878/218882619-919a5d60-dfd9-4fd9-bf77-b6d31916ed17.png">
* Con **git add .** indicamos que queremos enviar todos los cambios.
* Con **git commit -m "style: images to b2c section hero"** agregamos una descripción al cambio que enviaremos.
* Con **git push origin home-carlos** indicamos que el cambio se sube a la *branch* "home-carlos".
