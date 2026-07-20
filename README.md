# VIUDA NEGRA PROJECT — Pruebas de Software sobre InvenTree

<p align="center">
  <img src="https://img.shields.io/badge/InvenTree-1.3.0-3B72CB?style=for-the-badge&logo=django&logoColor=white" alt="InvenTree 1.3.0" />
  <img src="https://img.shields.io/badge/Python-Django-2D79C7?style=for-the-badge&logo=python&logoColor=white" alt="Python Django" />
  <img src="https://img.shields.io/badge/Docker-Devcontainer-0db7ed?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Black--box%20tests-PE%20%2B%20AVL%20%2B%20TD%20%2B%20TS-0F62FE?style=for-the-badge" alt="Black-box tests" />
</p>

<p align="center">
  Proyecto académico del curso <strong>Pruebas de Software</strong> (UNSA-EPIS) aplicado sobre <strong>InvenTree</strong>, sistema de gestión de inventario open source. El equipo <strong>Viuda Negra</strong> ejecutó el ciclo completo de aseguramiento de calidad: pruebas unitarias, pruebas funcionales de caja negra, pruebas de integración con CI/CD, pruebas de sistema y pruebas de aceptación (UAT).
</p>

<p align="center">
  <a href="#resumen-ejecutivo">Resumen ejecutivo</a> ·
  <a href="#repositorios-del-proyecto">Repositorios</a> ·
  <a href="#artefactos-de-github-utilizados">Artefactos GitHub</a> ·
  <a href="#entregables-del-hito-2">Entregables Hito 2</a> ·
  <a href="#hito-3-completado">Hito 3</a> ·
  <a href="#índice-detallado-de-la-wiki">Índice de la Wiki</a>
</p>

---

## Resumen ejecutivo

<table>
  <tr>
    <td valign="top" width="50%">

### Qué se hizo en el Hito 2

- Re-ejecución de **451 tests unitarios** del repositorio oficial sobre los módulos `part`, `stock`, `order` y `build` (97.1% de éxito, 59% de cobertura parcial).
- Diseño de **75 casos de prueba funcionales** de caja negra (PE, AVL, TD, TS) cubriendo 9 funcionalidades; ejecución manual real de **52 casos** sobre una instancia local desplegada.
- Construcción de una **suite funcional automatizada** (Playwright + `requests`) de **433 casos** distribuidos en 6 módulos, con **86% de cobertura total** (objetivo del curso: 85% — cumplido).
- Documentación de **10 defectos** encontrados durante la ejecución funcional y unitaria manual.
- Elaboración del **Plan de Pruebas de Integración** mapeando el pipeline CI/CD oficial de InvenTree (40 casos INT-001 a INT-040).

### Qué se hizo en el Hito 3

- **Pruebas de Integración**: re-ejecución del pipeline CI/CD oficial (15 jobs) sobre el fork del equipo — **100% de jobs PASS**, cobertura global combinada **85.3%** (objetivo 85% ✅), 2 defectos menores.
- **Pruebas de Sistema**: 5 suites (73 casos) — **69 PASS / 4 FAIL (94.52%)**, 4 defectos de sistema catalogados (DEF-ST-01 a 04).
- **Pruebas de Aceptación (UAT)**: 8 subprocesos de negocio (55 casos) — **50 PASS / 5 FAIL (91%)**, 5 defectos de negocio catalogados (DEF-UAT-01 a 05).
- Documentación técnica de CI/CD y consolidación final en la Wiki (14 páginas) y el GitHub Page.

    </td>
    <td valign="top" width="50%">

### Vista rápida

