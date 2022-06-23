#Práctica 4. Implementación de página con Azure App Service

##Creación de la página web
En [Azure portal](https://portal.azure.com/) buscamos los App Services.
![p4p1](imagenes\p4p1.png)

Seleccionamos crear.
![p4p2](imagenes\p4p2.png)

Elegimos:
- Suscripción
- Grupo de recursos: sesion4
- Nombre de la instancia, el cuál deberá ser único: restaurantepagina
- Pila del entorno de ejeción: PHP 8.0
- Región: Central US
![p4p3](imagenes\p4p3.png)

En Plan de App Service seleccionamos cambiar tamaño y elegimos Gratis F1. Los demás parámetros permanecen igual.
Seleccionamos "Revisar y crear" y luego "Crear".
![p4p5](imagenes\p4p5.png)

--------------------------------------
##Subir página a GitHub

En el [acordeón del Sherpa Jesús](https://github.com/josejesusguzman/acordeon-az900-innovaccion), buscamos en la semana 2 la práctica [Lab de Azure App Service: Sube tu página a App Service](https://github.com/josejesusguzman/lab-subir-app-service-azure) y la seleccionamos.

![p4p6](imagenes\p4p6.png)

Para copiar la carpeta que usaremos, seleccionamos "Code" y copiamos el link del repositorio.
![p4p7](imagenes\p4p7.png)

Abrimos un cmd donde vamos a descargar el repositorio y lo clonamos con _git clone_ seguido del URL que copiamos.

![p4p9](imagenes\p4p9.png)

El repositorio se copiará donde lo seleccionamos.
![p4p10](imagenes\p4p10.png)

Ahora en Visual Studio Code abrimos la carpeta de la página we y la subimos a GitHub. Usamos:
- git init
- git add . (en este caso es punto ya que la carpeta de la página se abrió directamente)
- git commit -m "first comit"
- git branch -M main
- git remote add origin _URL_
- git push -u origin main
![p4p14](imagenes\p4p14.png)
-------------------------------
##Subir la página con App Service
En nuestra instancia de App Services, en Implementación buscamos _Centro de implementación_.
![p4p11](imagenes\p4p11.png)

Seleccionamos GitHub como origen.
![p4p12](imagenes\p4p12.png)

Autorizamos la conexión entre App Service y GutHub.
![p4p13](imagenes\p4p13.png)

Seleccionamos la organización donde subimos el repositorio de la página web, así como el repositorio y la rama.
![p4p15](imagenes\p4p15.png)

En GitHub observamos que la página comenzará a implementarse.
![p4p16](imagenes\p4p16.png)

Esto podemos verlo mejor en Actions.
![p4p17](imagenes\p4p17.png)

Una vez que ha terminado de implementarse la página en GitHub seleccionamos el URL que aparece debajo de _deploy_.
![p4p18](imagenes\p4p18.png)

Nos irigirá a la página que se tenía en código.
![p4p19](imagenes\p4p19.png)

En la misma instancia de App Service que creamos tenemos el mismo link que nos aparece en GutHub, ambos nos conducen a la página que hemos creado.
![p4p20](imagenes\p4p20.png)

-------------------------------------
###Recursos creados
Al crear nuestra página web, se han creado 2 recursos:
- Plan de App Service
- App Service

![p4p21](imagenes\p4p21.png)

#### Nota personal

- git add .
- git commit -m "README añadido"
- git push origin main
- git pull origin main (si algo falla)