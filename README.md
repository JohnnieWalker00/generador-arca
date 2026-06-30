# 🔐 Generador de Certificados ARCA (ex AFIP) — Versión Premium

Esta es una herramienta **100% Client-Side** (del lado del cliente) diseñada para que estudios contables y empresas generen los certificados digitales necesarios para la Facturación Electrónica en Argentina (Web Services de ARCA).

Al funcionar completamente en el navegador sin backend, se garantiza **privacidad y seguridad absoluta**, ya que las llaves privadas nunca viajan por internet.

## ✨ Características Principales (Actualización 2026)

* **Seguridad Zero-Knowledge:** No utiliza bases de datos ni servidores (PHP/Node). Toda la criptografía se resuelve localmente mediante `forge.js`. Las llaves privadas (`.key`) jamás abandonan tu computadora.
* **UI/UX Premium:** Interfaz moderna con *Glassmorphism*, animaciones sutiles y un "Stepper" interactivo de 4 pasos que guía al usuario reduciendo la fricción técnica.
* **Drag & Drop Inteligente:** En el Paso 3, los usuarios pueden arrastrar y soltar sus archivos `.crt` y `.key` directamente sobre la pantalla para generar el PFX final.
* **Sistema de Descargas Robusto:** Preparado para funcionar 100% offline o desde un archivo local (`file://`). Utiliza Data URIs en Base64 para evitar bloqueos del navegador o problemas de renombrado de archivos (UUIDs).
* **Instructivo Imprimible a prueba de fallos:** Genera una versión para imprimir con el paso a paso detallado para el portal de ARCA. Incluye una sección de contingencia con los 5 errores más comunes y sus soluciones.

## 🚀 Cómo usarlo

1. **Paso 1 (Generar CSR):** El cliente ingresa su CUIT. El sistema autocompleta su Razón Social. Elige un Alias y genera los archivos **.csr** (solicitud) y **.key** (llave privada).
2. **Paso 2 (Portal ARCA):** El cliente sigue el instructivo desplegable para subir el `.csr` a la web oficial de ARCA y descarga el certificado **.crt**.
3. **Paso 3 (Generar PFX):** El cliente arrastra el `.crt` (de ARCA) y el `.key` (del Paso 1) a las zonas de carga para obtener el archivo definitivo **.pfx** sin contraseña.
4. **Paso 4 (Envío):** Se muestra un panel final con accesos directos de email para enviar el archivo al agente de cuenta.

## 🛠️ Tecnologías

* **HTML5 / CSS3 / JavaScript (ES6)**: 100% Vanilla. Un solo archivo `index.html` portátil.
* **[Node-Forge](https://github.com/digitalbazaar/forge)**: Implementación pura en JavaScript de herramientas criptográficas (RSA, PKCS#12, CSR).

---
*Un desarrollo de Germán Pratto para Grupo Oleum SRL*