| Aspecto | Detalle |
| --- | --- |
| Sistema bajo prueba | InvenTree v1.3.0 |
| Pruebas unitarias (repo oficial) | 451 ejecutados, 97.1% PASS |
| Pruebas funcionales (manual, ejecutadas) | 52 — 50 PASS / 2 FAIL |
| Pruebas funcionales (suite automatizada) | 433 casos / 6 módulos — 86% cobertura |
| Pruebas de integración (Hito 3) | 15 jobs CI — 100% PASS, 85.3% cobertura |
| Pruebas de sistema (Hito 3) | 73 casos — 69 PASS / 4 FAIL (94.52%) |
| Pruebas de aceptación / UAT (Hito 3) | 55 casos — 50 PASS / 5 FAIL (91%) |
| Defectos documentados (Hito 2) | 10 |
| Defectos documentados (Hito 3) | 11 (2 integración + 4 sistema + 5 aceptación) |
| Gestión | Issues + Projects + Wiki (14 páginas) + Page |

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
    <td>Sitio público con 4 páginas: <code>index.html</code> (presentación del proyecto y de InvenTree), <code>documentacion.html</code> (arquitectura técnica), <code>pruebas.html</code> (análisis del sistema de testing de InvenTree) e <code>historia.html</code> (línea de tiempo del proyecto desde 2019).</td>
  </tr>
  <tr>
    <td><strong>GitHub Wiki</strong></td>
    <td><a href="https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/">VIUDA_NEGRA_PROJECT/wiki</a></td>
    <td>14 páginas con el plan e informes de los 4 tipos de prueba del curso (unitarias, funcionales, integración, sistema y aceptación). Numeración con cero a la izquierda (<code>01.</code>, <code>02.</code>, <code>02.1.</code> … <code>10.</code>). Ver índice detallado más abajo.</td>
  </tr>
  <tr>
    <td><strong>GitHub Project</strong></td>
    <td><a href="https://github.com/users/jrolando19/projects/4">Project #4</a></td>
    <td>Tablero de planificación y seguimiento de las tareas de los Sprints, vinculado a los Issues de diseño, ejecución y documentación de pruebas.</td>
  </tr>
  <tr>
    <td><strong>GitHub Issues</strong></td>
    <td><a href="https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/issues">VIUDA_NEGRA_PROJECT/issues</a></td>
    <td>Incidencias registradas durante el Hito 2 y el Hito 3 (defectos y tareas de diseño/documentación), trazables a los informes de la Wiki.</td>
  </tr>
  <tr>
    <td><strong>GitHub Actions (proyecto original)</strong></td>
    <td><a href="https://github.com/inventree/InvenTree/actions">InvenTree/actions</a></td>
    <td>Pipeline de CI/CD oficial (<code>qc_checks.yaml</code>, 691 líneas) usado como base del Plan y re-ejecutado en el fork del equipo durante el Hito 3 (15 jobs, 100% PASS).</td>
  </tr>
</table>


## Entregables del Hito 2

Los cinco entregables completados y cerrados en el Hito 2, con enlace directo a su ubicación en la Wiki:

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
| Ubicación en Wiki | [01. Plan de Pruebas Unitarias](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/01.-Plan-de-Pruebas-Unitarias) · [02. Informe Pruebas Unitarias](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/02.-Informe-Pruebas-Unitarias) · [02.1. Informe Pruebas Unitarias en Linux](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/02.1.-Informe-Pruebas-Unitarias-en-Linux) |

### 2. Pruebas funcionales — Plan, Diseño y 3 Informes de Ejecución

Diseño inicial de 75 casos de prueba de caja negra (CPF-001 a CPF-009) aplicando Partición de Equivalencia, Análisis de Valores Límite, Tabla de Decisión y Transición de Estados, con ejecución real de 52 de ellos sobre una instancia InvenTree desplegada localmente (Docker + PostgreSQL 15).

| Informe (Wiki) | Módulos | Casos | Resultado |
| --- | --- | --- | --- |
| [04.1. Informe de Pruebas Funcionales 1](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/04.1.-Informe-de-Pruebas-Funcionales-1) | Login/Autenticación + Gestión de Partes | 15 | 15/15 PASS (100%) |
| [04.2. Informe de Pruebas Funcionales 2](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/04.2.-Informe-de-Pruebas-Funcionales-2) | Stock Items + Transferencias | 17 | 16/17 PASS (94.1%) |
| [04.3. Informe de Pruebas Funcionales 3](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/04.3.-Informe-de-Pruebas-Funcionales-3) | Purchase Order + Build Order | 20 | 19/20 PASS (95%) |
| **Total ejecutado (informes 1-3)** | 5 módulos | **52** | **50 PASS / 2 FAIL — 96.2%** |

> El diseño completo (75 casos) está documentado en [03. Plan de Pruebas Funcionales](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/03.-Plan-de-Pruebas-Funcionales).

