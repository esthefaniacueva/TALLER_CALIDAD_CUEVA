 

TALLER
Calidad de Software: Pruebas automatizadas y mejora continua
	


Autora:
Bella Esthefania Cueva Leones


Institución: 
Universidad Técnica “Luis Vargas Torres de Esmeraldas” Sede La Concordia

Facultad: 
Ingenierías

Asignatura: 
Componente profesional de Ingeniería y Gestión de Software.

Docente: 
Ing. Javier Mendoza



Fecha: 28 de octubre de 2026
CALIDAD DE SOFTWARE
Objetivo general
Aplicar pruebas unitarias, cobertura de código, regresión e integración continua.	
Herramientas a utilizar:
1.	Instalación del entorno de visual studio code.
 
2.	Instalación de Python
Opción 1: Descargar directamente desde el navegador
 
Opción 2: Descargar la extensión dentro del entorno de visual studio code.
 
Desarrollo
1.	Preparar el proyecto
Crear una carpeta llamada “Taller_calidad_Cueva”, una vez hecho esto creamos tres archivos:
•	banco.py: código de transferencia. 
•	test_banco.py: pruebas. 
•	requirements.txt: dependencias.
 
Una vez creado los archivos, abrimos una terminal dentro del entorno y escribimos los siguientes comandos:
•	python --version comprueba la versión de Python instalada en tu equipo. 
•	python -m pip install pytest pytest-cov utiliza el gestor de paquetes de Python para instalar pytest (una librería para ejecutar pruebas unitarias) y pytest-cov (una extensión que mide qué porcentaje de tu código pasa por dichas pruebas)
 
2.	Agregar código dentro de los archivos banco.py y test_banco.py
•	Banco.py:
 
•	Test_banco.py:
 
Una vez agregado código dentro de los dos archivos procedemos a ejecutar python -m pytest -v  para verificar que todo marche bien.
 
Luego verificamos la cobertura inicial utilizando:
python -m pytest --cov=banco --cov-report=term-missing 
 
3.	Ampliar pruebas
Amplía las pruebas agregando los casos parametrizados al final de tu archivo test_banco.py: 
 
Volvemos a ejecutar el comando de cobertura para comprobar que esté al 100%.
 
4.	Detectar y corregir defectos
Agrega esta nueva prueba al final de test_banco.py para evaluar transferencias hacia la misma cuenta:
 
Ejecutamos una vez más: python -m pytest -v
 
Se corrige el defecto en banco.py: Modifica la función agregando la validación inmediatamente después de la línea def transferir(...)


 
Vuelve a ejecutar las pruebas aplicando el umbral de calidad exigido (mínimo 81%):
 
