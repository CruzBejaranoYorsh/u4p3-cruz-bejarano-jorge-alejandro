# Guion de defensa — U4P3

Ensáyalo en voz alta con cronómetro; el objetivo es que dure cerca de dos minutos.

**0:00–0:30 — Qué hace el sistema**

“Mi proyecto es una aplicación para consultar y administrar servicios. El nombre del proyecto es U4P3 y yo soy Cruz Bejarano Jorge Alejandro. Un usuario puede crear una cuenta, iniciar sesión y gestionar sus propios servicios y facturas.”

**0:30–1:15 — Decisiones técnicas**

“Usé Django para organizar el proyecto con modelos, vistas y plantillas, y para aprovechar su sistema de autenticación. La aplicación guarda los datos en MySQL con Aiven y está desplegada con Render. El listado filtra por `propietario=request.user`, y las vistas de edición y eliminación buscan el registro junto con su propietario. Además, las facturas muestran sus renglones y calculan el total; los reportes permiten consultar y descargar resultados en CSV.”

**1:15–1:45 — Pulido de la interfaz**

“En esta versión agregué búsqueda por título, paginación y mensajes claros cuando no hay resultados. En pantallas pequeñas, las tablas permiten desplazamiento horizontal. En la revisión por pares encontré que al mostrar o editar un registro era importante comprobar siempre el propietario; lo corregí obteniendo el objeto con `get_object_or_404` y el usuario autenticado, además de filtrar los servicios disponibles al crear una factura.”

**1:45–2:00 — Cierre**

“La aplicación está en https://u4p3-cruz-bejarano-jorge-alejandro.onrender.com y el código está en https://github.com/CruzBejaranoYorsh/u4p3-cruz-bejarano-jorge-alejandro. Como mejora principal puedo mostrar el aislamiento entre usuarios: una cuenta nueva inicia sesión y no puede ver ni modificar los datos de otra cuenta.”