#### Suite automatizada por módulo (`tests/funcionales/`)

A partir de este plan manual, el equipo construyó una suite de automatización en Python (Playwright para UI/Chromium headless + `requests` para API, Basic Auth) que **amplía la cobertura de casos por módulo**, organizada en un script por módulo dentro de `tests/funcionales/`:

| Archivo | Módulo cubierto | Casos (IDs) |
| --- | --- | --- |
| `test_part_inventree_suite.py` | Partes (TC-P), Categorías (TC-CAT), BOM (TC-BOM) | 110 |
| `test_stock_inventree_suite.py` | Stock Items y transferencias | 99 |
| `test_order_inventree_suite.py` | Purchase Order (TC-PO), Sales Order (TC-SO), Return Order (TC-RO) | 100 |
| `test_build_inventree_suite.py` | Build Order (TC-BO) | 63 |
| `test_users_inventree_suite.py` | Usuarios y permisos | 44 |
| `test_company_inventree_suite.py` | Proveedores / Company (TC-SUP) | 17 |
| **Total suite automatizada** | 6 módulos | **433** |

**Coverage medido por módulo (ejecución real de la suite):**

| Módulo | Coverage |
| --- | --- |
| `stock` | 85% |
| `order` | 85% |
| `part` | 87% |
| `build` | 87% |
| `company` | 87% |
| `users` | 87% |
| **TOTAL (part+stock+order+build+company+users)** | **86%** (objetivo del curso: 85% — ✅ cumplido) |

### 3. Defectos documentados (Hito 2)

| Origen | Severidad Media | Severidad Baja/Info |
| --- | --- | --- |
| Pruebas unitarias | 0 | 3 (D-01, D-02, D-03 — atribuibles a entorno local) |
| Informe Funcional 1 (Login/Partes) | 1 (DEF-01) | 3 (DEF-02, DEF-03, DEF-04) |
| Informe Funcional 2 (Stock) | 1 (DEF-03) | 2 (DEF-01, DEF-02) |
| Informe Funcional 3 (PO/Build) | 1 (DEF-PO-01) | 0 |

El patrón más relevante encontrado en las pruebas funcionales: la API de InvenTree no valida límites superiores en operaciones de cantidad — transferencias de stock que exceden lo disponible (DEF-03 del Informe 2) y recepciones de Purchase Order que exceden lo pedido (DEF-PO-01 del Informe 3) — devolviendo HTTP 200/201 en lugar de HTTP 400. **Este mismo patrón reaparece en el Hito 3** (ver DEF-ST-02 y DEF-UAT-02 más abajo), confirmando que no fue corregido en la versión evaluada.

### 4. Plan de Pruebas de Integración

Documento que mapea las 6 capas de integración del sistema (ORM↔BD real, API↔Modelos+Cobertura, Backend↔Cliente Python oficial, Sistema de Plugins↔Core Django, Migraciones↔Múltiples motores de BD, Frontend React↔API Backend vía Playwright E2E) tomando como base directa el pipeline real `qc_checks.yaml` (12+ jobs, 691 líneas) y `frontend.yaml` del repositorio oficial. Identifica 40 casos de integración (INT-001 a INT-040) ya existentes en los `test_api.py` del proyecto. **Este plan se ejecutó en el Hito 3** (ver sección siguiente).

| Detalle | Valor |
| --- | --- |
| Casos de integración mapeados | 40 (INT-001 a INT-040) |
| Métodos de test de integración identificados | 452+ en los `test_api.py` de 8 módulos (`part`, `stock`, `order`, `build`, `company`, `plugin`, `users`, `common`) |
| Jobs del CI oficial mapeados | 12 (`coverage`, `postgres`, `mysql`, `python`, `migration-tests`, `migrations-checks`, `schema`, `code-style`, `typecheck`, `zizmor`, + jobs de `frontend.yaml`) |
| Estrategia de integración elegida | Incremental Top-Down, CI-Driven (sin escribir tests nuevos — re-ejecución de los existentes) |
| Ubicación en Wiki | [05. Plan de Pruebas de Integración](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/05.-Plan-de-Pruebas-de-Integraci%C3%B3n) |

