# 🍴 Ejercicio: Git Recipes (Git Flow)

## 🎯 Objetivos

- Practicar el flujo de trabajo Git Flow en un proyecto existente.
- Crear y trabajar en ramas paralelas.
- Resolver conflictos de merge.

> Importante: Para realizar este práctico es necesario que tengas instalado
> un IDE (por ejemplo Visual Studio Code), git y Node.js.

## ⚙️ Set up inicial

1. Realiza un fork del repositorio. A partir de este punto, se trabajará en el repositorio creado en este paso.
2. En el fork: Clonar el repositorio con 

```bash 
git clone https://github.com/<USUARIO>/git-recipes.git
cd git-recipes
code .
```

2. Inicializa la aplicación:
```bash
npm install
npm run dev
```

3. Una vez ejecutada la aplicación desde tu navegador, agregá algunas recetas y navegá entre las secciones para familiarizarte con el proyecto.


## 🌿 Parte 1 — Configurar las ramas base

1. Creá la rama `develop` a partir de `main` y realiza push en el repositorio remoto.

2. Verificá con el siguiente comando que la estructura de ramas es correcta antes de continuar:
```bash
git log --oneline --graph
```


## 📝 Parte 2 — Feature 1: Descripción de la receta

1. Desde `develop`, creá la rama `feature/description`.

2. En esta rama debés agregar un campo **Descripción** a la aplicación: un área de texto donde el usuario pueda escribir los pasos o ingredientes de la receta. Al agregar una receta se debe mostrar en la lista de recetas su descripción.

3. Verificá que la aplicación funcione correctamente: agregá una receta con descripción y corroborá que los campos pre-existentes y la descripción se muestren en la lista.

4. Hacé commit de los cambios y publicá la rama en el repositorio remoto.


## ⏱️ Parte 3 — Feature 2: Tiempo de preparación

> Importante: esta feature se desarrolla en paralelo con la anterior. Creá la rama **desde `develop`**, **no** desde `feature/description`.

1. Desde `develop`, creá la rama `feature/prep-time`.

2. En esta feature debés agregar un campo **Tiempo de preparación** a la aplicación: un campo numérico obligatorio, con mínimo 0, donde el usuario pueda indicar el tiempo en minutos. El tiempo de preparación se debe mostrar en la lista de recetas.

3. Verificá que la aplicación funcione correctamente: agregá una receta con tiempo de preparación y corroborá que los campos pre-existentes y el tiempo de preparación se muestren en la lista.

4. Hacé commit de los cambios y publicá la rama en el repositorio remoto.


## 🤺 Parte 4 — Merge y resolución de conflictos

1. Volvé a `develop` y mergeá `feature/description`.

2. Mergeá `feature/prep-time` en `develop`. Git reportará conflictos en algunos archivos.

3. Abrí cada archivo en conflicto. Vas a encontrar los marcadores `<<<<<<<`, `=======` y `>>>>>>>` indicando las versiones en conflicto. Resolvé los conflictos de forma que **ambas funcionalidades queden integradas** en el resultado final.

4. Verificá que la aplicación funciona correctamente con ambos campos presentes y funcionales.

5. Completá el merge con:
```bash
git add .
git commit
```

## 🚀 Parte 5 — Primer release

1. Mergeá `develop` en `main` y realizá push.

2. Creá un tag para marcar el release:
```bash
git tag v1.0.0
git push origin v1.0.0
```

3. Verificá con `git log --oneline --graph --all` que `main`, `develop` y el tag apuntan al mismo commit.

---

## 📖 Referencias y recursos útiles

- [Git](https://git-scm.com/book/es/v2)
- [TypeScript](https://www.w3schools.com/typescript/)
- [HTML](https://www.w3schools.com/html/)
- [Git Flow (Atlassian)](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
