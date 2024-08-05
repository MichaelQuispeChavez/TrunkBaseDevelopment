# 📈 Propuesta para la Gestión de Código en Microservicios usando Trunk Based Development (TBD)

Mi propuesta para implementar **Trunk Based Development (TBD)** en los microservicios del proyecto PRS se basa en la adopción de prácticas ágiles y una estructura de ramas clara y eficiente. A continuación, detallo la propuesta para la estructuración y gestión del código fuente.

## 🌳 Propuesta de Estructuración de Ramas

**Trunk Based Development** es una metodología que enfatiza la integración continua y mantiene una única rama principal de integración. Esta propuesta establece cómo aplicar TBD en el desarrollo de microservicios para asegurar una entrega continua y de alta calidad.

### 🌟 Estructura de Ramas

1. **Rama Principal (Trunk)**
   - **`main`**: Esta es la rama central del proyecto y debe estar siempre en un estado desplegable y estable. Todas las nuevas funcionalidades, correcciones y mejoras se integran en esta rama, la cual es el punto de referencia para el despliegue continuo.

2. **Ramas de Funcionalidad (Feature)**
   - **`feature/nombre-funcionalidad`**: Se crean a partir de la rama `main` para desarrollar nuevas características o mejoras. Al completar una funcionalidad, se realiza una revisión mediante pull request y, una vez aprobada, se fusiona de vuelta a `main`.

3. **Ramas de Hotfix**
   - **`hotfix/nombre-correccion`**: Se utilizan para aplicar correcciones críticas en producción. Estas ramas se generan a partir de `main` y, después de solucionar el problema, se realiza una revisión y fusión de vuelta a `main`.

### 📜 Buenas Prácticas

1. **Integración Continua**
   - Los cambios se integran en `main` de manera frecuente y continua. Esto ayuda a evitar conflictos y asegura que la rama principal siempre esté lista para el despliegue.

2. **Mensajes de Commit Convencionales**
   - Se utilizan mensajes de commit siguiendo el estándar de Commits Convencionales. Esto facilita la comprensión del historial del proyecto y la gestión de versiones. Ejemplos:
     - `feat: agregar funcionalidad de creación de ingresos`
     - `fix: corregir error crítico en la función de listado de ingresos`

3. **Pull Requests (PR)**
   - Todas las ramas de funcionalidad y hotfix deben ser revisadas mediante pull requests antes de ser fusionadas en `main`. Esto asegura una revisión exhaustiva del código y mejora la calidad del producto final.

4. **Pruebas Automatizadas**
   - Se ejecutan pruebas automatizadas con cada commit y pull request para garantizar que el código cumpla con los requisitos y esté libre de errores.

5. **Versionamiento Semántico**
   - Se aplica el versionamiento semántico para las versiones de lanzamiento. Los tags se siguen del formato `vX.Y.Z`, donde:
     - `X` representa la versión principal,
     - `Y` la versión menor,
     - `Z` el número de corrección.
