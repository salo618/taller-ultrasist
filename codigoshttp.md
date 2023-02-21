# Códigos de estado Http #


## Códigos de estado HTTP 100 ##

La solicitud se está procesando

| Código | Descripción |
| ----------- | ----------- |
| 100 | Continue. Encabezado solicitado, recibido y aceptado, listo para recibir el cuerpo de la petición. |
| 101 | Switching protocols. Tu navegador solicita una actualización del encabezado, el servidor funciona correctamente. |
| 102 | Processing. Solicitud recibida y en proceso. La respuesta todavía no está disponible. |
| 103 | Early hints. El servidor proporciona algunos encabezados que permiten la precarga de recursos mientras se carga el resto de la respuesta. |

## Códigos de estado HTTP 200 ## 

La solicitud se ha completado con éxito y el navegador ha recibido información. 

| Código | Descripción |
| ----------- | ----------- |
| 200 | Everything OK. La solicitud se ha completado con éxito y está definida por el método HTTP utilizado |
| 201 | Accepted. La solicitud del navegador ha sido aceptada, pero sigue en proceso. Puede tener éxito o no. |
| 202 | Non-authoritative information. La información procede de un servidor proxy que ha recibido un código de estado 200 “OK”. |
| 203 | No content. Solicitud procesada, pero no se ha enviado contenido. Los encabezados pueden ser de utilidad. |
| 204 | No content. Solicitud procesada, pero no se ha enviado contenido. Los encabezados pueden ser de utilidad. |
| 205 | Reset content. Similar al 204, pero informa al usuario que se debe cargar de nuevo el documento.  |
| 206 | Partial content. Si tu navegador utiliza “range headers”, este código te informa que solo se ha enviado una parte de la fuente. |
| 226 | IM used. El servidor ha recibido una solicitud GET, pero la respuesta refleja una manipulación de la instancia. |

## Métodos HTTP ##

- GET: el recurso se ha obtenido y está en el cuerpo del mensaje.
- HEAD: los encabezados están en el cuerpo del mensaje.
- POST or PUT: el recurso que describe el resultado de la acción ha sido transmitido al cuerpo del mensaje.
- TRACE: el body del mensaje contiene la solicitud.

## Códigos de estado HTTP 300 ##

Indica que un recurso ha sido realojado. Estos códigos ofrecen información sobre dónde buscar el contenido realojado.

| Código | Descripción |
| ----------- | ----------- |
| 300 | Multiple choice. La solicitud tiene más de una respuesta posible. El navegador/usuario debe elegir una. |
| 301 | Moved permanently. La URL de la fuente solicitada ha cambiado de forma permanente. La nueva URL se ofrece en la respuesta. |
| 302 | Found. La URL de la fuente solicitada ha cambiado de forma temporal. Por lo tanto, el cliente debería utilizar la misma URL en futuras consultas. |
| 303 | See other. El servidor devuelve esta respuesta para dirigir al cliente a la fuente solicitada en otra URL con una solicitud GET. Requiere conocimiento de los cuatro métodos de petición HTTP. |
| 304 | Not modified. Se utiliza con fines de almacenamiento en caché. Le dice al cliente que los recursos almacenados en caché no han cambiado. El cliente puede continuar usando la misma versión en caché de la respuesta, acelerando así el proceso. |
| 307 | Temporary redirect. Reemplaza el código de respuesta HTTP 302 Found HTTP cuando una fuente ha sido desplazada temporalmente a otra URL. En este caso, el método HTTP no puede cambiarse, si se ha utilizado POST, debe utilizarse de nuevo. |
| 308 | Permanent redirect. Similar al código HTTP 301; la fuente se encuentra ubicada permanentemente en otra URL, especificada por Location: HTTP Response header |

## Códigos de estado HTTP 400: códigos de error de cliente ##

No se puede encontrar la web o la página. La página no está disponible o la solicitud es técnicamente problemática.

