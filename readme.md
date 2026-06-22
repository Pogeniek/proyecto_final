# Proyecto de Automatización QA - Marcos Vargas

---

## 📖 ¿Qué es este proyecto?

Este es mi proyecto final del curso de QA Testing Automatizado. 

Creé un conjunto de pruebas automáticas para probar una página web (SauceDemo) y una API (ReqRes), usando Python.

El objetivo es practicar lo que aprendimos en clase y tener un proyecto para mostrar lo que sé hacer.

---

## 🛠️ Tecnologías que usé

- **Python** - Lenguaje de programación
- **Selenium WebDriver** - Para controlar el navegador
- **Pytest** - Para escribir y ejecutar las pruebas
- **Requests** - Para probar APIs
- **Pytest-HTML** - Para generar reportes
- **Git y GitHub** - Para guardar el código

---

## 📁 Estructura del proyecto

proyecto_final/
│
├── pages/ # Page Objects (login, productos, carrito, checkout)
├── tests/ # Pruebas (login, carrito, checkout, API)
├── utils/ # Configuraciones y helpers
├── data/ # Datos de prueba (JSON, CSV)
├── reports/ # Reportes HTML
├── logs/ # Logs de ejecución
├── screenshots/ # Capturas de pantalla (fallos)
│
├── requirements.txt # Dependencias
└── README.md # Este archivo


---

## ⚙️ Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/Pogeniek/proyecto_final.git

Instalar dependencias

pip install -r requirements.txt

▶️ Cómo ejecutar las pruebas
Ejecutar todas las pruebas
bash

pytest

Ejecutar pruebas específicas
bash

# Solo pruebas de login
pytest tests/test_login.py

# Solo pruebas de API
pytest tests/test_api.py

Generar reporte HTML
bash

pytest --html=reports/report.html

📊 Resultados y reportes
Reporte HTML

Después de ejecutar las pruebas, se genera un reporte en reports/report.html. Lo abro en el navegador y veo:

    ✅ Pruebas que pasaron

    ❌ Pruebas que fallaron

    ⏱️ Tiempo de ejecución

    📸 Captura de pantalla si falló

Logs

En la carpeta logs/ se guarda un registro de lo que pasó durante la ejecución.
Capturas de pantalla

Si una prueba falla, se guarda automáticamente una captura en screenshots/.
🧪 Pruebas que hice
Pruebas de UI (página web)
#	Prueba	Tipo
1	Login exitoso	Positivo
2	Login fallido	Negativo
3	Agregar producto al carrito	Positivo
4	Eliminar producto del carrito	Positivo
5	Completar proceso de compra	Positivo
Pruebas de API
#	Prueba	Método
1	Obtener lista de usuarios	GET
2	Crear usuario nuevo	POST
3	Eliminar usuario	DELETE
🏗️ Cómo organicé el código

Usé Page Object Model para separar las páginas de las pruebas:
text

pages/          → Dónde están los botones, campos, etc.
tests/          → Las pruebas que verifican el comportamiento

Esto hace que el código sea más fácil de mantener.
📌 Buenas prácticas que apliqué

    ✅ Separé las páginas de las pruebas (POM)

    ✅ Usé esperas explícitas (evito time.sleep())

    ✅ Las pruebas son independientes entre sí

    ✅ Usé datos externos (JSON/CSV) para parametrizar

    ✅ Incluí escenarios negativos

    ✅ Genero reportes automáticos

    ✅ Capturo pantalla cuando falla

    ✅ Guardo logs de ejecución

🐛 Si algo falla

    Reviso el log en logs/test_execution.log

    Abro el reporte HTML en reports/report.html

    Veo la captura en screenshots/
