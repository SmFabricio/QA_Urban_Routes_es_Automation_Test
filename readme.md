# **UrbanRoutes Automation Testing**

## Descripción del Proyecto

**UrbanRoutes Automation Testing** es un conjunto de pruebas automatizadas para la aplicación web UrbanRoutes.
El objetivo asegurar que las funcionalidades principales operen correctamente:
- Configuración de rutas
- Selección de categoría (Comfort)
- Selección de métodos de pago
- Agregar número de teléfono
- Añadir comentarios al conductor
- Añadir comodidades (mantas, helados)

_Estas pruebas se ejecutan utilizando Selenium WebDriver._

## Tecnologías y Técnicas Utilizadas

- **Python**: Lenguaje de programación principal utilizado para escribir las pruebas.
- **Selenium WebDriver**: Herramienta para la automatización de navegadores web que permite interactuar con la aplicación como si fuera un usuario real.
- **pytest**: Framework de pruebas para ejecutar y gestionar las pruebas automatizadas.
- **POM (Page Object Model)**: Patrón de diseño que facilita la separación de la lógica de prueba y la interacción con la interfaz de usuario, mejorando la mantenibilidad del código.

## Estructura del Proyecto

El proyecto está dividido en los siguientes archivos:

- **data.py**: Contiene los datos de prueba y configuraciones, como URLs, direcciones, números de teléfono, y detalles de la tarjeta de crédito.
- **helpers.py**: Incluye funciones auxiliares reutilizables, como la recuperación de códigos de confirmación.
- **locators.py**: Define los selectores de los elementos web utilizados en las pruebas y los metodos con los que interactua
- **urban_routes_test.py**: Contiene las pruebas automatizadas para la aplicación UrbanRoutes, utilizando los métodos y localizadores definidos en los otros archivos.

## Instrucciones para Ejecutar las Pruebas

### Prerrequisitos

1. **Instala Python**: Asegúrate de tener Python instalado en tu sistema.
2. **Instala el driver de Selenium**: Asegúrate de tener Selenium en tu dispositivo, puedes encontrarlo en el siguiente enlace: https://www.selenium.dev/downloads/
3. **Instala Selenium para Python**: Para poder utilizar Selenium con Python, necesitas instalar el paquete de Selenium. Sigue los siguientes pasos:
   - Abrir la Consola o Terminal desde las aplicaciones o usando el buscador de aplicaciones.
   - Ejecutar el Comando de Instalación
      ```bash
      pip install selenium
      ```
   - Verifica la instalación con el siguiente comando
      ```bash
      pip freeze
      ```
4. **Instalar PyCharm**: Para descargar PyCharm visita: https://www.jetbrains.com/pycharm/download/ y descarga la versión Community (gratuita) o Professional.
   - Ejecuta el instalador siguiendo las instrucciones en pantalla para completar la instalación.

5. **Instala pytest**: Instala pytest para gestionar y ejecutar las pruebas:
   ```bash
   pip install pytest
   ```

### Configuración del WebDriver

Asegúrate de tener el WebDriver correspondiente para tu navegador (por ejemplo, `chromedriver` para Google Chrome) en tu PATH.
Puedes seguir los siguientes pasos:

1. **Para Windows:**
   - Abre el Panel de Control.
   - Ve a Sistema
   - Configuración avanzada del sistema
   - Variables de entorno. Busca y edita la variable PATH agregando la ruta completa hacia la carpeta bin que acabas de crear. Debería ser algo como C:\\WebDriver\\bin.
2. **Para MacOS y Linux:**
   - Abre la terminal.
   - Ejecuta el siguiente comando para agregar la carpeta bin al PATH del sistema:
    ```bash
      export PATH=/Users/<username>/Downloads/WebDriver/bin:$PATH
      ```
_**Nota:**_ Si planeas descargar WebDriver para otros navegadores y sus versiones, guarda todos los archivos en la misma carpeta: WebDriver/bin. De esta manera, no tendrás que editar PATH de nuevo.

### Ejecutar las Pruebas

**Ejecuta las pruebas con pytest**:
   ```bash
   pytest urban_routes_test.py
   ```
Esto ejecutará todas las pruebas definidas en `urban_routes_test.py` y mostrará los resultados en la terminal.
