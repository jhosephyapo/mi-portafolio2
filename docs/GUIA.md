
# Laboratorio 3: Trabajo colaborativo con repositorios remotos

**Curso:** Diseño de Interfaces de Programación Avanzado  
**Alumno:** Jhoseph Brandon Yapo Bravo · **Grupo:** A  
**Entrega:** 21/10/2026 · **Docente:** Jeisson Daniel Paredes Cano

## Objetivos

- Diferenciar *fork* y *clone*.
- Reportar y corregir errores mediante *Issues*, ramas y *Pull Requests*.
- Sincronizar el *fork* y la copia local.

## Conceptos clave

| Término | Resumen |
|---|---|
| Fork | Copia un repositorio a tu cuenta de GitHub. |
| Clone | Descarga el repositorio a tu computadora (`git clone`). |
| Issue | Reporta un problema en el repositorio original. |
| Pull Request | Propone cambios para revisión e integración. |
| origin | Remoto que apunta a tu *fork*. |

## Parte guiada: corregir el total del carrito

El README indica que el total esperado es **S/ 68.00**, pero la página muestra **S/ 43.00**. En `script.js`, `calcularTotal` suma cada precio sin considerar la cantidad. La corrección es multiplicar ambos valores:

```javascript
total = total + producto.precio * producto.cantidad;
```

### Pasos

1. Crear un *fork* del repositorio del docente en GitHub.
2. Clonar el *fork* y comprobar que `origin` apunta a tu cuenta:

   ```bash
   git clone https://github.com/TU-USUARIO/tienda-tecsup.git
   cd tienda-tecsup
   git remote -v
   ```

3. Reportar el error en **Issues** del repositorio original, indicando qué se esperaba (S/ 68.00), qué ocurre (S/ 43.00), dónde está el error (`script.js`, `calcularTotal`) y cómo reproducirlo.
4. Crear una rama y corregir el cálculo:

   ```bash
   git checkout -b fix-total-carrito
   git add script.js
   git commit -m "Corrige el calculo del total del carrito (#NUMERO)"
   git push origin fix-total-carrito
   ```

5. Abrir un *Pull Request* hacia `main` del repositorio docente. Verificar que `Files changed` muestre únicamente `script.js` y probar que el total resulte S/ 68.00.

## Tarea: segunda contribución

El segundo error está en la referencia al CSS: `estilos.css` tiene contenido correcto, pero `index.html` no lo muestra. Comparar el nombre del archivo con el atributo `href` y corregirlo.

Completar por cuenta propia el ciclo: crear un *Issue*, partir desde `main`, crear una rama, corregir y probar, hacer commit, subir la rama y abrir un PR al repositorio del docente. Cada PR debe modificar un solo archivo. Al terminar, sincronizar el *fork* en GitHub y ejecutar `git pull` en la carpeta local.

## Entregables registrados

- **Fork:** [jhosephyapo/tienda-tecsup](https://github.com/jhosephyapo/tienda-tecsup)
- **Issues:** [#389](https://github.com/jeisson-tecsup/tienda-tecsup/issues/389), [#393](https://github.com/jeisson-tecsup/tienda-tecsup/issues/393)
- **Pull Requests:** [#390](https://github.com/jeisson-tecsup/tienda-tecsup/pull/390), [#394](https://github.com/jeisson-tecsup/tienda-tecsup/pull/394)
- **Repositorio original:** [jeisson-tecsup/tienda-tecsup](https://github.com/jeisson-tecsup/tienda-tecsup)

![Pantalla principal del proyecto](../img/imangen.png)

