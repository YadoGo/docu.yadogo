---
sidebar_label: 'Conventional Commit'
sidebar_position: 1
---

# Conventional Commit

En el desarrollo de software, los "Conventional Commits" (Commits Convencionales) son una convención para escribir mensajes de commit que siguen un formato estructurado y consistente. Esta práctica se ha vuelto popular en proyectos de código abierto y en la comunidad de desarrollo en general debido a su claridad, legibilidad y facilidad para automatizar ciertas tareas relacionadas con el versionado del software y la generación de cambios.

## El formato de un "Conventional Commit" se compone de tres partes principales:

1. **Tipo (Type):** Representa el propósito general del cambio introducido en el commit. Los tipos más comunes incluyen:
   - **feat:** Se utiliza cuando se agrega una nueva característica al código.
   - **fix:** Se usa cuando se corrige un error o un bug.
   - **docs:** Hace referencia a cambios en la documentación del proyecto.
   - **style:** Refleja cambios que no afectan el código en sí, sino la forma en que se ve o se formatea.
   - **refactor:** Se utiliza cuando se realiza un cambio interno en el código que no agrega nuevas características ni corrige errores.
   - **test**: Representa cambios en los casos de prueba (tests) del proyecto.
   - **chore:** Indica cambios en tareas de mantenimiento, configuración, entre otros.

2. **Área (Scope) [opcional]:** Indica la parte específica del proyecto que se ve afectada por el commit. No es obligatorio, pero puede ser útil para proyectos grandes con múltiples componentes o módulos.

3. **Mensaje (Message):** Es una breve descripción del cambio realizado en el commit. Debe estar escrito en tiempo presente y en imperativo. Por ejemplo: "Agrega nueva función X" o "Corrige el cálculo de Y".

4. **Ejemplo de un Conventional Commit**
    
    A continuación, se muestra un ejemplo de cómo se vería un commit convencional:
    ```
    feat(users): 📦 Add login functionality
    ```
    En este caso, el commit agrega una nueva característica relacionada con los usuarios (users), específicamente, la funcionalidad de inicio de sesión (feat).

5. **Extensión Conventional Commit:**
    Hay una extensión para Visual Studio Code llamada [Conventional Commit](https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits) muy intuitiva que nos ayudara en los primeros días a hacerlo bien

## Recursos
- https://www.conventionalcommits.org/en/v1.0.0/
- https://carlosazaustre.es/conventional-commits
- https://gitmoji.dev/