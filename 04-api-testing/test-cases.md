# API Testing — Casos de prueba 
 
## Caso API-01: Crear una mascota valida (Positivo)
 
**Objetivo:** verificar que se pueda registrar los datos completos de una nueva mascota.
 
**Operación y endpoint:** 
 `POST /pet`
 
**Precondiciones:** Ninguna.
 
**Datos de entrada:**  
Json Body
```json
{
  "id": 98765,
    "name": "PERROQA",
    "status": "available"
}
```
 
**Resultado esperado:** 
CODIGO DE ESTADO 200 ok , respuesta del JSON con ID 98765 y nombre "PERROQA"
 
**Resultado obtenido:** 

Paso exitoso (PASS).
El servidor respondio con el codigo del estado esperado. Y la estructura correcta

**Evidencia:** 

evidence/Api-1.png

 --- 
 
## Caso API-02: Consulta mascota utilizando un ID previamente creado (Positivo)
 
**Objetivo:** Verificar las respuesta del sistema al buscar un ID existente
 
**Operación y endpoint:** `GET /pet/{petId}`
 
**Precondiciones:** La mascota con ID 98765 debe existir.
 
**Datos de entrada:** Parameters petId:98765
 
**Resultado esperado:** Codigo 200 ok y datos de "PERROQA"
 
**Resultado obtenido:** 
Paso exitoso. El servidor respondio con el codigo del estado esperado.
 
**Evidencia:** 
evidence/Api-2.png

 --- 

## Caso API-03: Consulta mascota utilizando un ID inexistente (Negativo)
 
**Objetivo:** verificar que el sistema emita error al buscar un ID inexistente
 
**Operación y endpoint:** 
 `GET /pet/{petId}`
 
**Precondiciones:** Ninguna.
 
**Datos de entrada:**  
 Parameters petId:998877665544
 
**Resultado esperado:** Codigo de estado 404 not found y mensaje de error "Pet not found"

**Resultado obtenido:** 
Paso exitoso. El servidor respondio con el codigo del estado esperado.
 
**Evidencia:** 
evidence/Api-3.png

 --- 

## Caso API-04: Actualizar nombre y estado de la mascota (Positivo)
 
**Objetivo:** Modificar datos de una mascota existente
 
**Operación y endpoint:** 
 `PUT /pet`
 
**Precondiciones:** La mascota con ID 98765 debe existir.
 
**Datos de entrada:**  
Json Body
```json
{
  "id": 98765,
    "name": "PERROQA_MODIFICADO",
    "status": "sold"
}
```
 
**Resultado esperado:** CODIGO DE ESTADO 200 ok y el campo status actualizado a "sold"
 
**Resultado obtenido:** 
Paso exitoso. El servidor respondio con el codigo del estado esperado.
 
**Evidencia:** 
evidence/Api-4.png

 --- 

## Caso API-05: Eliminar la mascota creada (positivo)
 
**Objetivo:** Eliminar la mascota del sistema
 
**Operación y endpoint:** `DELETE /pet/{petId}`
 
**Precondiciones:** La mascota con ID 98765 debe existir.
 
**Datos de entrada:**  Parameters petId:98765

**Resultado esperado:** CODIGO DE ESTADO 200 ok 
 
**Resultado obtenido:** 
Paso exitoso. El servidor respondio con el codigo del estado esperado.
 
**Evidencia:** 
evidence/Api-5.png

 --- 

# Conclusiones 
## Resultados relevantes 
¿Qué resultados consideras más importantes y por qué?
1. Se validó correctamente el ciclo básico (Crear, Consultar, Actualizar y Eliminar) dentro del módulo de mascotas
2. Se verificó el manejo del código de respuesta 404 Not Found en un escenario de búsqueda con ID inexistente.

## Limitaciones 
¿Qué aspectos no pudiste verificar? 
1. Al ejecutarse sobre una API pública y compartida (Swagger Petstore), existe la posibilidad de que otros usuarios alteren o eliminen el registro con ID 98765

## Pruebas adicionales 
¿Qué otras pruebas realizarías si tuvieras más tiempo? 
Validar el comportamiento del endpoint enviando tipos de datos inválidos en la ruta (ejemplo: enviar letras en lugar de números para el `petId`) para comprobar si retorna un `400 Bad Request`

