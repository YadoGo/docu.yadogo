---
sidebar_label: 'Flujo de trabajo de Gitflow'
sidebar_position: 2
---

# Flujo de trabajo de Gitflow
Gitflow es un modelo de flujo de trabajo de Git que proporciona una estructura organizada para gestionar el desarrollo de proyectos. Utiliza ramas de función y varias ramas principales para mantener un historial claro y permitir una colaboración más eficiente entre los miembros del equipo.

## Ramas main y de develop
En Gitflow, se utilizan dos ramas principales para mantener el historial del proyecto:

- **main:** Es la rama principal que almacena el historial de las versiones oficiales del proyecto. Cada vez que se complete una versión estable, se fusionará con esta rama.

- **develop:** Es la rama de integración donde se combinan las características y cambios terminados antes de realizar una nueva versión. Es a partir de esta rama que se bifurcan las ramas de función.

![img main develop](https://wac-cdn.atlassian.com/dam/jcr:a13c18d6-94f3-4fc4-84fb-2b8f1b2fd339/01%20How%20it%20works.svg?cdnVersion=1107)
Para iniciar Gitflow, primero necesitas asegurarte de tener una rama main existente. Luego, desde la rama main, creas la rama develop utilizando el siguiente comando:
```
git checkout -b develop main
```

## Ramas de feature
En Gitflow, cada nueva característica o cambio significativo se desarrolla en su propia rama de feature. Estas ramas se crean a partir de la rama develop y se fusionan nuevamente en ella una vez que la función está completa.

Para crear una nueva rama de función, puedes usar el siguiente comando:
```shell
git checkout -b feature/nombre-de-la-feature develop

```

![](https://wac-cdn.atlassian.com/dam/jcr:34c86360-8dea-4be4-92f7-6597d4d5bfae/02%20Feature%20branches.svg?cdnVersion=1107)
Trabaja en la rama de función como lo harías normalmente, realizando los cambios necesarios para la nueva característica. Una vez que hayas terminado, realiza la fusión de la rama de función en develop:

```
git checkout develop
git merge feature/nombre-de-la-feature
```


## Ramas de release
Cuando develop contiene suficientes características para una nueva versión o cuando se acerca la fecha de publicación programada, se crea una rama de release. Esta rama se utiliza para preparar la versión final antes de lanzarla.

Para crear una rama de release, utiliza el siguiente comando:
```
git checkout -b release/version-x.x.x develop
```
![](https://wac-cdn.atlassian.com/dam/jcr:8f00f1a4-ef2d-498a-a2c6-8020bb97902f/03%20Release%20branches.svg?cdnVersion=1107)
Realiza los últimos ajustes, corrección de errores y pruebas en esta rama de release. Una vez que todo está listo, fusiona la rama de release en main y develop, y etiqueta la versión:

```
git checkout main
git merge release/version-x.x.x

git checkout develop
git merge release/version-x.x.x

git tag -a version-x.x.x
```

## Ramas de corrección (Hotfix)
Las ramas de corrección, también conocidas como "hotfix", se utilizan para corregir problemas críticos en la versión actual en producción. Estas ramas se crean directamente desde main para asegurar una corrección rápida.

Para crear una rama de corrección, puedes utilizar:
```
git checkout -b hotfix/nombre-del-hotfix main
```
Una vez que hayas hecho las correcciones necesarias, fusiona la rama de corrección en main y develop, y etiqueta la versión corregida:

```
git checkout main
git merge hotfix/nombre-del-hotfix

git checkout develop
git merge hotfix/nombre-del-hotfix

git tag -a version-corregida
```

![](https://wac-cdn.atlassian.com/dam/jcr:cc0b526e-adb7-4d45-874e-9bcea9898b4a/04%20Hotfix%20branches.svg?cdnVersion=1107)

Recuerda eliminar las ramas de función y de corrección una vez que se han fusionado para mantener el repositorio limpio:

```
git branch -d feature/nombre-de-la-funcion
git branch -d hotfix/nombre-del-hotfix
```

## Recursos
- https://www.atlassian.com/es/git/tutorials/comparing-workflows/gitflow-workflow