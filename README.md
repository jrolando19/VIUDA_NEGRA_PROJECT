# VIUDA NEGRA PROJECT — Pruebas de Software sobre InvenTree

<p align="center">
  <img src="https://img.shields.io/badge/InvenTree-1.3.0-3B72CB?style=for-the-badge&logo=django&logoColor=white" alt="InvenTree 1.3.0" />
  <img src="https://img.shields.io/badge/Python-Django-2D79C7?style=for-the-badge&logo=python&logoColor=white" alt="Python Django" />
  <img src="https://img.shields.io/badge/Docker-Devcontainer-0db7ed?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Black--box%20tests-PE%20%2B%20AVL%20%2B%20TD%20%2B%20TS-0F62FE?style=for-the-badge" alt="Black-box tests" />
</p>

<p align="center">
  Proyecto académico del curso <strong>Pruebas de Software</strong> (UNSA-EPIS) aplicado sobre <strong>InvenTree</strong>, sistema de gestión de inventario open source. El equipo <strong>Viuda Negra</strong> ejecuta un ciclo de aseguramiento de calidad que abarca pruebas unitarias, pruebas funcionales de caja negra y la planificación de pruebas de integración con CI/CD.
</p>

<p align="center">
  <a href="#resumen-ejecutivo">Resumen ejecutivo</a> ·
  <a href="#repositorios-del-proyecto">Repositorios</a> ·
  <a href="#artefactos-de-github-utilizados">Artefactos GitHub</a> ·
  <a href="#entregables-del-hito-2">Entregables Hito 2</a> ·
  <a href="#índice-detallado-de-la-wiki">Índice de la Wiki</a>
</p>

---

## Resumen ejecutivo

<table>
  <tr>
    <td valign="top" width="50%">

### Qué se hizo en el Hito 2

- Re-ejecución de **451 tests unitarios** del repositorio oficial sobre los módulos `part`, `stock`, `order` y `build` (97.1% de éxito, 59% de cobertura parcial).
- Diseño de **75 casos de prueba funcionales** de caja negra (PE, AVL, TD, TS) cubriendo 9 funcionalidades.
- Ejecución real de **52 casos de prueba funcionales** sobre una instancia local desplegada (Login, Partes, Stock, Purchase Order, Build Order).
- Documentación de **10 defectos** encontrados durante la ejecución funcional y unitaria.
- Elaboración del **Plan de Pruebas de Integración** mapeando el pipeline CI/CD oficial de InvenTree, pendiente de ejecución en el Hito 3.

    </td>
    <td valign="top" width="50%">

### Vista rápida

| Aspecto | Detalle |
| --- | --- |
| Sistema bajo prueba | InvenTree v1.3.0 |
| Pruebas unitarias (repo oficial) | 451 ejecutados, 97.1% PASS |
| Pruebas funcionales ejecutadas | 52 — 50 PASS / 2 FAIL |
| Defectos documentados | 10 |
| Pruebas de integración | Plan listo — ejecución en Hito 3 |
| Gestión | Issues + Projects + Wiki + Page |

</td>
  </tr>
</table>

---

## Repositorios del proyecto

