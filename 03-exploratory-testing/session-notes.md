# Sesión 1 
## Charter 
(Define qué explorar y con qué propósito) 

Explorar el flujo de compras, utilizando diferentes productos y cantidades, para descubrir inconsistencias en la actualizacion de stock, errores en el proceso de pago y fallas en la generacion de orden, que pueden afectar las ventas y la experiencia de compra del cliente.

## ÁREAS 
(Contextualiza el entorno donde se ejecuta la prueba)

Pagina Web; https://petstore.octoperf.com/ 

## INICIO 
(Registra cuándo comienza la sesión – control de tiempo). 
- Fecha: 16 de setiembre 2026
- Hora de Inicio: 18:30
- Hora Fin: 21:30
- Duracion: 3 horas
## TESTER 
(Identifica quién realizó la exploración.) 
Nombre: Dahiana Lezcano
## DESGLOSE DE TAREAS 
(Muestra cómo se distribuyó el tiempo durante la sesión) 
- Comprension del Charter 45 min
- Busqueda y seleccion del producto 15 min
- Agregar productos al carrito 30 min
- Modificar cantidades de compras 10 min
- Eliminar producto seleccionado 10 min
- Finalizar compra del carrito 10 min
- Realizar el pago 10 min
- Verificar la orden de pago 10 min
- Controlar el stock 15 min
- Registrar observaciones 55 min

## ARCHIVOS DE DATOS 
(Indica qué datos se usaron en las pruebas). 
Catalogo de productos

## NOTAS DE PRUEBA 
(Captura lo que se exploró, observó y aprendió del sistema): 
- Seleccion y carga de productos en el carrito: se cargaron algunos animales y se coloco una cierta cantida, se observa que permite tambien agregar al carrito animales con estado "Reservado" (sin stock). No es posible detectar si este es el comportamiento esperado del sistema o una inconsistencia en el stock
- Modificar compra; el sistema permite modificar las cantidades, la actualizacion de importes requiere presional el boton "Cartucho de Actualizacion", salvo contrario no lo hace.
- Eliminar producto; se prueba eliminar el producto del carrito, la actualizacion de importes requiere presional el boton "Cartucho de Actualizacion", salvo contrario no lo hace.
- Limite de compra; el sistema permite realizar la compra de animales sin un monto maximo.
- Proceso de pago; se avanza con el pago del producto hasta la generacion de la orden de compra.
- Seguimiento de orden de compra; en la sesion mis ordenes uno puede volver a visualizar su compra y el detalle de la misma

## LISTA DE RIESGOS  
(Resume posibles problemas importantes detectados o inferidos) 
- Posible inconsistencia en el stock del carrito y el contenido al realizar modificaciones
- Posible inconveniente en compras de cantidades muy grandes

## DEFECTOS (BUGS)  
(Documenta fallos concretos encontrados en el producto.) 
- Actualizacion de modificaciones no es automatica.
- Limite de compras

## INCIDENTES (ISSUES)  
(Registra dudas, vacíos o problemas en el conocimiento del sistema )
- No es posible determinar si existe una cantidad maxima de compra permitida de animales, no se verifica restriccion al ingresar cantidades elevadas.

- las modifcaciones podrian afectar la experiencia del cliente, ya que no es automatico el recalculo

# Sesión 2 
## Charter 
(Define qué explorar y con qué propósito)

Explorar el proceso de registro, autenticación y gestión de cuentas, utilizando diferente tipos de datos valido e inválidos, para descubrir errores en el proceso de validación, autenticación y administración de cuentas, con el fin de garantizar un acceso seguro y confiable para el cliente

## ÁREAS 
(Contextualiza el entorno donde se ejecuta la prueba)
Pagina Web; https://petstore.octoperf.com/ 

## INICIO 
(Registra cuándo comienza la sesión – control de tiempo). 
- Fecha: 16 de setiembre 2026
- Hora de Inicio: 17:00
- Hora Fin: 18:30
- Duracion: 1,5 horas

## TESTER 
(Identifica quién realizó la exploración.) 
Nombre: Dahiana Lezcano

## DESGLOSE DE TAREAS 
(Muestra cómo se distribuyó el tiempo durante la sesión) 
- Registro de usuario 15 min
- Validacion de la cuenta 5 min
- Inicio de sesion 5 min
- verificacion del perfil 10 min
- Registrar forma de pago 15 min
- Registrar Observaciones 40 min

## ARCHIVOS DE DATOS 
(Indica qué datos se usaron en las pruebas). 
- Nombre y Apellido del usuario
- correo
- Telefono
- Direccion
- Ciudad
- Estado
- Pais
- Informacion del Perfil
- contraseña
- ID de usuario

## NOTAS DE PRUEBA 
(Captura lo que se exploró, observó y aprendió del sistema): 
- Ingresar en la pagina, en la opcion "Registrate ahora".
- Completar los datos que solicita el formulario
- click en "Guardar informacion de la cuenta".
- el sistema no completo el registro y emitio un mensaje de error #*HTTP 500- Internal Server Error*#
- Debito al error no se puede completar correctamente el flujo de creacion de cuenta.

## LISTA DE RIESGOS  
(Resume posibles problemas importantes detectados o inferidos)
- El cliente podria no culminar exitosamente el registro.
- Clientes nuevos no podran crear sus cuentas
- Posible perdida de nuevos clientes por fallo en el proceso de registro.
- Se podria entregar pedidos sin la correcta evaluacion de los datos de pago. 
- Falta de registro de forma de pago, puede afectar el proceso de compra y facturacion
- Perdida de confianza del usuario debido a errores durante el registro.    

## DEFECTOS (BUGS)  
(Documenta fallos concretos encontrados en el producto.) 
- No se puede culminar la creacion del usuario,el sistema muestra una pagina de error *HTTP 500- Internal Server Error* 
- No es posible registra la forma de pago

## INCIDENTES (ISSUES)  
(Registra dudas, vacíos o problemas en el conocimiento del sistema )
- Si no se registra una forma de pago, como es posible validar en el sistema que el pedido fue abonado.
- No se cuenta con informacion suficiente para verificar si el error es con todos los usuarios nuevos o es con la carga de determinados datos.  