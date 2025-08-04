# URL pública del proyecto: https://jidpruebas.github.io/cocinandocongit_g1.github.io/

## Objetivo

Aprender el flujo de trabajo colaborativo con Git y GitHub mediante un proyecto práctico en el que cada estudiante contribuya al desarrollo del proyecto.

## Descripción del taller

Cada estudiante será agregado como colaborador a este repositorio de GitHub. Este proyecto es una página web que contiene tarjetas (cards) con el nombre de distintas recetas. El objetivo de cada estudiante es crear la página individual de una receta, trabajarla en una rama, hacer un *commit* de sus cambios, subir su rama y abrir un *Pull Request* (PR). Luego, otro compañero revisará el PR y aprobará el *merge*.

## Flujo de trabajo

1. **Clonar el repositorio**:

   ```bash
   git clone https://github.com/jidpruebas/cocinandocongit_g1.github.io.git
   cd cocinandocongit_g1.github.io
   ```

2. **Crear una rama propia**:

   ```bash
   git checkout -b receta-nombre
   ```

3. **Editar archivos**: Crear un nuevo archivo HTML para tu receta dentro de la carpeta `/recetas`. Asegúrate que el nombre del archivo sea igual al botón de la receta que está en el archivo `index.html`.

4. **Verificar, agregar, confirmar y subir los cambios**:

   ```bash
   git status
   git add .
   git commit -m "feat: agregar receta de [nombre]"
   git push receta-nombre
   ```

5. **Abrir un Pull Request (PR)** en GitHub desde tu rama.

6. **Revisión cruzada**: Otro estudiante debe revisar el PR, comentar y aprobar el merge.

7. **Hacer merge en GitHub**: Se puede elegir una de estas opciones:

   - *Create a merge commit*: conserva todo el historial de la rama. (Recomendado)
   - *Squash and merge*: aplana los commits en uno solo.
   - *Rebase and merge*: inserta los commits encima del historial de `main`.

## Estrategia de ramas

Se recomienda una estrategia simple tipo **Trunk-Based Development**:

- `main`: contiene la versión estable del proyecto.
- Cada estudiante trabaja en su propia rama basada en `main`.

## Cómo simular un conflicto

1. Crear dos ramas desde `main`.
2. Modificar la misma línea (por ejemplo, en `index.html`) en ambas ramas.
3. Hacer merge de una rama en `main`.
4. Intentar mergear la segunda rama: Git debería mostrar un conflicto.

## Buenas prácticas de commits

Estructura:

```bash
<tipo>(opcional-alcance): descripción breve
```

Seguir la convención:

- `feat:` para nuevas recetas
- `fix:` para corregir errores
- `chore:` para tareas como configuración o estructura base

Recomendaciones:

- Usa verbos en infinitivo: agregar, corregir, actualizar.
- Usa minúsculas en el mensaje.
- No pongas punto final.

Ejemplo:

```bash
git commit -m "feat: agregar receta de arroz con leche"
```

