# Entrega Examen Parcial — Politécnico Open World (POW)

## 1. Datos de identificación

* **Institución:** Instituto Politécnico Nacional — ESCOM
* **Unidad de Aprendizaje:** Desarrollo de Aplicaciones Móviles Nativas
* **Grupo:** 7CV4

### Integrantes

| Integrante              | Boleta     | Usuario GitHub                                       |
| ----------------------- |------------| ---------------------------------------------------- |
| Diego Mendieta González | 2024630077 | [@D1EGX10](https://github.com/D1EGX10)               |
| Sofía Ortega García     | 2024630517 | [@sofiaortegar01](https://github.com/sofiaortegar01) |

---

## 2. Objetivo de la entrega

La entrega documenta dos contribuciones individuales realizadas sobre el proyecto **Politécnico Open World**, cada una mediante su propio Pull Request, acompañadas de pruebas, evidencias y revisión técnica por pares.

### Contribución de Diego Mendieta González

Implementar retroalimentación visual para identificar el slot seleccionado dentro del inventario durante el modo historia.

La modificación permite que el jugador identifique visualmente el slot desbloqueado que está seleccionando mediante un indicador verde.

### Contribución de Sofía Ortega García

Implementar un mecanismo de navegación de salida seguro y accesible dentro del modo de exploración libre (Free Roam) en `WorldMapScreen.kt`.

La modificación incorpora un botón de salida, un diálogo modal de confirmación y soporte de accesibilidad mediante `contentDescription`.

---

## 3. Alcance

### Contribución de Diego

**Incluido:**

* Estado del slot seleccionado.
* Selección de slots desbloqueados.
* Actualización visual de la selección en el HUD.
* Restablecimiento de la selección al cerrar el inventario.
* Pruebas funcionales, de regresión, navegación/estado, accesibilidad y compatibilidad.

**Fuera de alcance:**

* Cambios en la capacidad del inventario.
* Modificación de las reglas de las llaves.
* Cambios en otros modos de juego.
* Cambios no relacionados con la selección visual de slots.

### Contribución de Sofía

**Incluido:**

* Integración de un `IconButton` con icono `ArrowBack`.
* Diálogo modal de confirmación mediante `AlertDialog`.
* Confirmación para regresar al menú principal.
* Opción para continuar explorando.
* Soporte de accesibilidad mediante `contentDescription`.
* Reutilización del callback existente `onNavigateToMainMenu`.

**Fuera de alcance:**

* Cambios en la arquitectura MVVM.
* Modificaciones de otras pantallas.
* Cambios en la lógica general del modo Free Roam no relacionados con la navegación de salida.

---

## 4. Issue y Pull Requests

### Diego Mendieta González

**Issue #1 — Visual feedback for inventory slot selection**

[Ver Issue #1](https://github.com/D1EGX10/PolitecnicoOpenWorld/issues/1)

**PR #175 — feat: add visual feedback for inventory slot selection**

[Ver Pull Request #175](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/175)

* **Repositorio:** `gabrielhuav/PolitecnicoOpenWorld`
* **Fork:** `D1EGX10/PolitecnicoOpenWorld`
* **Rama:** `feature/inventory-slot-selection`
* **Base SHA:** `7ed32539`
* **SHA funcional probado:** `caae27c3`
* **SHA final de entrega:** `f039d547`

### Sofía Ortega García

**PR #159 — feat(map): add exit navigation button with confirmation dialog**

[Ver Pull Request #159](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/159)

* **Repositorio:** `gabrielhuav/PolitecnicoOpenWorld`
* **Fork:** `sofiaortegar01/PolitecnicoOpenWorld`
* **Rama:** `fix/free-roam-exit-navigation`
* **Rama académica:** `entrega-examen`
* **Base SHA:** `7ed325393f82872c2be94ff2ada46948efa19152`
* **SHA final de la funcionalidad:** `ebe4a27ee36b270026ef7175b810f789632de4ea`

---

## 5. Matriz de pruebas y QA

### Diego

La matriz completa se encuentra en:

[docs/pruebas.md](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/175/changes/f039d5477baab04d95d0206be2f9ee288b2f7e9d#diff-7fa88b078aed25186e1568d8a0d73937629cc9dbe2c37ecbebba22d640e39503)

Casos ejecutados:

| ID     | Tipo                     | Resultado |
| ------ | ------------------------ | --------- |
| INV-01 | Happy path               | PASS      |
| INV-02 | Alterno / límite         | PASS      |
| INV-03 | Regresión                | PASS      |
| INV-04 | Navegación / estado      | PASS      |
| INV-05 | Accesibilidad            | PASS      |
| INV-06 | Compatibilidad / entorno | PASS      |

**Resultado:** 6 PASS, 0 defectos abiertos.

## 6. Evidencias

### Evidencias de Diego

**Antes — comportamiento original sin retroalimentación visual:**

https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/175/changes/f039d5477baab04d95d0206be2f9ee288b2f7e9d#diff-90fd2787a3f140f76cd6c53c6c84b33419ee5d107a4608b48d52e1765dac0c05

**Después — selección visual implementada y ejecución de QA:**

https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/175/changes/f039d5477baab04d95d0206be2f9ee288b2f7e9d#diff-3cf9e4afb0a3352dd4b43e2390d70c784de3530b80c499bdbddf87ee677a777c

## 7. Entornos de prueba

### Diego

* **Dispositivo:** Samsung Galaxy S24+
* **Modelo:** SM-S926B
* **Sistema operativo:** Android 16
* **API:** 36.1
* **Versión funcional probada:** `caae27c3`

### Sofía

* **Dispositivo:** Emulador Pixel 7
* **API:** 37
* **Orientación:** Horizontal
* **Versión funcional:** `ebe4a27ee36b270026ef7175b810f789632de4ea`

---

## 8. Checks de integración

El Pull Request de Diego está sujeto al workflow:

[`.github/workflows/pr-quality-gate.yml`](https://github.com/gabrielhuav/PolitecnicoOpenWorld/blob/main/.github/workflows/pr-quality-gate.yml)

El Quality Gate contempla:

* Build Android en modo Debug.
* Pruebas unitarias de `app`.
* Pruebas de `shared`.
* Validación de nombres de pruebas KMP.
* Detekt.
* JDK 21.
---

## 9. Revisión técnica por pares

### Revisión realizada por Diego a Sofía

Diego revisó el [PR #159](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/159).

Se revisó `WorldMapScreen.kt` y se reprodujo el caso **TC01** en el emulador.

La revisión verificó:

* Apertura correcta del `AlertDialog`.
* Bloqueo de interacción con el fondo mientras el diálogo está activo.
* Confirmación y cancelación de la acción.
* Exposición correcta de `contentDescription` mediante TalkBack.

La observación fue registrada en la conversación del PR.

### Revisión realizada por Sofía a Diego

Sofía revisó el [PR #175](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/175).

La revisión reprodujo los casos **INV-01** e **INV-02**.

Se verificó:

* Selección de un slot desbloqueado.
* Aparición del indicador visual verde.
* Cambio del indicador al seleccionar otro slot.
* Conexión entre el estado de selección y la presentación del HUD.

La observación fue registrada en la conversación del PR.

---

## 10. Bitácora — Diego Mendieta González

### Commits de implementación

| SHA        | Descripción                               |
| ---------- | ----------------------------------------- |
| `b4ac3018` | `feat: add selected inventory slot state` |
| `09647963` | `feat: add inventory slot selection`      |
| `66b9145b` | `fix: reset inventory slot selection`     |
| `55a86d95` | `feat: connect inventory slot selection`  |
| `caae27c3` | `feat: highlight selected inventory slot` |

### Commit de QA

| SHA        | Descripción                       |
| ---------- | --------------------------------- |
| `f039d547` | `docs: add inventory QA evidence` |

### Casos ejecutados

* INV-01
* INV-02
* INV-03
* INV-04
* INV-05
* INV-06

Todos finalizaron con **PASS**.

### Revisión por pares

[Revisión realizada al PR #159](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/159)

---

## 11. Herramientas de IA utilizadas

Las herramientas de IA fueron utilizadas como apoyo al desarrollo y documentación. Cada integrante revisó y verificó la información y los cambios correspondientes a su contribución.

### Diego Mendieta González

**ChatGPT**

Utilizado como apoyo para:

* Planificación de la implementación.
* Análisis y revisión de cambios.
* Organización de la documentación de QA.
* Redacción y revisión de documentación técnica.
* Preparación de la entrega académica.

**Gemini**

Utilizado como apoyo para:

* Redacción y revisión de documentación.
* Organización de contenido técnico.
* Apoyo en tareas relacionadas con la preparación de la entrega.

**Claude**

Utilizado como apoyo de programación para:

* Análisis de código.
* Apoyo durante la implementación.
* Revisión de cambios relacionados con la funcionalidad.

### Sofía Ortega García

**Gemini**

Utilizado como apoyo para:

* Estructuración de la matriz de casos de prueba de QA.
* Redacción técnica en inglés de la plantilla del Pull Request.
* Organización del índice de entrega académica.

---

## 12. Conclusiones

La entrega documenta dos contribuciones individuales realizadas sobre el proyecto **Politécnico Open World**, cada una con su correspondiente Pull Request, Issue o trazabilidad de cambio, matriz de pruebas, evidencias y revisión técnica por pares.

La contribución de Diego implementa retroalimentación visual para la selección de slots del inventario y fue verificada mediante seis casos de QA en un Samsung Galaxy S24+ con Android 16 / API 36.1.

La contribución de Sofía implementa navegación de salida en Free Roam mediante un botón de salida y un diálogo de confirmación, incluyendo soporte para TalkBack y pruebas de compatibilidad en un emulador Pixel 7 con API 37.

Las evidencias y matrices de prueba se mantienen vinculadas a las ramas correspondientes para conservar la trazabilidad de las versiones probadas.

---

## 13. Referencias

* [Repositorio original — gabrielhuav/PolitecnicoOpenWorld](https://github.com/gabrielhuav/PolitecnicoOpenWorld)
* [Fork de Diego — D1EGX10/PolitecnicoOpenWorld](https://github.com/D1EGX10/PolitecnicoOpenWorld)
* [Fork de Sofía — sofiaortegar01/PolitecnicoOpenWorld](https://github.com/sofiaortegar01/PolitecnicoOpenWorld)
* [Issue #1 — Inventory slot selection](https://github.com/D1EGX10/PolitecnicoOpenWorld/issues/1)
* [PR #175 — Inventory slot selection](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/175)
* [PR #159 — Free Roam exit navigation](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/159)
* [Matriz QA de Diego](https://github.com/gabrielhuav/PolitecnicoOpenWorld/pull/175/changes/f039d5477baab04d95d0206be2f9ee288b2f7e9d#top)
* [Matriz QA de Sofía](https://github.com/sofiaortegar01/PolitecnicoOpenWorld/blob/entrega-examen/PolitecnicoOpenWorld/docs/pruebas.md)
