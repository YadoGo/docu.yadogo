---
sidebar_label: 'Gitflow Commands'
sidebar_position: 3
---

GitFlow es una estrategia de ramificación de Git que se utiliza comúnmente en proyectos de desarrollo de software. Es una metodología para gestionar ramas y flujos de trabajo en un repositorio Git, lo que ayuda a mantener una estructura organizada y facilita la colaboración entre desarrolladores. A continuación, te proporcionaré los pasos básicos para implementar GitFlow en un proyecto:

1. **Iniciar un repositorio Git:** Si aún no tienes un repositorio Git, crea uno en la plataforma de alojamiento que prefieras (por ejemplo, GitHub, GitLab o Bitbucket). Inicia el repositorio con un archivo `README.md` y un archivo `.gitignore` para evitar incluir archivos innecesarios en el control de versiones.

2. **Configurar GitFlow:** Asegúrate de tener GitFlow instalado en tu sistema. Puedes instalarlo utilizando un administrador de paquetes como Homebrew (en macOS) o mediante descarga directa. Una vez instalado, inicializa GitFlow en el repositorio:

   ```bash
   git flow init
   ```

   Esto configurará las ramas principales utilizadas en GitFlow: `develop` para el desarrollo en curso y `master` para reflejar la producción estable.

3. **Flujo de trabajo:** El flujo de trabajo de GitFlow involucra dos ramas principales: `develop` y `master`, junto con otras ramas temporales. Los cambios nuevos se realizan en una rama temporal y luego se integran en las ramas principales.

   - `master`: Representa la versión del código en producción, es decir, la rama estable y lista para el despliegue en producción.
   - `develop`: Es la rama que contiene las últimas características y correcciones que se han completado y se encuentran en pruebas para ser lanzadas en la próxima versión.
   - Ramas temporales:
     - `feature`: Para agregar nuevas características. Se crean desde `develop` y se fusionan nuevamente en `develop` cuando están listas.
     - `release`: Cuando `develop` alcanza un estado estable y se va a preparar una nueva versión, se crea una rama de lanzamiento. Desde esta rama, solo se permiten correcciones de errores. Una vez que está lista para ser lanzada, se fusiona tanto en `master` como en `develop`.
     - `hotfix`: Si surge una corrección crítica en producción, se crea una rama de hotfix desde `master`, se corrige el problema y luego se fusiona en `master` y `develop`.

4. **Crear y trabajar con ramas:** Cuando empieces a trabajar en una nueva funcionalidad, crea una rama de `feature` desde `develop`:

   ```bash
   git flow feature start nombre_de_la_funcionalidad
   ```

   Realiza tus cambios y, una vez completada la funcionalidad, finaliza la rama:

   ```bash
   git flow feature finish nombre_de_la_funcionalidad
   ```

5. **Lanzar una versión:** Cuando hayas realizado suficientes cambios en la rama `develop` y estés listo para lanzar una nueva versión, crea una rama de `release`:

   ```bash
   git flow release start 1.0.0
   ```

   Realiza las pruebas necesarias, corrige problemas si los hay y, cuando esté lista para ser lanzada, finaliza la rama de `release`:

   ```bash
   git flow release finish 1.0.0
   ```

6. **Corregir problemas en producción:** Si surge un problema crítico en la rama `master`, puedes crear una rama de `hotfix` para corregirlo:

   ```bash
   git flow hotfix start nombre_del_hotfix
   ```

   Realiza la corrección, finaliza la rama de `hotfix` y asegúrate de fusionarla tanto en `master` como en `develop`:

   ```bash
   git flow hotfix finish nombre_del_hotfix
   ```

7. **Publicar ramas:** No olvides que después de crear una rama (feature, release o hotfix), debes publicarla en el repositorio remoto para que otros miembros del equipo puedan colaborar:

   ```bash
   git push origin nombre_de_la_rama
   ```

Recuerda que GitFlow es una guía, y algunos equipos pueden adaptarlo para satisfacer sus necesidades específicas. Asegúrate de comunicarte con tu equipo y seguir las prácticas establecidas por tu organización para garantizar una colaboración fluida y eficiente.
