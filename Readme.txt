# Ejercicio de Prueba de Carga - API de Login

## Descripción
Este repositorio contiene los elementos de una prueba de carga realizada sobre el servicio de login de la API 'https://fakestoreapi.com/auth/login'. 
El objetivo principal es simular un escenario de carga de al menos 20 Transacciones Por Segundo (TPS) y validar el rendimiento y la estabilidad del servicio bajo las siguientes condiciones:
- Tiempo de respuesta: Máximo 1,5 segundos.
- Tasa de error: Menor al 3%.

## Tecnologías Utilizadas
- Herramienta de prueba: Apache JMeter (versión 5.6.3)
- Ejecución: Java 17

## Archivos del Repositorio
- 'Test Plan - Login.jmx': El plan de pruebas de JMeter con la configuración completa del escenario.
- 'users.csv': El archivo de datos de entrada que contiene los usuarios y contraseñas para la prueba.
- 'conclusiones.txt': Un resumen de los hallazgos y conclusiones obtenidos del análisis de los resultados.
- 'readme.txt': Este archivo con las instrucciones de ejecución.
- 'index.html': Reporte html generado con los resultados obtenidos.
- 'outcome.jtl': Archivo de resultados del test.

## Instrucciones de Ejecución

1.  Requisitos previos: Asegúrate de tener instalado Java 17, JMeter 5.6.3 y configuradas las variables de entorno requeridas.

2.  Clonar el repositorio:
    git clone [https://github.com/97Armando/users-jmeter.git]
    cd users-jmeter
    

3.  Ejecutar la prueba de carga: Abra una terminal, navegue a la carpeta 'bin' de su instalación de JMeter y ejecute el siguiente comando.
    
    Asegurese de reemplazar la '[RUTA_DEL_PROYECTO]' con la ruta absoluta donde se clono el repositorio.
    
    jmeter -n -t "[RUTA_DEL_PROYECTO]/Test Plan - Login.jmx" -l "[RUTA_DEL_PROYECTO]\Outome\outcome.jtl" -e -o "[RUTA_DEL_PROYECTO]\Report"
    
    
    EJEMPLO EN EQUIPO LOCAL USADO:
    jmeter -n -t "C:\Users\JAMALDONADO\Documents\TEST\users-jmeter\Test Plan - Login.jmx" -l "C:\Users\JAMALDONADO\Documents\TEST\users-jmeter\Outcome\outcome.jtl" -e -o "C:\Users\JAMALDONADO\Documents\TEST\users-jmeter\Report"



    * 'Test Plan - Login.jmx': El plan de pruebas.
    * 'outcome.jtl': Archivo de resultados brutos.
    * 'Report': Carpeta de destino del reporte (debe estar vacía antes de la ejecución del comando).

4.  Revise el reporte: Una vez que la ejecución termine, abra el archivo 'index.html' en la carpeta 'Report' en su navegador web para visualizar el dashboard de resultados.

5.  Análisis de conclusiones: Lea el archivo 'conclusiones.txt' para entender el análisis de los resultados de la prueba.