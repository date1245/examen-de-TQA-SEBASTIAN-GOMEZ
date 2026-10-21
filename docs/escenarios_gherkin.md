# Escenarios Gherkin - SauceDemo

```gherkin
Feature: Inicio de sesión en SauceDemo

  Scenario: Acceso exitoso con credenciales válidas
    Given que el usuario está en la página de inicio de sesión de SauceDemo
    When ingresa el usuario "standard_user" y la contraseña "secret_sauce"
    And presiona el botón Login
    Then debería ver la página Products con el catálogo

  Scenario: Rechazar el acceso con contraseña incorrecta
    Given que el usuario está en la página de inicio de sesión de SauceDemo
    When ingresa el usuario "standard_user" y la contraseña "clave_incorrecta"
    And presiona el botón Login
    Then debería mostrarse un mensaje de error
    But no debería acceder al catálogo

Feature: Compra de productos

  Scenario: Completar el checkout con datos válidos
    Given que el usuario inició sesión y tiene dos productos en el carrito
    When abre el carrito y presiona Checkout
    And completa nombre, apellido y código postal
    And presiona Continue y luego Finish
    Then debería ver el mensaje "Thank you for your order!"
```
