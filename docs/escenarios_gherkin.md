# Escenarios Gherkin 
Feature: Inicio de sesion en SauceDemo 
Scenario: Acceso exitoso con credenciales validas 
Given que estoy en la pagina de inicio de sesion 
When ingreso credenciales validas y pulso Login 
Then deberia acceder al catalogo de productos 
