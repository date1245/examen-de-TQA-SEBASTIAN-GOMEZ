# &#x20;Casos de prueba de caja negra — SauceDemo

# 

# &#x20;1. Información general

# 

# \-Aplicación:\*\* SauceDemo

# \-URL:\*\* https://www.saucedemo.com/

# \-Tipo de prueba:\*\* Caja negra funcional

# \-Objetivo:\*\* comprobar el comportamiento visible de las funciones de inicio de sesión, carrito de compras y checkout.

# 

# &#x20;2. Casos de prueba

# 

# &#x20;CP-01: Inicio de sesión exitoso

# 

# \-Precondición:\*\* la página de inicio de sesión está disponible.

# \-Datos de prueba:\*\* usuario `standard\_user`; contraseña `secret\_sauce`.

# \- Pasos:

# &#x20; 1. Abrir SauceDemo.

# &#x20; 2. Introducir el usuario y la contraseña indicados.

# &#x20; 3. Pulsar Login.

# \- Resultado esperado:\*\* se muestra el catálogo de productos.

# \- Resultado obtenido:\*\* pendiente de ejecución.

# \- Estado:\*\* Pendiente.

# \- Evidencia:\*\* guardar una captura del resultado en `evidencias/capturas/CP-01.png`.

# 

# \### CP-02: Inicio de sesión con contraseña incorrecta

# 

# \- \*\*Precondición:\*\* la página de inicio de sesión está disponible.

# \- \*\*Datos de prueba:\*\* usuario `standard\_user`; contraseña incorrecta `clave\_incorrecta`.

# \- \*\*Pasos:\*\*

# &#x20; 1. Abrir SauceDemo.

# &#x20; 2. Introducir el usuario y la contraseña incorrecta.

# &#x20; 3. Pulsar Login.

# \- \*\*Resultado esperado:\*\* el sistema impide el acceso y muestra un mensaje de error.

# \- \*\*Resultado obtenido:\*\* pendiente de ejecución.

# \- \*\*Estado:\*\* Pendiente.

# \- \*\*Evidencia:\*\* `evidencias/capturas/CP-02.png`.

# 

# \### CP-03: Agregar un producto al carrito

# 

# \- \*\*Precondición:\*\* iniciar sesión correctamente.

# \- \*\*Datos de prueba:\*\* usuario `standard\_user`; contraseña `secret\_sauce`; producto Sauce Labs Backpack.

# \- \*\*Pasos:\*\*

# &#x20; 1. Iniciar sesión.

# &#x20; 2. Ubicar Sauce Labs Backpack.

# &#x20; 3. Pulsar Add to cart.

# &#x20; 4. Revisar el indicador del carrito.

# \- \*\*Resultado esperado:\*\* el producto se agrega al carrito y el indicador muestra una unidad.

# \- \*\*Resultado obtenido:\*\* pendiente de ejecución.

# \- \*\*Estado:\*\* Pendiente.

# \- \*\*Evidencia:\*\* `evidencias/capturas/CP-03.png`.

# 

# \### CP-04: Eliminar un producto del carrito

# 

# \- \*\*Precondición:\*\* iniciar sesión y agregar Sauce Labs Backpack al carrito.

# \- \*\*Pasos:\*\*

# &#x20; 1. Abrir el carrito.

# &#x20; 2. Verificar que aparece Sauce Labs Backpack.

# &#x20; 3. Pulsar Remove.

# \- \*\*Resultado esperado:\*\* el producto deja de aparecer en el carrito y el indicador se actualiza según corresponda.

# \- \*\*Resultado obtenido:\*\* pendiente de ejecución.

# \- \*\*Estado:\*\* Pendiente.

# \- \*\*Evidencia:\*\* `evidencias/capturas/CP-04.png`.

# 

# \### CP-05: Validar campos obligatorios del checkout

# 

# \- \*\*Precondición:\*\* iniciar sesión y agregar al menos un producto al carrito.

# \- \*\*Pasos:\*\*

# &#x20; 1. Abrir el carrito.

# &#x20; 2. Pulsar Checkout.

# &#x20; 3. Dejar vacíos los campos del formulario de información.

# &#x20; 4. Pulsar Continue.

# \- \*\*Resultado esperado:\*\* el sistema impide continuar y muestra un mensaje que identifica un campo obligatorio.

# \- \*\*Resultado obtenido:\*\* pendiente de ejecución.

# \- \*\*Estado:\*\* Pendiente.

# \- \*\*Evidencia:\*\* `evidencias/capturas/CP-05.png`.

# 

# \## 3. Resumen de ejecución

# 

# Los cinco casos están diseñados, pero todavía deben ejecutarse. Completar el resultado obtenido y el estado de cada caso después de comprobar el comportamiento real de la aplicación.

# 

# \- \*\*Passed:\*\* el resultado real coincide con el esperado.

# \- \*\*Failed:\*\* el resultado real no coincide con el esperado.

# \- \*\*Blocked:\*\* no se pudo ejecutar por un impedimento.

# \- \*\*Pendiente:\*\* todavía no se ejecutó.

# 

# No registrar un defecto únicamente porque una prueba haya fallado: primero documentar los pasos, el resultado observado y la evidencia.



