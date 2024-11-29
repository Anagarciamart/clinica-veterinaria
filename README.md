## 🖥️ Tecnologías

Este proyecto utiliza:

    Frontend: Streamlit
    Una biblioteca para construir aplicaciones web interactivas.

    Backend: FastAPI
    Un framework para crear APIs basadas en Python.

    Base de datos en memoria
    Los datos se almacenarán en listas.

## 🚀 Funcionalidades del Sistema
Frontend (Streamlit)

Al iniciar la aplicación, tendrás acceso a un menú principal con las siguientes opciones:

    Registrar Dueño
        Permite registrar los datos de un dueño: nombre, DNI, dirección, correo electrónico y teléfono.
        Envía los datos al backend para ser validados y almacenados.

    Registrar Mascota
        Si el dueño ya está registrado: ingresa los datos de la mascota (nombre, tipo, raza, fecha de nacimiento y condiciones médicas).
        Si el dueño no está registrado: permite registrar al dueño y su mascota en una sola operación.

    Buscar Dueño
        Busca y muestra los datos de un dueño y sus mascotas asociadas usando el DNI o el teléfono.

    Eliminar Dueño/Mascota
        Permite eliminar un dueño y todas sus mascotas asociadas.
        También puedes eliminar o marcar como fallecida una mascota específica.

Backend (FastAPI)

El backend tiene los siguientes endpoints:

    POST /registrar-dueño/
        Registra un nuevo dueño, validando que el DNI no esté duplicado.

    POST /registrar-mascota/
        Registra una mascota para un dueño existente, validando que el dueño exista.

    GET /buscar-dueño/{dni_o_tel}
        Busca un dueño usando su DNI o teléfono, devolviendo sus datos y las mascotas asociadas.

    DELETE /eliminar-dueño-y-mascotas/
        Elimina un dueño y todas sus mascotas.

    DELETE /eliminar-mascota/
        Elimina una mascota específica asociada a un dueño.

    PUT /actualizar-estado-mascota/
        Actualiza el estado de una mascota (por ejemplo, marcarla como fallecida).
