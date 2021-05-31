# Estrategia de pruebas:

Para ver la estartegia de pruebas para la semana 8 de clic [aquí](https://drive.google.com/file/d/1zUkMoHK-1Ukpo-ktSir54X3wmQXuQ9bJ/view?usp=sharing).

## Pruebas de reconocimiento manuales

En este repositorio encontrará el inventario de pruebas realizadas para la versión de Ghost 3.42.5, y también los issues encontrados en su relaización, 
estas pruebas se hicieron tomando como base las realizadas previamente para la versión de Ghost 3.3.0 y se valido que los comportamientos se mantuvieran.

## Otros repositorios

- [Pruebas de reconocimiento](https://github.com/anderson0365/pruebasReconocimiento) Monkeys and Rippers
- [Pruebas E2E](https://github.com/anderson0365/escenariosPruebasCypressE2E)
- [Pruebas de regresión VRT](https://github.com/andres-benavides-andes/escenariosPruebasCypressE2E)
- [Pruebas con generación de datos](https://github.com/anderson0365/randomValueTest)

## Distribución de Esfuerzo
Los ingenieros automatizadores senior ejecutarán las pruebas como se describe a continuación. Durante las pruebas ejecutadas, todas las incidencias encontradas deberán ser reportadas en el repositorio de GitHub creado para las pruebas. Los repositorios listados como soporte para las pruebas a ejecutar, ya cuentan con algunas incidencias reportadas en ellos.
### Primera semana: 
El repositorio donde se encuentra el inventario de las pruebas  manuales y los issues encontrados en esta etapa es el siguiente: https://github.com/asantaba/ghost-issues. En el, el documento https://github.com/asantaba/ghost-issues/blob/main/inventario-pruebas-exploratorias-ghost.ods registra el inventario de pruebas manuales elaboradas en la primera semana. <br>

1. Configuración de máquinas virtuales para pruebas: Los ingenieros crean una máquina virtual con el sistema operativo Ubuntu 20.04, y cargan sobre esta todos los programas necesarios para ejecutar las pruebas: ghost v3.42.5, ghost v3.3.0 (para VRT), se instala node y npm, y se carga el repositorio que contiene los scripts y la programación de las pruebas de la versión anterior de ghost bajo pruebas (git clone). Se instalan las librerías necesarias y se comprueba que todo esté ejecutándose correctamente sobre la máquina (Cada ingeniero dedicará 2 horas para hacer esta labor sobre sus máquinas). En este tiempo, a uno de los ingenieros se le encarga la labor de inicializar en GitHub un repositorio para las pruebas.
2. Pruebas de reconocimiento manuales, a nivel de sistema, tipo caja negra, sobre ghost v3.42.5. Los ingenieros dedican el resto de las horas de la semana a esta labor (6 horas por cada ingeniero automatizador). 
### Segunda semana:
El repositorio del código con las pruebas es el siguiente: https://github.com/anderson0365/pruebasReconocimiento <br>
1. Exploración automatizada mediante RIPuppet, a nivel sistema, tipo positivo. Cada ingeniero ejecutará la aplicación RIPuppet sobre el ghost v3.42.5. Se busca que la aplicación se configure de tal forma que alcance la mayor cantidad de nodos durante la exploración (2 horas por cada ingeniero). 
2. Reconocimiento automatizado mediante monkeys en cypress, a nivel sistema, tipo caja negra. Los ingenieros deberán consolidar y listar el conjunto de URL alcanzadas por la aplicación RIPuppet, para repartirlas de forma equitativa. Posteriormente, cada ingeniero, con su lista de URL, ejecutará repetidas veces el cypress-monkey de tal forma que los monkeys se inicien desde las URL de su lista. El ingeniero deberá configurar los parámetros de ejecución del cypress-monkey, y de ser necesario, el script, para que inicie su ejecución desde las URL que a este le correspondan probar. En el tiempo asignado, se deberá como mínimo haber corrido una vez el cypress-monkey iniciando desde cada una de las URL (6 horas por cada ingeniero). 
### Tercera y cuarta semana: 
El repositoria del código asociado a las prueba es el siguiente: https://github.com/anderson0365/escenariosPruebasCypressE2E <br>
1. Ejecución de pruebas e2e de versión anterior de ghost (pruebas positivas, a nivel de sistema, automatizadas): Se ejecutan las pruebas e2e elaboradas en Cypress, para la versión 3.3.0, sobre la versión 3.42.5. Se valida que los escenarios programados se ejecuten correctamente. Si los escenarios de pruebas son fallidos debido a los cambios en la nueva versión, se deberán hacer los ajustes de código necesarios para lograr su correcta ejecución. Los ingenieros se reparten equitativamente los escenarios para hacer esta labor. Deberán ejecutar repetidas veces los escenarios programados, y hacer los ajustes necesarios, con la finalidad de reducir al máximo los  “flaky test”. Se les da a los ingenieros 2 semanas con la finalidad de que si les sobra tiempo luego de haber probado y analizados los escenarios ya creados, puedan generar nuevos escenarios de pruebas (16 horas por cada ingeniero). 
### Quinta Semana: 
El repositorio del código con las pruebas es el siguiente: https://github.com/andres-benavides-andes/escenariosPruebasCypressE2E <br>
1. VRT con Resemble JS: Los ingenieros se reparten de forma equitativa, los escenarios de pruebas programado en cypress configurados con las toma automática de screenshots, para su respectivo análisis con Resemble JS. Se hace el VRT de la aplicación ghost v3.42.5 respecto a la v3.3.0 (8 horas por cada ingeniero). 
### Sexta y séptima semana:
El repositorio del código con las pruebas es el siguiente: https://github.com/anderson0365/randomValueTest 
1. Pruebas con valores aleatorios (Nivel: Sistema, Técnica: Automatizada (API), Tipo: Positivas y Negativas): Para la validación de los formularios de la aplicación con pruebas positivas y negativas, los ingenieros de dividen la labor por grupos de funcionalidad a evaluar, y proceden a la programación y ejecución de las pruebas (16 horas por cada ingeniero). 
### Octava Semana:
1. Discusión de los resultados generales de las pruebas y informe final: Los ingenieros se reúnen para discutir los resultados que obtuvieron durante cada una de las pruebas ejecutadas durante las semanas anteriores. En general, se habla sobre los resultados obtenidos, errores encontrados, mejoras o defectos entre las versión anterior y versión actual, y posibles sugerencias al cliente. Todo esto es condensado en un informe final desarrollado por los ingenieros, el cual se entrega al cliente, junto con el paquete de pruebas (8 horas por cada ingeniero).
