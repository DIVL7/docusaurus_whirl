---
sidebar_position: 3
---

# Manual de Usuario - Administrador

Bienvenido al manual de usuario para administradores de la plataforma Whirlpool LMS. Esta guía describe las funcionalidades clave disponibles para los administradores.

## Inicio de Sesión

Para acceder a las funcionalidades de administrador, debes iniciar sesión a través de la página de login (`login.html`) con tus credenciales de administrador.

1.  Abre tu navegador web y ve a la URL de la plataforma (ej. `http://localhost:[puerto]/` o la URL de producción).
2.  Serás redirigido a la página de inicio de sesión (`login.html`).
3.  Ingresa tu **Usuario** de administrador.
4.  Ingresa tu **Contraseña** de administrador.
5.  Haz clic en el botón "Iniciar Sesión".
6.  Si las credenciales son correctas, serás redirigido al Panel de Control del Administrador. Si no, verás un mensaje de error.


## Panel de Control (Dashboard)

El panel de control (`admin/dashboard.html`) proporciona una vista general del estado del sistema. Aquí puedes encontrar:

- Estadísticas clave (usuarios activos, cursos disponibles, etc.).
- Accesos directos a las secciones más utilizadas.
- Notificaciones importantes.

Al ingresar, verás un resumen visual con:
- **Tarjetas de Estadísticas:** Números clave como total de usuarios, cursos activos, técnicos completando cursos, etc.
- **Gráficos:** Representaciones visuales del progreso general, actividad reciente, o distribución de usuarios.
- **Accesos Rápidos:** Botones para ir directamente a las secciones de gestión más comunes (Usuarios, Cursos).
- **Actividad Reciente:** Un listado de las últimas acciones realizadas en la plataforma (nuevos registros, cursos completados).

## Gestión de Usuarios

La sección de gestión de usuarios (`admin/users.html`) permite administrar todas las cuentas de usuario en la plataforma. Las funcionalidades incluyen:

- Ver la lista de todos los usuarios (administradores y técnicos).
- Crear nuevas cuentas de usuario.
- Editar la información de usuarios existentes (roles, datos personales).
- Activar/Desactivar cuentas de usuario.
- Eliminar cuentas de usuario.
- Buscar y filtrar usuarios.

**Para Crear un Nuevo Usuario:**
1.  Navega a la sección "Gestión de Usuarios".
2.  Haz clic en el botón "Crear Usuario" o similar.
3.  Completa el formulario con la información requerida (nombre, email, contraseña inicial, rol - Administrador/Técnico).
4.  Guarda los cambios. El nuevo usuario recibirá (o se le deberá proporcionar) sus credenciales.

**Para Editar un Usuario Existente:**
1.  En la lista de usuarios, localiza al usuario que deseas modificar. Puedes usar la barra de búsqueda.
2.  Haz clic en el icono de "Editar" (usualmente un lápiz) junto al nombre del usuario.
3.  Modifica los campos necesarios en el formulario (rol, nombre, estado - activo/inactivo).
4.  Guarda los cambios.

**Para Eliminar un Usuario:**
1.  Localiza al usuario en la lista.
2.  Haz clic en el icono de "Eliminar" (usualmente una papelera).
3.  Confirma la acción en el cuadro de diálogo emergente. *Nota: Esta acción suele ser irreversible.*

**Para Buscar y Filtrar Usuarios:**
1.  Utiliza la barra de búsqueda en la parte superior de la lista para buscar por nombre o email.
2.  Hay opciones de filtro para ver según se necesite. Selecciónalos según sea necesario.

## Gestión de Cursos

Desde la sección de gestión de cursos (`admin/courses.html`), los administradores pueden manejar el catálogo de cursos:

- Ver la lista de todos los cursos disponibles.
- Crear nuevos cursos (título, descripción, imagen).
- Editar la información de cursos existentes.
- Asignar cursos a técnicos o grupos.
- Publicar/Ocultar cursos.
- Eliminar cursos.

**Para Crear un Nuevo Curso:**
1.  Ve a la sección "Gestión de Cursos".
2.  Haz clic en el botón "Crear Curso".
3.  Rellena los detalles del curso: Título, Descripción, Categoría (si aplica), sube una Imagen de portada.
4.  Define si el curso estará "Publicado" (visible para técnicos) o "Borrador".
5.  Guarda el curso. Aparecerá en la lista.

**Para Editar un Curso Existente:**
1.  Localiza el curso en la lista.
2.  Haz clic en el icono de "Editar".
3.  Modifica la información necesaria (título, descripción, imagen, estado).
4.  Guarda los cambios.

**Para Eliminar un Curso:**
1.  Localiza el curso en la lista.
2.  Haz clic en el icono de "Eliminar".
3.  Confirma la acción. 

**Para Asignar Cursos:**
*   Hay una opción dentro de la edición del curso o en la gestión de usuarios para asignar cursos específicos a técnicos individuales o grupos.

## Gestión de Módulos de Curso

Dentro de cada curso, se pueden administrar sus módulos y contenido (`admin/course-modules.html`):

- Añadir nuevos módulos a un curso.
- Editar el contenido de los módulos (texto, imágenes, videos, PDFs).
- Reordenar módulos dentro de un curso.
- Añadir cuestionarios (quizzes) a los módulos.
- Eliminar módulos.

Una vez creado un curso, puedes añadirle contenido estructurado en módulos.

**Para Añadir un Módulo:**
1.  Ve a la gestión del curso específico (puede ser haciendo clic en el nombre del curso en la lista o a través de una opción "Administrar Contenido").
2.  Dentro de la vista de módulos del curso (`admin/course-modules.html`), busca un botón como "Añadir Módulo".
3.  Ingresa el título del módulo y guárdalo.

**Para Editar el Contenido de un Módulo:**
1.  Dentro de la vista de módulos, haz clic en el módulo que deseas editar.
2.  Utiliza el editor de contenido proporcionado para añadir/modificar:
    - **Texto:** Escribe y formatea explicaciones, instrucciones, etc.
    - **Imágenes:** Sube archivos de imagen relevantes.
    - **Videos:** Incrusta videos (mediante enlaces externos).
    - **PDFs:** Adjunta documentos PDF para descargar o visualizar.
3.  Guarda los cambios del contenido del módulo.

**Para Reordenar Módulos:**
1.  En la vista de módulos del curso, busca controles para arrastrar y soltar (drag-and-drop) o botones de "Subir"/"Bajar" junto a cada módulo.
2.  Ajusta el orden según sea necesario. El cambio suele guardarse automáticamente o mediante un botón "Guardar Orden".

**Para Añadir Cuestionarios (Quizzes):**
1.  Dentro de la edición de un módulo o curso, busca una opción "Añadir Cuestionario" o similar.
2.  Configura el cuestionario: título, preguntas (opción múltiple, verdadero/falso, etc.), respuestas correctas, puntaje.
3.  Guarda el cuestionario. Se asociará al módulo o curso correspondiente.

**Para Eliminar un Módulo:**
1.  En la lista de módulos del curso, localiza el módulo a eliminar.
2.  Haz clic en el icono de "Eliminar".
3.  Confirma la acción.

## Generación de Reportes

La sección de reportes (`admin/reports.html`) permite generar informes sobre diversas actividades en la plataforma:

- Reportes de tasa de finalización de cursos.
- Reportes de tasa de éxito de usuarios.
- Reportes de tasa de error de usuarios
- Reportes de actividad en foros.

---