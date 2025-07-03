# EventNow - Prueba Técnica Integral

## 🎯 Descripción del Proyecto

EventNow es una empresa ficticia que desea crear un portal web para que sus usuarios puedan:

1. **Buscar eventos:** Los usuarios deben poder consultar un listado de eventos disponibles, filtrarlos o seleccionarlos según sus preferencias. Esto puede incluir búsqueda por nombre, ciudad, fecha u otros criterios relevantes.

2. **Reservar entradas:** Una vez que el usuario seleccione un evento, debe poder completar un formulario de reserva donde ingrese sus datos personales y la cantidad de entradas que desea reservar, con las validaciones necesarias para garantizar que la información sea correcta y completa.

3. **Gestionar sus reservas:** Los usuarios deben tener la posibilidad de visualizar todas las reservas realizadas, organizadas de manera clara (por ejemplo, por fecha o por evento). Esta funcionalidad incluye listar los eventos reservados y los detalles de cada reserva.

4. **Recibir notificaciones seguras:** La aplicación debe permitir mostrar mensajes claros de éxito o error durante el proceso de reserva, notificando al usuario sobre el estado de sus acciones. Además, debe garantizar que las notificaciones y mensajes sean seguros, evitando problemas como ataques de inyección de código (XSS) y asegurando que los datos se manejen de manera confiable.

Como parte de esta prueba técnica, deberás construir una versión inicial del portal donde los usuarios puedan:

- Capturar reservas de eventos a través de un formulario en React.
- Enviar esas reservas al backend (API REST desarrollada en Python).
- Visualizar las reservas almacenadas mediante plantillas Jinja2.

## ✅ Objetivo

Construir una aplicación funcional que integre React, Python (Flask) y Jinja2 con el siguiente flujo:

1. **Formulario de reserva (React):**
   - Selección de evento.
   - Ingreso de datos personales.
   - Validaciones en el frontend.
   - Envío de la reserva mediante API REST.

2. **Backend (Flask):**
   - API REST para recibir las reservas.
   - Almacenamiento temporal de las reservas.
   - Renderizado de las reservas mediante Jinja2 en una ruta específica.

## ✅ Estructura del Proyecto Sugerida

```
/project-root
|-- backend/                  # Flask backend
|   |-- app.py                # Flask app with API and Jinja2 views
|   |-- reservations.json     # (Optional) File for storing reservations
|   |-- templates/            # Jinja2 templates
|       |-- base.html         # Base template
|       |-- reservations.html # Template for listing reservations
|-- src/                      # React source code
|   |-- components/           # React components
|   |   |-- EventReservationForm.jsx  # Event reservation form component
|   |-- MainApp.jsx           # Main React component
|   |-- main.js               # React entry point
|-- static/                   # Directory for compiled React build
|   |-- js/
|-- README.md                 # This instruction file
```

## ✅ Instrucciones Generales

Al finalizar tu prueba, deberás documentar explícitamente en tu README o en un archivo separado:

- Qué requisitos no funcionales de calidad (según la norma ISO 25010) aplicaste durante tu implementación.
- Por qué los consideraste necesarios.
- Cómo los llevaste a cabo (ejemplos de código, técnicas, decisiones).

Esto es obligatorio y forma parte de la evaluación.

Los detalles sobre cómo implementar las validaciones, qué validaciones adicionales incluir, qué mostrar exactamente en las búsquedas o en las vistas de reservas, así como la experiencia del usuario final, se dejan a tu criterio.

Este aspecto de la prueba evalúa tu capacidad propositiva, creatividad en el diseño funcional, y sentido común para plantear soluciones adecuadas y usables. Se valoran especialmente las propuestas que aporten claridad, buena experiencia de usuario y facilidad de uso.

1. Crea un formulario en React que permita reservar entradas para un evento.
2. Desarrolla un backend en Flask que exponga:
   - Una API REST para recibir reservas.
   - Una vista Jinja2 para mostrar todas las reservas guardadas.
3. Las reservas deben almacenarse de forma temporal en memoria o en un archivo JSON.
4. La vista Jinja2 debe mostrar los datos organizados y ordenados.
5. Asegúrate de utilizar técnicas básicas de seguridad como el escapado de variables en Jinja2.

## ✅ Requisitos Técnicos

- React debe encargarse únicamente de la captura de datos.
- Flask debe encargarse del API REST y del renderizado con Jinja2.
- El frontend de React debe enviarse al backend precompilado como archivos estáticos.
- React y Flask deben mantenerse en entornos separados: Flask con Python y React con Node.js. El backend de Flask debe ser el único servidor en ejecución, que expone la API y sirve los archivos precompilados de React.

## ✅ Requisito Adicional

Deberás incluir un script (en Bash, Python o Node.js) que automatice el proceso de:

1. Instalación de dependencias del backend (Flask).
2. Instalación de dependencias del frontend (React).
3. Compilación del frontend (React build).
4. Integración automática del build del frontend en el backend.
5. Lanzamiento del backend (Flask).

Este script debe permitir a cualquier evaluador ejecutar la aplicación completa con un solo comando.



- Entrega el proyecto con la estructura completa.
- Incluye un README con instrucciones claras para:
  - Instalar dependencias.
  - Ejecutar el backend.
  - Ejecutar y compilar el frontend.
  - Integrar el build de React al backend.
- Documenta cualquier decisión técnica relevante.

## ✅ Consideraciones Importantes

- Flask y React utilizan entornos de ejecución independientes:
  - Flask usa Python (`venv` + `pip`).
  - React usa Node.js y npm.
- Flask actuará como el servidor principal que expondrá la API REST y servirá los archivos de React ya compilados.

---

Este proyecto pondrá a prueba tus habilidades en:
- React (formularios, validaciones, envío de datos a una API).
- Backend en Python (API REST y renderizado con Jinja2).
- Integración frontend-backend en un solo sistema funcional.

---

¡Éxito en la prueba!