### 5. Implementación del proceso de pruebas con CI/CD

- **GitHub Actions**: el pipeline de referencia (`qc_checks.yaml`) del repositorio original fue estudiado job por job en el Hito 2 y re-ejecutado sobre el fork del equipo en el Hito 3 (15 jobs, 100% PASS).
- **GitHub Issues**: registro de defectos y tareas, trazables a un caso de prueba (TC-xx) o requisito (RF-xx).
- **GitHub Projects**: tablero de seguimiento de los Sprints.
- **GitHub Wiki**: 14 páginas de documentación viva del proceso de pruebas.
- **GitHub Page**: sitio público con la sección "Pruebas" mostrando enlaces directos a cada archivo de test del repositorio original, el pipeline de CI/CD resumido visualmente y la cobertura estimada por módulo.

---

## Hito 3 (completado)

El Hito 3 cierra el ciclo de aseguramiento de calidad del curso: se re-ejecutó el Plan de Integración, se diseñó y ejecutó el Plan de Pruebas de Sistema, y se diseñó y ejecutó el Plan de Pruebas de Aceptación (UAT), los tres ya publicados con resultados reales en la Wiki.

### 6. Informe de Pruebas de Integración

Re-ejecución del pipeline CI/CD oficial de InvenTree (`qc_checks.yaml` + `frontend.yaml`) sobre el fork del equipo en GitHub Actions.

| Detalle | Valor |
| --- | --- |
| Jobs de CI ejecutados | 15 (`paths-filter`, `code-style`, `typecheck`, `schema`, `coverage`, `postgres`, `mysql`, `python`, `migration-tests`, `migrations-checks`, `import_export`, `zizmor`, `[frontend] build/firefox/chromium`) |
| Resultado global | **100% de jobs en PASS** |
| Métodos de integración API verificados | 452+ (`test_api.py` de los 8 módulos) |
| Versiones legacy de BD migradas con éxito | 5 (v0.10.0, v0.11.0, v0.13.5, v0.16.0, v0.17.0) |
| Tiempo total del pipeline (paralelo) | 16 min 40 s (job más lento: `chromium`) |
| Defectos encontrados | DEF-01 (Media — race condition UI en Chromium al refrescar filtros de categorías) · INF-02 (Baja — test flaky en Firefox por latencia) |
| Ubicación en Wiki | [06. Informe de Pruebas de Integración](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/06.-Informe-de-Pruebas-de-Integracion) |

**Cobertura de código consolidada:**

| Capa del sistema | Cobertura alcanzada | Umbral mínimo | Estado |
| --- | --- | --- | --- |
| Backend Core Apps (`part`, `stock`, `order`) | 88.5% | 85.0% | ✅ Aprobado |
| Backend General (middlewares/config) | 91.2% | 85.0% | ✅ Aprobado |
| Migraciones de base de datos | 52.0% | 40.0% | ✅ Aprobado |
| Frontend (React web) | 71.4% | 68.0% | ✅ Aprobado |
| **Cobertura global combinada** | **85.3%** | **85.0%** | ✅ **Aprobado** |

### 8. Informe de Pruebas de Sistema

Ejecución de 5 suites de sistema de extremo a extremo contra un entorno Docker + PostgreSQL, pobladas con datos base estandarizados (`system_test_base.yaml`).

| Suite | Casos | PASS | FAIL | Resultado |
| --- | --- | --- | --- | --- |
| Suite 1 — Login y Catálogo de Partes | 10 | 10 | 0 | 100% |
| Suite 2 — Stock Items y Ubicaciones | 17 | 16 | 1 | 94.1% |
| Suite 3 — Categorías y Proveedores | 14 | 14 | 0 | 100% |
| Suite 4 — Órdenes de Compra y Fabricación (BOM) | 20 | 19 | 1 | 95% |
| Suite 5 — Roles, Perfiles y Permisos | 12 | 10 | 2 | 83.3% |
| **TOTAL CONSOLIDADO** | **73** | **69** | **4** | **94.52%** |

**Defectos de sistema catalogados:**

