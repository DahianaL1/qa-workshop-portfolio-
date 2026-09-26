# API Testing — Alcance 
## API 
Swagger Petstore (https://petstore.swagger.io/)

## Alcance funcional 
Gestión de mascotas (pet). 

## Operaciones seleccionadas 
| Método HTTP | Endpoint | Propósito | 
|---|---|---| 
| POST | /pet | Crear una nueva mascota en la tienda |
| GET | /pet/{petId} | Consultar la información de una mascota por su ID |
| PUT | /pet | Actualizar los datos de una mascota existente |
| DELETE | /pet/{petId} | Eliminar una mascota del sistema | 

## Justificación 
¿Por qué seleccionaste estas operaciones? 

Seleccione estas operaciones porque representan el flujo completo de una API (Crear, Consultar, Actualizar, Borrar). Con las pruebas se estaria verificando las funciones esenciales del sistema.

## Condiciones de prueba identificadas 
¿Qué condiciones consideras necesario verificar?
1. Creacion exitosa con datos validos.
2. Busqueda exitosa utilizando ID valido.
3. Busqueda fallida utilizando ID Inexistente (escenario negativo)
4. Actualizacion exitosa del nombre o estado de la mascota.
5. Eliminacion exitosa de la mascota creada.

## Fuera de alcance 
¿Qué operaciones o aspectos no probarás en este ejercicio?

1. Carga de imagenes para mascotas (POST /pet/{petId}/uploadImage)
2. Busqueda por estado (GET /pet/findByStatus)
3. Operaciones del modulo 'store' y 'user'