| Código | Descripción |
| ----------- | ----------- |
| 400 | Bad request. El servidor no puede responder debido a un error con el cliente. |
| 401 | Unauthorized. El cliente debe autentificarse para obtener una respuesta. |
| 402 | Payment required. Reservado para un uso futuro; rara vez se utiliza, ya que no se ha adoptado ninguna convención estándar. |
| 403 | Forbidden. El cliente no tiene permiso para acceder al contenido; por ejemplo, puede requerir una contraseña. |
| 404 | Proxy authentication required. A la hora de utilizar un servidor proxy, tu navegador tiene que autentificarse para continuar. |
| 405 | Method not allowed. El servidor admite el método utilizado, pero la fuente objetivo no, ya que ha sido deshabilitada. |
| 406 | Not acceptable. El recurso solicitado solo puede generar contenido inaceptable de acuerdo con los encabezados solicitados.  |
| 407 | Proxy authentication required. A la hora de utilizar un servidor proxy, tu navegador tiene que autentificarse para continuar. |
| 408 | Request timeout. Al servidor le gustaría cerrar una conexión inactiva, pero la solicitud no se ha completado antes del tiempo de espera. Algunos servidores no envían ningún mensaje antes de desconectarse. |
| 409 | Conflict. Tu solicitud ha entrado en conflicto con la fuente o el servidor. |
| 410 | Gone. El contenido solicitado ha sido eliminado permanentemente del servidor y no se restablecerá. |
| 411 | Length required. La solicitud ha sido rechazada, ya que la longitud del encabezado no encaja con las especificaciones del servidor. |
| 412 | Precondition failed. El servidor no ha cumplido con las condiciones del encabezado de tu navegador. |
| 413 | Payload too large. Tu solicitud es mayor que los límites definidos por el servidor. |
| 414 | URI too long. La solicitud es demasiado larga para el servidor. |
| 415 | Unsupported media type. El servidor ha rechazado la solicitud, ya que no admite el formato multimedia de los datos solicitados. |
| 416 | Range not satisfiable. El servidor no puede devolver la solicitud; el rango del campo del encabezado está fuera del alcance de los datos del URI. |
| 417 | Expectation failed. El servidor no puede cumplir con las condiciones del campo del encabezado de la solicitud. |
| 421 | Misdirected request. El servidor no está configurado para producir una respuesta a la solicitud. |
| 422 | Unprocessable entity. Los errores semánticos en la solicitud prohíben al servidor procesar una respuesta. |
| 423 | Locked. La fuente está bloqueada y no se puede acceder a ella.  |
| 424 | Failed dependency. La solicitud ha fallado debido a la solicitud previa. |
| 425 | Too early. Indica que el servidor no puede procesar una solicitud. |
| 426 | Upgrade required. El servidor declina una solicitud en el protocolo actual; en su lugar, envía un Upgrade Header indicando el protocolo correcto. |
| 428 | Pre-condition required. El servidor no puede procesar la solicitud hasta que no se cumplan las condiciones. |
| 429 | Too many requests. Es una respuesta que limita la velocidad del servidor cuando el usuario ha enviado demasiadas solicitudes en un periodo de tiempo determinado.  |
| 431 | Request header fields too large. Los campos del encabezado en la solicitud son demasiado largos para el servidor. |
| 451 | Unavailable for legal reasons. El servidor tiene prohibido otorgar acceso a la solicitud; puede ser una página web censurada oficialmente |


## ¿Cómo solucionar los errores de estado 503? ##

Este tipo de errores están relacionados con el servidor y están fuera de tu control. Ten en cuenta estos tres factores:

1. Si una web está recibiendo mucho tráfico cuando aparece este error (asegúrate primero de que sea tráfico real y no de bots), es posible que el plan actual del hosting de tu web no pueda soportar el flujo de tráfico. La mejor solución sería contactar con tu proveedor y mejorar tu servidor.

2. Si una página está devolviendo un error 503, puede que tu servidor esté en mantenimiento o se haya colapsado. Ten paciencia y contacta con tu proveedor de hosting para averiguar cuándo va a solucionarse el problema.

3. Identifica si es un ataque DoS o DDoS

| Ataques DoS |	Ataques DDoS  
| ----------- | ----------- |
| Se puede llevar a cabo con un solo sistema o computadora. |	Utiliza múltiples sistemas o computadoras para llevar a cabo el ataque. |
| DoS es un ataque lento. |	DDoS es más rápido por naturaleza. |