| Repositorio | Rol | URL |
| --- | --- | --- |
| **Repositorio de grupo** | Documentación, GitHub Page, Wiki, Issues y Projects del equipo | [github.com/jrolando19/VIUDA_NEGRA_PROJECT](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT) |
| **Repositorio de pruebas (fork)** | Fork de InvenTree donde se ejecutan las pruebas de manera local | [github.com/jrolando19/InvenTree-VIUDANEGRA](https://github.com/jrolando19/InvenTree-VIUDANEGRA) |
| **Repositorio original** | Proyecto InvenTree sobre el cual se diseñan y ejecutan las pruebas | [github.com/inventree/InvenTree](https://github.com/inventree/InvenTree) |

> El repositorio de grupo concentra la **documentación y gestión** (informes, wiki, tablero, página pública). El fork (`InvenTree-VIUDANEGRA`) es donde se clona y ejecuta InvenTree localmente vía Docker/devcontainer para correr `invoke dev.test` sin afectar el repositorio original.

---

## Artefactos de GitHub utilizados

<table>
  <tr>
    <th align="left">Artefacto</th>
    <th align="left">URL</th>
    <th align="left">Descripción</th>
  </tr>
  <tr>
    <td><strong>GitHub Page</strong></td>
    <td><a href="https://jrolando19.github.io/VIUDA_NEGRA_PROJECT/">jrolando19.github.io/VIUDA_NEGRA_PROJECT</a></td>
    <td>Sitio público con 4 páginas: <code>index.html</code> (presentación del proyecto y de InvenTree), <code>documentacion.html</code> (arquitectura técnica), <code>pruebas.html</code> (análisis del sistema de testing de InvenTree: estructura de archivos por módulo, pipeline CI/CD, cobertura estimada por módulo, enlaces directos al código fuente real en GitHub) e <code>historia.html</code> (línea de tiempo del proyecto desde 2019).</td>
  </tr>
  <tr>
    <td><strong>GitHub Wiki</strong></td>
    <td><a href="https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/">VIUDA_NEGRA_PROJECT/wiki</a></td>
    <td>9 páginas con el plan e informes de pruebas unitarias y funcionales del equipo (ver índice detallado más abajo).</td>
  </tr>
  <tr>
    <td><strong>GitHub Project</strong></td>
    <td><a href="https://github.com/users/jrolando19/projects/4">Project #4</a></td>
    <td>Tablero de planificación y seguimiento de las tareas del Sprint 2, vinculado a los Issues de diseño, ejecución y documentación de pruebas.</td>
  </tr>
  <tr>
    <td><strong>GitHub Issues</strong></td>
    <td><a href="https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/issues">VIUDA_NEGRA_PROJECT/issues</a></td>
    <td>Incidencias registradas durante el Hito 2: defectos encontrados en la ejecución funcional y unitaria, y tareas de diseño/documentación.</td>
  </tr>
  <tr>
    <td><strong>GitHub Actions (proyecto original)</strong></td>
    <td><a href="https://github.com/inventree/InvenTree/actions">InvenTree/actions</a></td>
    <td>Pipeline de CI/CD oficial (<code>qc_checks.yaml</code>, 691 líneas) tomado como base del Plan de Pruebas de Integración del equipo. Define los jobs <code>coverage</code>, <code>postgres</code>, <code>mysql</code>, <code>python</code>, <code>migration-tests</code>, <code>schema</code>, <code>zizmor</code> y los workflows complementarios <code>frontend.yaml</code> e <code>import_export.yaml</code>. Su ejecución real sobre el fork del equipo está programada para el Hito 3.</td>
  </tr>
</table>


### 1. Pruebas unitarias — Plan e Informe

Re-ejecución de la suite de pruebas unitarias oficial de InvenTree (Django TestCase + coverage.py 7.14.1 + django-slowtests) sobre un entorno local (Ubuntu 22.04 LTS sobre WSL2, Python 3.11).

| Detalle | Valor |
| --- | --- |
| Módulos ejecutados | `part`, `stock`, `order`, `build` (ejecución parcial; quedan 6+ módulos pendientes: `company`, `users`, `plugin`, `report`, `label`, `InvenTree`) |
| Total de tests ejecutados | 451 |
| Tests PASSED | 438 (97.1%) |
| Tests FAILED / ERROR | 2 FAILED + 11 ERROR — atribuibles a limitaciones del entorno local (worker Django Q2 inactivo, paths de módulo de test, fixtures de tasas de cambio no cargadas), no a bugs reales de InvenTree |
| Cobertura medida (parcial) | 59% — la cobertura oficial completa del proyecto reportada en Codecov es ~87% |
| Archivo con mayor cobertura | `stock/tests.py` — 96% |
| Archivo con menor cobertura | `build/models.py` — 34% |
| Test más lento | `test_shipment_many_items` (order) — 114.57 s, ~32% del tiempo total |
| Ubicación en Wiki | [1. Plan de Pruebas Unitarias](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/1.-Plan-de-Pruebas-Unitarias) · [2. Informe Pruebas Unitarias](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/2.-Informe-Pruebas-Unitarias) · [3. Informe Pruebas Unitarias Linux](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/2.1.-Informe-Pruebas-Unitarias-en-Linux)|

### 2. Pruebas funcionales — Plan, Diseño y 3 Informes de Ejecución

Diseño de 75 casos de prueba de caja negra (CPF-001 a CPF-009) aplicando Partición de Equivalencia, Análisis de Valores Límite, Tabla de Decisión y Transición de Estados, y ejecución real de 52 de ellos sobre una instancia InvenTree desplegada localmente (Docker + PostgreSQL 15), automatizada con Playwright (Chromium headless) y la librería `requests` (Basic Auth).

| Informe (Wiki) | Módulos | Casos | Resultado |
| --- | --- | --- | --- |
| [4. Informe de Pruebas Funcionales 1](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/4.1.-Informe-de-Pruebas-Funcionales-1) | Login/Autenticación + Gestión de Partes | 15 | 15/15 PASS (100%) |
| [4. Informe de Pruebas Funcionales 2](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/4.2.-Informe-de-Pruebas-Funcionales-2) | Stock Items + Transferencias | 17 | 16/17 PASS (94.1%) |
| [4. Informe de Pruebas Funcionales 3](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/4.3.-Informe-de-Pruebas-Funcionales-3) | Purchase Order + Build Order | 20 | 19/20 PASS (95%) |
| **Total ejecutado** | 5 módulos | **52** | **50 PASS / 2 FAIL — 96.2%** |

> El diseño completo (75 casos) está documentado en [3. Plan de Pruebas Funcionales](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/3.-Plan-de-Pruebas-Funcionales). Los módulos de BOM (8 casos) y Proveedores (7 casos) están diseñados pero su ejecución queda pendiente para el Hito 3, junto con Sales Orders, Clientes y Búsqueda Global (aún no diseñados).

### 3. Defectos documentados

| Origen | Severidad Media | Severidad Baja/Info |
| --- | --- | --- |
| Pruebas unitarias | 0 | 3 (D-01, D-02, D-03 — atribuibles a entorno local) |
| Informe Funcional 1 (Login/Partes) | 1 (DEF-01) | 3 (DEF-02, DEF-03, DEF-04) |
| Informe Funcional 2 (Stock) | 1 (DEF-03) | 2 (DEF-01, DEF-02) |
| Informe Funcional 3 (PO/Build) | 1 (DEF-PO-01) | 0 |

El patrón más relevante encontrado en las pruebas funcionales: la API de InvenTree no valida límites superiores en operaciones de cantidad — transferencias de stock que exceden lo disponible (DEF-03 del Informe 2) y recepciones de Purchase Order que exceden lo pedido (DEF-PO-01 del Informe 3) — devolviendo HTTP 200/201 en lugar de HTTP 400.

### 4. Plan de Pruebas de Integración

Documento que mapea las 6 capas de integración del sistema (ORM↔BD real, API↔Modelos+Cobertura, Backend↔Cliente Python oficial, Sistema de Plugins↔Core Django, Migraciones↔Múltiples motores de BD, Frontend React↔API Backend vía Playwright E2E) tomando como base directa el pipeline real `qc_checks.yaml` (12+ jobs, 691 líneas) y `frontend.yaml` del repositorio oficial. Identifica 40 casos de integración (INT-001 a INT-040) ya existentes en los `test_api.py` del proyecto, pendientes de re-ejecución sobre el fork del equipo en el Hito 3.

| Detalle | Valor |
| --- | --- |
| Casos de integración mapeados | 40 (INT-001 a INT-040) |
| Métodos de test de integración identificados | 452+ en los `test_api.py` de 8 módulos (`part`, `stock`, `order`, `build`, `company`, `plugin`, `users`, `common`) |
| Jobs del CI oficial mapeados | 12 (`coverage`, `postgres`, `mysql`, `python`, `migration-tests`, `migrations-checks`, `schema`, `code-style`, `typecheck`, `zizmor`, + jobs de `frontend.yaml`) |
| Estrategia de integración elegida | Incremental Top-Down, CI-Driven (sin escribir tests nuevos — re-ejecución de los existentes) |
| Ubicación en Wiki | [5. Plan de Pruebas de Integración](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/5.-Plan-de-Pruebas-de-Integraci%C3%B3n) |
| Estado del Informe de Integración | Plan de pruebas de integración más no la ejecución que sera para el Hito 3 |

### 5. Implementación del proceso de pruebas con CI/CD

- **GitHub Actions**: el pipeline de referencia (`qc_checks.yaml`) del repositorio original fue estudiado y documentado a fondo job por job; su ejecución real sobre el fork del equipo es el primer entregable técnico del Hito 3.
- **GitHub Issues**: registro de defectos y tareas, trazables a un caso de prueba (TC-xx) o requisito (RF-xx).
- **GitHub Projects**: tablero de seguimiento del Sprint 2.
- **GitHub Wiki**: 9 páginas de documentación viva del proceso de pruebas.
- **GitHub Page**: sitio público con la sección "Pruebas" mostrando enlaces directos a cada archivo de test del repositorio original, el pipeline de CI/CD resumido visualmente y la cobertura estimada por módulo.

---

## Índice detallado de la Wiki

| # | Página | Contenido |
| --- | --- | --- |
| — | [Home](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki) | Bienvenida del equipo |
| 1 | [Plan de Pruebas Unitarias](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/1.-Plan-de-Pruebas-Unitarias) | Alcance, glosario, módulos del backend, registro de riesgos técnicos, estrategia y comandos de `invoke dev.test` |
| 2 | [Informe Pruebas Unitarias](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/2.-Informe-Pruebas-Unitarias) | Resultados de 451 tests ejecutados, cobertura por archivo, catálogo de defectos D-01 a D-03, tests más lentos |
| 2 | [Informe Pruebas Unitarias en Linux](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/2.1.-Informe-Pruebas-Unitarias-en-Linux) | Resultados de los tests ejecutados, cobertura por archivo, catálogo de defectos en Linux |
| 3 | [Plan de Pruebas Funcionales](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/3.-Plan-de-Pruebas-Funcionales) | Los 75 casos CPF-001 a CPF-009 con técnicas PE/AVL/TD/TS y matriz de trazabilidad |
| 4 | [Informe de Pruebas Funcionales 1](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/4.-Informe-de-Pruebas-Funcionales-1) | Ejecución Login + Partes — 15/15 PASS |
| 4 | [Informe de Pruebas Funcionales 2](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/4.-Informe-de-Pruebas-Funcionales-2) | Ejecución Stock Items + Transferencias — 16/17 PASS |
| 4 | [Informe de Pruebas Funcionales 3](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/4.-Informe-de-Pruebas-Funcionales-3) | Ejecución Purchase Order + Build Order — 19/20 PASS |
| 5 | [Plan de Pruebas de Integración](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/5.-Plan-de-Pruebas-de-Integraci%C3%B3n) | Mapeo completo del pipeline CI/CD oficial, 40 casos INT-001 a INT-040, registro de riesgos, RACI del equipo |
| 6 | [Informe de Pruebas de Integracion](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/6.-Informe-de-Pruebas-de-Integracion) | Plan de pruebas de integración más no la ejecución que sera para el Hito 3 |

---

## Equipo

Según consta en el Plan de Pruebas de Integración (Wiki, página 5):

| Integrante | Rol |
| --- | --- |
| Ing. Robert Edison Arisaca Mamani | Docente del curso |
| Tejada Lazo, Jordy Rolando | Test Lead / Test Design |
| Hurtado Bejarano, Michael Steve | Test Analyst |
| Yare Chullunquia, Kevin Pedro | Test Analyst |
| Del Castillo Montoya, Brad Christopher | Test Architect |
| Jaita Chura, Jose Manuel | Test Design |

---

## Cómo navegar este proyecto

1. **Para ver el resumen visual del proyecto y el análisis de testing de InvenTree** → [GitHub Page](https://jrolando19.github.io/VIUDA_NEGRA_PROJECT/), sección [Pruebas](https://jrolando19.github.io/VIUDA_NEGRA_PROJECT/pruebas.html).
2. **Para revisar el diseño y los informes de pruebas en detalle** → [GitHub Wiki](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/).
3. **Para ver el avance y las tareas del Sprint** → [GitHub Project](https://github.com/users/jrolando19/projects/4).
4. **Para ver los defectos encontrados** → [GitHub Issues](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/issues).
5. **Para ejecutar las pruebas localmente** → clona el fork [InvenTree-VIUDANEGRA](https://github.com/jrolando19/InvenTree-VIUDANEGRA) y sigue las instrucciones de despliegue con Docker del [repositorio original](https://github.com/inventree/InvenTree).

---

## Tecnologías utilizadas

<table>
  <tr>
    <th align="left">Tecnología</th>
    <th align="left">Rol</th>
  </tr>
  <tr>
    <td><strong>Python / Django / DRF</strong></td>
    <td>Backend del sistema bajo prueba (InvenTree)</td>
  </tr>
  <tr>
    <td><strong>React / TypeScript</strong></td>
    <td>Frontend del sistema bajo prueba</td>
  </tr>
  <tr>
    <td><strong>PostgreSQL / SQLite / MySQL</strong></td>
    <td>Motores de base de datos soportados por InvenTree</td>
  </tr>
  <tr>
    <td><strong>Docker / Docker Compose</strong></td>
    <td>Despliegue local del sistema bajo prueba</td>
  </tr>
  <tr>
    <td><strong>Playwright</strong></td>
    <td>Automatización de pruebas de interfaz (Chromium headless)</td>
  </tr>
  <tr>
    <td><strong>requests (Python)</strong></td>
    <td>Pruebas directas sobre la API REST (Basic Auth)</td>
  </tr>
  <tr>
    <td><strong>Django TestCase + coverage.py + django-slowtests</strong></td>
    <td>Ejecución y medición de cobertura del suite unitario oficial</td>
  </tr>
  <tr>
    <td><strong>GitHub Actions, Issues, Projects, Wiki, Pages</strong></td>
    <td>Gestión, documentación y CI/CD del proceso de pruebas</td>
  </tr>
</table>
