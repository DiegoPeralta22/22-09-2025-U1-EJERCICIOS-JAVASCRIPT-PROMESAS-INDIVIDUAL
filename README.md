Este repositorio contiene una serie de 7 ejercicios diseñados para practicar la implementación y el manejo de flujos asíncronos en JavaScript utilizando el objeto Promise. Cada ejercicio simula un escenario de la vida real (descargas, pagos, autenticación) para ilustrar el uso de resolve y reject.
-------descargarArchivo(tamaño)------------------
Concepto Clave: Introducción a las promesas y manejo de estados básicos.

Objetivo: Simular la descarga de un archivo.

Lógica: La promesa se resuelve exitosamente si el tamaño es menor o igual a un umbral definido (50), y se rechaza si es demasiado grande, demostrando el manejo del flujo .then() y .catch().

-----------------------------verificarEdad(edad) -----------------------------------

Concepto Clave: Uso de promesas para validación de datos.

Objetivo: Implementar un control de acceso basado en la edad.

Lógica: La promesa utiliza una condición simple para determinar si la edad es válida para la acción (ej. una compra), resolviendo el flujo si la condición se cumple o rechazándolo si no, reforzando la estructura básica de Promise(resolve, reject).

---------------------------------verificarStock(producto, cantidad)  ---------------------------------------------------------
Concepto Clave: Promesas con validación contra una fuente de datos externa.

Objetivo: Verificar la disponibilidad de un producto en un inventario estático.

Lógica: La función recibe dos parámetros y consulta un objeto global (inventario) para confirmar la existencia del producto (hasOwnProperty) y si la cantidad solicitada está disponible, resolviendo solo si ambas condiciones son ciertas.

------------------------------------------------ procesarPago(monto)-----------------------------------------------------------------------
Concepto Clave: Promesas para validación de transacciones simples.

Objetivo: Validar si un monto de pago es aceptable.

Lógica: Es un ejercicio directo que resuelve la promesa si el monto es un valor positivo, simulando un pago exitoso, o lo rechaza si el monto es inválido (negativo o cero).

------------------------------------------ autenticarUsuario(usuario, contraseña) ---------------------------------------------------------------
Concepto Clave: Simulación de API con respuestas estructuradas (JSON).

Objetivo: Implementar una promesa para verificar credenciales fijas.

Lógica: En lugar de devolver solo un mensaje de texto, esta promesa devuelve objetos estructurados. En caso de éxito, retorna un objeto con el usuario y su rol. En caso de fallo, retorna un objeto de error con un código (ej. 401 Unauthorized), imitando una respuesta de servidor real.

--------------------------------------------- verificarSaldo(cuenta, monto) -------------------------------------------------------------------------------
Concepto Clave: Lógica de negocio avanzada con retorno de estado financiero.

Objetivo: Simular una verificación de saldo bancario antes de una transacción.

Lógica: Compara el monto a retirar con la cuenta actual. La promesa retorna un objeto de éxito con el saldoRestante calculado o un objeto de error (ej. con código 402, Fondos Insuficientes) que incluye el saldoDisponible, proporcionando datos detallados en ambos escenarios.

------------------------------------- consultarClima(ciudad) ------------------------------------------------------------------------------------------------------
Concepto Clave: Simulación completa de una consulta a una base de datos/API.

Objetivo: Consultar el clima para una ciudad específica en una "Base de Datos" local (objeto).

Lógica: Utiliza un objeto global como fuente de datos. Si la ciudad existe en la base de datos, la promesa se resuelve devolviendo un objeto con la temperatura y condición. Si la ciudad no existe, se rechaza con un objeto de error y un código 404 (No Encontrado), consolidando el uso de funciones, promesas y objetos estructurados.
