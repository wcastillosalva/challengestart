# Challenge Start 2025
## API para Mocks de Servicios REST
### Contexto
En proyectos de desarrollo de software es muy común tener que simular el comportamiento de servicios externos mediante mocks, lo cual facilita el desarrollo y las pruebas de sistemas que dependen de ellos. El objetivo de este challenge es que desarrolles una API que permita definir y gestionar mocks de endpoints. La API deberá devolver respuestas personalizadas según la configuración especificada, teniendo en cuenta la ruta, el método HTTP, y parámetros enviados en la URL, en el cuerpo de la solicitud o en los headers así como variaciones en el Content-Type.
Tiempo aproximado de resolución 12 horas.
________________________________________
### Requisitos Funcionales
1.	Configuración Dinámica de Mocks:
o	Endpoint de Configuración:
Crea un endpoint POST /configure-mock que permita registrar nuevas configuraciones para mocks. La configuración deberá incluir:
	Ruta: La URL que se utilizará para acceder al mock (por ejemplo, /api/v1/productos).
	Método HTTP: GET, POST, PUT, DELETE, etc.
	Parámetros de Entrada URL: Especifica si se espera que ciertos parámetros en la URL (fechaInicial=2021-01-29 13:01:00&fechaFinal=2021-01-29 13:06:00)
	Parámetros de Entrada Body: Especifica si se espera en el cuerpo de la solicitud algún valor ("telefono": "45456060").
	Encabezados: Especifica si se espera que ciertos parámetros en los headers de la solicitud (Authorization: Bearer xxxxxxxxxxxxxxx)
	Código de Estado HTTP: El código de respuesta (200, 404, 500, etc.).
	Contenido de la Respuesta: Los datos estáticos (o basados en plantillas) que se deben retornar.
	Content-Type: El tipo de contenido que se retornará (por ejemplo, application/json, text/xml).
2.	Ejecución del Mock:
o	Endpoint Genérico para Mocks:
Todos los endpoints configurados deben ser “escuchados” por la API. Es decir, cuando se haga una solicitud a una ruta que coincida con alguna configuración:
	La API deberá buscar la configuración correspondiente.
	Verificar que el método HTTP y, en caso de ser necesario, los parámetros (en la URL, en el cuerpo o en los headers) coincidan con lo definido.
	Devolver la respuesta configurada, con el código de estado y el encabezado Content-Type indicados.
o	Si la solicitud no coincide con ninguna configuración, retornar un 404 Not Found con un mensaje adecuado.
3.	Gestión de Configuraciones:
o	Permite visualizar, actualizar y eliminar configuraciones existentes (por ejemplo, a través de endpoints como GET /configure-mock o DELETE /configure-mock/:id).
4.	Consideraciones sobre Variaciones:
o	La configuración debe poder admitir variaciones según los parámetros recibidos. Por ejemplo, si un parámetro usuario=admin está presente, retornar una respuesta distinta a cuando no lo esté.
o	Se valorará la capacidad de implementar lógica condicional o utilizar plantillas para generar respuestas dinámicas.
________________________________________
### Requisitos Técnicos
•	Lenguaje y Framework:
Puedes utilizar el lenguaje y framework de tu preferencia (por ejemplo, Node.js con Express, Python con Flask o FastAPI, etc.).
•	Documentación:
Proporciona un archivo README que incluya:
o	Instrucciones de instalación y ejecución.
o	Ejemplos de configuración y de solicitudes a los endpoints (incluir los curls).
o	Descripción de la arquitectura y decisiones de diseño.
•	Buenas Prácticas:
o	Manejo adecuado de errores y validación de datos.
o	Código modular y limpio.
o	(Opcional) Implementa pruebas unitarias para demostrar la robustez de tu solución.
•	Entrega:
o	Sube el proyecto a un repositorio público (por ejemplo, GitHub).
o	Incluye instrucciones claras para probar la aplicación.
________________________________________
### Bonus (Opcionales)
•	Utiliza tu creatividad para agregar funcionalidades extra que creas puedan agregar valor a la solucion.
________________________________________
### Puntos a Evaluar
•	Diseño y Arquitectura:
Claridad en la separación de responsabilidades y modularidad del código.
•	Funcionalidad:
El API debe responder correctamente según la configuración definida.
•	Calidad del Código:
Legibilidad, uso correcto de patrones de diseño y buenas prácticas en general.
•	Documentación y Pruebas:
Calidad y claridad en la documentación, así como la existencia de pruebas unitarias.
•	Creatividad y Extensibilidad:
La implementación de características adicionales (bonus) y la facilidad para ampliar el proyecto.
•	Uso de herramientas de IA:
Como aplicaste tus conocimientos en el uso de las herramientas de IA para acelear tu desarrollo, coloca en el README prompts utilizados
________________________________________
¡Buena suerte y esperamos ver soluciones creativas y robustas!

