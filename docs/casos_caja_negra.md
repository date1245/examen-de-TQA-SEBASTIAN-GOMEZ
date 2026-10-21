# Casos de prueba de caja negra - SauceDemo

Detalle completo (diseño y ejecución) en `casos_caja_negra_SauceDemo.docx`, elaborado con la plantilla de la materia.
Datos de acceso: `standard_user` / `secret_sauce`.

| ID | Caso | Resultado esperado | Estado | Evidencia |
|---|---|---|---|---|
| CP-01 | Inicio de sesión exitoso | Se muestra el catálogo (Products) | Passed | `CP-01.png` |
| CP-02 | Inicio de sesión con contraseña incorrecta | Acceso rechazado con mensaje de error | Pendiente | `CP-02.png` |
| CP-03 | Agregar Sauce Labs Bike Light al carrito | Producto en el carrito y contador en 1 | Passed | `CP-03.png` |
| CP-04 | Eliminar producto del carrito | Carrito vacío y contador sin número | Pendiente | `CP-04.png` |
| CP-05 | Completar el checkout con 2 productos | Se muestra "Thank you for your order!" | Passed | `CP-05_01.png`, `CP-05_02.png`, `CP-05_03.png` |