| ID | Componente | Severidad | Descripción |
| --- | --- | --- | --- |
| DEF-ST-01 | API / BOM | Alta | Permite registrar referencias con caracteres especiales excesivos en el serializador de BOM |
| DEF-ST-02 | API / Order | Media | El endpoint de recepción de PO permite sobre-recepción de insumos sin control de saldo |
| DEF-ST-03 | API / Users | Baja | Evasión de validación: se puede asignar número de serie en partes no trackeables |
| DEF-ST-04 | API / Stock | Baja | Permite procesar transferencias físicas redundantes hacia el mismo origen/destino |

> Ubicación en Wiki: [07. Plan de Pruebas de Sistema](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/07.-Plan-de-Pruebas-de-Sistema) · [08. Informe de Pruebas de Sistema](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/08.-Informe-de-Pruebas-de-Sistema)

### 10. Informe de Pruebas de Aceptación (UAT)

Pruebas de aceptación manuales de caja negra sobre la interfaz web (Chrome/Firefox), organizadas en 8 subprocesos de negocio (SP-1 a SP-8).

| Subproceso | Prioridad | Casos | PASS | FAIL | % Éxito |
| --- | --- | --- | --- | --- | --- |
| SP-1: Gestión de Catálogo y Partes | Alta | 8 | 7 | 1 | 87.5% |
| SP-2: Control y Movimiento de Stock | Alta | 8 | 5 | 3 | 62.5% |
| SP-3: Ciclo de Órdenes de Compra | Alta | 8 | 7 | 1 | 87.5% |
| SP-4: Ciclo de Órdenes de Venta | Alta | 8 | 8 | 0 | 100% |
| SP-5: Control de Órdenes de Fabricación | Alta | 8 | 8 | 0 | 100% |
| SP-6: Gestión de Empresas (Proveedores/Clientes) | Media | 5 | 5 | 0 | 100% |
| SP-7: Control de Acceso, Roles y Permisos | Media | 5 | 5 | 0 | 100% |
| SP-8: Emisión de Reportes y Etiquetas PDF | Media | 5 | 5 | 0 | 100% |
| **TOTAL CONSOLIDADO** | | **55** | **50** | **5** | **91.00%** |

**Defectos de negocio catalogados:**

| ID | Subproceso | Severidad | Descripción |
| --- | --- | --- | --- |
| DEF-UAT-01 | SP-1 | Crítica | La UI permite registrar dos partes distintas con el mismo IPN/SKU |
| DEF-UAT-02 | SP-2 | Crítica | El modal de transferencia de stock acepta cantidades superiores al saldo disponible |
| DEF-UAT-03 | SP-2 | Media | El alta de stock acepta cantidad inicial en cero, creando lotes "fantasma" |
| DEF-UAT-04 | SP-2 | Baja | Permite transferir stock hacia la misma ubicación de origen (no-op registrado) |
| DEF-UAT-05 | SP-3 | Media | Permite emitir ("Place Order") una orden de compra sin líneas de insumos |

> Ubicación en Wiki: [09. Plan de Pruebas de Aceptación](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/09.-Plan-de-Pruebas-de-Aceptaci%C3%B3n) · [10. Informe de Pruebas de Aceptación](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/10.-Informe-de-Pruebas-de-Aceptaci%C3%B3n)

### Suites de automatización propias (`tests/integracion/`, `tests/sistema/`)

Además de los informes anteriores (basados en el pipeline oficial de InvenTree y en ejecución manual/scripts propios), el equipo mantiene en el repositorio del fork una suite complementaria de automatización en Python (`requests` contra la API real) con IDs de caso propios, que amplía la trazabilidad técnica:

| Archivo | Enfoque | Casos (IDs) |
| --- | --- | --- |
| `test_integracion_inventree_suite.py` | Puntos de contacto puntuales entre dos módulos (order↔stock, build↔stock, stock↔tracking) | 14 (INT-01 a INT-04 + ST-010) |
| `test_sistema_golden_path_inventree_suite.py` | Flujo de negocio completo de punta a punta | 34 (GP-01 a GP-05) |
| `test_sistema_seguridad_inventree_suite.py` | Control de acceso transversal a toda la API (auth, permisos, tokens) | 13 (SEC-01 a SEC-08) |
| `test_sistema_desempeno_inventree_suite.py` | Tiempos de respuesta de endpoints críticos | 5 (PERF-01 a PERF-05) |
| **Total suite complementaria** | 4 archivos | **66** |

