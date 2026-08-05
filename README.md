# 🔍 SQL Joins Challenge - 15 Consultas Interactivas

Una aplicación web interactiva alojada en **GitHub Pages** diseñada para practicar y dominar las combinaciones relacionales (`INNER`, `LEFT`, `RIGHT` y `FULL OUTER JOIN`). 

El reto te presenta **15 ejercicios progresivos**: se te muestra la descripción del requerimiento, el esquema de la base de datos y la **tabla de resultados esperada**. Tu objetivo es redactar la consulta SQL exacta que genera dicho resultado.

🔗 **[Probar la aplicación en vivo (GitHub Pages)](https://jhoanbaez214.github.io/github.io/index.html)**

---

## 🚀 Características principales

- 🎯 **15 Retos Progresivos:** Desde combinaciones básicas de 2 tablas hasta combinaciones múltiples con agregaciones y filtrado.
- 📊 **Feedback Inmediato:** Compara en tiempo real la salida de tu consulta con el resultado esperado.
- 💡 **Esquema Visible:** Diagrama entidad-relación accesible en todo momento para referencia rápida.
- ⚡ **Sin Configuración:** Funciona 100% en el navegador gracias a SQLite/SQL.js, sin necesidad de instalar servidores de bases de datos.

---

## 🗄️ Esquema de la Base de Datos

La práctica utiliza una base de datos de un sistema de comercio electrónico simplificado con 4 tablas principales:

```text
  ┌──────────────┐       ┌──────────────┐       ┌──────────────┐
  │  Clientes    │       │   Ordenes    │       │  Productos   │
  ├──────────────┤       ├──────────────┤       ├──────────────┤
  │ cliente_id PK│───┐   │ orden_id  PK │   ┌───│ producto_idPK│
  │ nombre       │   └──<│ cliente_idFK │   │   │ nombre_prod  │
  │ email        │       │ fecha_orden  │   │   │ precio       │
  └──────────────┘       └──────────────┘   │   └──────────────┘
                               │            │
                               ▼            │
                         ┌──────────────────┐
                         │ Detalle_Ordenes  │
                         ├──────────────────┤
                         │ orden_id      FK │
                         │ producto_id   FK │
                         │ cantidad         │
                         └──────────────────┘
