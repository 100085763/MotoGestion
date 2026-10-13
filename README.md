# MotoGestión

**Sistema de gestión para un taller de motocicletas.**

## 1. Objetivo

Diseñar un sistema que permita organizar la información de los clientes, sus motocicletas y los servicios o reparaciones realizados en un taller, facilitando el seguimiento de cada vehículo y la consulta de su historial.

## 2. Problema que resuelve

Cuando la información de un taller se lleva en libretas o en registros dispersos, puede ser difícil localizar los datos de un cliente, identificar qué motocicletas le pertenecen, conocer el estado de una reparación y revisar los trabajos o repuestos utilizados anteriormente. MotoGestión propone centralizar esa información para mejorar la organización y el seguimiento del trabajo.

## 3. Funcionalidades principales

- **Gestión de clientes:** registrar, consultar y actualizar los datos de los clientes.
- **Registro de motocicletas:** registrar motocicletas y asociarlas con sus propietarios.
- **Registro de servicios:** crear un registro u orden del servicio solicitado para una motocicleta.
- **Seguimiento de reparaciones:** actualizar y consultar el estado de una reparación.
- **Historial de servicios y repuestos:** consultar los trabajos anteriores y los repuestos registrados para una motocicleta.

## 4. Requisitos e historias de usuario

El seguimiento inicial de requisitos se realiza mediante GitHub Issues:

| Issue | Funcionalidad |
| --- | --- |
| [#1 – Registro de clientes](https://github.com/100085763/MotoGestion/issues/1) | RF-01: registrar, consultar y actualizar clientes. |
| [#2 – Registro de motocicletas](https://github.com/100085763/MotoGestion/issues/2) | RF-02: registrar motocicletas y asociarlas a un cliente. |
| [#3 – Gestión de servicios](https://github.com/100085763/MotoGestion/issues/3) | RF-03: crear órdenes o registros de servicio. |
| [#4 – Seguimiento de reparaciones](https://github.com/100085763/MotoGestion/issues/4) | RF-04: actualizar y consultar el estado de una reparación. |
| [#5 – Historial de servicios](https://github.com/100085763/MotoGestion/issues/5) | RF-05: consultar el historial de servicios y repuestos. |

También se han abierto tareas de apoyo para la estructura de base de datos, el modelo de datos de motocicletas, el módulo de clientes, el módulo de servicios y el diseño de la interfaz de inicio de sesión.

## 5. Arquitectura propuesta

Se propone una arquitectura cliente-servidor separada en **frontend**, **backend** y **base de datos**. Esta es la arquitectura prevista para el diseño; las tecnologías definitivas y su implementación deberán confirmarse durante el desarrollo.

### Frontend

Será la interfaz con la que interactúan el recepcionista o encargado del taller. Sus responsabilidades serán:

- Presentar formularios para clientes, motocicletas y servicios.
- Mostrar el estado de las reparaciones y el historial.
- Validar campos básicos antes de enviar los datos.
- Enviar solicitudes al backend y presentar los resultados o mensajes de error.

### Backend

Será la parte responsable de procesar las solicitudes y aplicar las reglas del sistema. Sus responsabilidades serán:

- Validar los datos recibidos.
- Gestionar clientes, motocicletas, órdenes de servicio y reparaciones.
- Consultar y actualizar la información almacenada.
- Aplicar las relaciones entre clientes, motocicletas y servicios.
- Devolver respuestas consistentes al frontend.

### Base de datos

Almacenará los datos persistentes del sistema. Como modelo inicial, se contemplan las entidades **Cliente**, **Motocicleta**, **Servicio/Orden de servicio** y **Repuesto**, además del estado y las fechas necesarias para el seguimiento. Las entidades, atributos y relaciones deberán validarse antes de implementar el esquema definitivo.

### Comunicación entre componentes

El frontend se comunicará con el backend mediante una API HTTP, utilizando solicitudes y respuestas en formato JSON. El backend validará cada solicitud, consultará o actualizará la base de datos y devolverá una respuesta al frontend. La tecnología concreta de la API y del motor de base de datos queda pendiente de selección o confirmación.

Flujo general:

`Usuario → Frontend → API del Backend → Base de datos`

La respuesta vuelve desde el backend al frontend para mostrar el resultado al usuario.

## 6. Herramientas utilizadas

- **GitHub:** alojamiento del repositorio y control de versiones.
- **GitHub Issues:** registro y seguimiento de requisitos e tareas.
- **GitHub Projects:** organización visual del trabajo y seguimiento de estados.
- **Visual Paradigm Online:** elaboración de modelos y diagramas UML.

## 7. Gestión del avance

El proyecto utiliza Issues para describir tareas y requisitos, y GitHub Projects para organizar su avance. Los estados del tablero deben reflejar el trabajo real: pendiente, en progreso, en revisión o finalizado, según las columnas configuradas en el proyecto.

Tablero: [MotoGestión – GitHub Projects](https://github.com/users/100085763/projects/1)

## 8. Estado actual del proyecto

El repositorio cuenta con la documentación inicial y Issues para las principales funcionalidades y tareas de apoyo. El proyecto se encuentra en etapa de análisis, diseño y organización del trabajo. **No se declara el sistema como terminado ni listo para producción**: el modelo de datos, la arquitectura tecnológica definitiva, la implementación, las pruebas y la validación con el personal del taller deben confirmarse y completarse.

## 9. Próximos pasos

1. Revisar y validar los requisitos con el encargado o usuario del taller.
2. Completar los diagramas UML y documentarlos en el repositorio.
3. Definir el modelo de datos y las relaciones entre entidades.
4. Seleccionar y documentar las tecnologías definitivas del frontend, backend y base de datos.
5. Implementar una primera funcionalidad completa, comenzando por el registro de clientes.
6. Realizar pruebas funcionales y actualizar los Issues y el tablero de acuerdo con el avance real.
