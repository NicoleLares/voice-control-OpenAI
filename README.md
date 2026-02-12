# 🤖 COSMO - Sistema de Control por Voz con OpenAI

Aplicación web desarrollada en **HTML, CSS (Bootstrap) y JavaScript** que permite controlar un sistema mediante comandos de voz utilizando la **Web Speech API** y la **API de OpenAI**.

El sistema funciona con activación por palabra clave:

> 🎙 Di **"COSMO"** para activar el reconocimiento de órdenes.

---

## 🚀 Características

- 🎤 Reconocimiento de voz en tiempo real (Web Speech API)
- 🧠 Interpretación inteligente de comandos usando OpenAI
- 🔐 API Key obtenida dinámicamente desde MockAPI
- 💤 Modo suspensión automática por inactividad
- ⚡ Activación mediante palabra clave **COSMO**
- 🎨 Interfaz moderna con Bootstrap
- 🧩 Arquitectura separada en HTML, CSS y JS
- 🔄 Uso de `async/await` y `fetch`

---

## 🗣️ Comandos Soportados

El sistema solo puede devolver exactamente uno de los siguientes comandos:

- `avanzar`
- `retroceder`
- `detener`
- `vuelta derecha`
- `vuelta izquierda`
- `90° derecha`
- `90° izquierda`
- `360° derecha`
- `360° izquierda`

Si la orden no coincide:

```
Orden no reconocida
```

---

## 🏗️ Estructura del Proyecto

```
cosmo-voice-control/
│
├── index.html
├── styles.css
└── app.js
```

---

## ⚙️ Funcionamiento del Sistema

1. Al cargar la página:
   - Se obtiene la API Key desde MockAPI
   - Se inicia el reconocimiento de voz
2. Si no hay actividad por 5 segundos:
   - El sistema entra en modo **SUSPENDIDO**
3. Si el usuario dice **"COSMO"**:
   - El sistema se activa nuevamente
4. Los comandos detectados se envían a OpenAI para validación

---

## 🔑 Obtención de API Key

La API Key se obtiene dinámicamente desde:

```
https://68e538728e116898997ee561.mockapi.io/apikey
```

Estructura esperada:

```json
[
  {
    "api_key": "sk-proj-XXXX",
    "id": "1"
  }
]
```

El sistema toma automáticamente el primer registro.

---

## 🛠️ Instalación y Uso

1. Clonar el repositorio:

```bash
git clone https://github.com/tuusuario/cosmo-voice-control.git
```

2. Abrir `index.html` en el navegador (Chrome recomendado).

3. Permitir acceso al micrófono.

---

## 🌐 Requisitos

- Navegador compatible con Web Speech API (Chrome recomendado)
- Conexión a internet
- API Key válida de OpenAI

---

## 🔐 Nota de Seguridad

⚠️ Este proyecto obtiene la API Key desde el frontend para fines académicos.

En un entorno de producción se recomienda:

```
Frontend → Backend (Node.js / Express) → OpenAI
```

Para evitar exponer la API Key públicamente.

---

## 📌 Tecnologías Utilizadas

- HTML5
- CSS3
- Bootstrap 5
- JavaScript ES6+
- Web Speech API
- OpenAI API
- MockAPI

---

## 👨‍💻 Autor

Desarrollado por **Nicole Dayana**  
2026 © Proyecto académico / experimental

---

## 📜 Licencia

Este proyecto se distribuye con fines educativos.