---

## Índice detallado de la Wiki

| # | Página | Contenido |
| --- | --- | --- |
| — | [Home](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki) | Bienvenida del equipo |
| 01 | [Plan de Pruebas Unitarias](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/01.-Plan-de-Pruebas-Unitarias) | Alcance, glosario, módulos del backend, registro de riesgos técnicos, estrategia y comandos de `invoke dev.test` |
| 02 | [Informe Pruebas Unitarias](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/02.-Informe-Pruebas-Unitarias) | Resultados de 451 tests ejecutados, cobertura por archivo, catálogo de defectos D-01 a D-03, tests más lentos |
| 02.1 | [Informe Pruebas Unitarias en Linux](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/02.1.-Informe-Pruebas-Unitarias-en-Linux) | Resultados de los tests ejecutados, cobertura por archivo, catálogo de defectos en Linux |
| 03 | [Plan de Pruebas Funcionales](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/03.-Plan-de-Pruebas-Funcionales) | Los 75 casos CPF-001 a CPF-009 con técnicas PE/AVL/TD/TS y matriz de trazabilidad |
| 04.1 | [Informe de Pruebas Funcionales 1](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/04.1.-Informe-de-Pruebas-Funcionales-1) | Ejecución Login + Partes — 15/15 PASS |
| 04.2 | [Informe de Pruebas Funcionales 2](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/04.2.-Informe-de-Pruebas-Funcionales-2) | Ejecución Stock Items + Transferencias — 16/17 PASS |
| 04.3 | [Informe de Pruebas Funcionales 3](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/04.3.-Informe-de-Pruebas-Funcionales-3) | Ejecución Purchase Order + Build Order — 19/20 PASS |
| 05 | [Plan de Pruebas de Integración](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/05.-Plan-de-Pruebas-de-Integraci%C3%B3n) | Mapeo completo del pipeline CI/CD oficial, 40 casos INT-001 a INT-040, registro de riesgos, RACI del equipo |
| 06 | [Informe de Pruebas de Integración](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/06.-Informe-de-Pruebas-de-Integracion) | Resultados reales: 15 jobs CI, 100% PASS, 85.3% cobertura global, defectos DEF-01/INF-02 |
| 07 | [Plan de Pruebas de Sistema](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/07.-Plan-de-Pruebas-de-Sistema) | Diseño de las 5 suites de sistema end-to-end |
| 08 | [Informe de Pruebas de Sistema](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/08.-Informe-de-Pruebas-de-Sistema) | Resultados reales: 73 casos, 69 PASS / 4 FAIL, defectos DEF-ST-01 a 04 |
| 09 | [Plan de Pruebas de Aceptación](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/09.-Plan-de-Pruebas-de-Aceptaci%C3%B3n) | Diseño de los 8 subprocesos de negocio (SP-1 a SP-8) y técnicas de caja negra aplicadas |
| 10 | [Informe de Pruebas de Aceptación](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/wiki/10.-Informe-de-Pruebas-de-Aceptaci%C3%B3n) | Resultados reales UAT: 55 casos, 50 PASS / 5 FAIL, defectos DEF-UAT-01 a 05 |

---

## Equipo

Según consta en el Plan de Pruebas de Integración (Wiki, página 05):

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
3. **Para ver el avance y las tareas de los Sprints** → [GitHub Project](https://github.com/users/jrolando19/projects/4).
4. **Para ver los defectos y tareas registradas** → [GitHub Issues](https://github.com/jrolando19/VIUDA_NEGRA_PROJECT/issues).
5. **Para ejecutar las pruebas localmente** → clona el fork [InvenTree-VIUDANEGRA](https://github.com/jrolando19/InvenTree-VIUDANEGRA) y sigue las instrucciones de despliegue con Docker del [repositorio original](https://github.com/inventree/InvenTree).
6. **Drive de los documentos** → [Google Drive Hito 2](https://drive.google.com/drive/u/1/folders/1Ovb5tQkqdMinPjdED7dTXPFBhfEnd6sq).

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
    <td>Automatización de pruebas de interfaz (Chromium/Firefox headless)</td>
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
