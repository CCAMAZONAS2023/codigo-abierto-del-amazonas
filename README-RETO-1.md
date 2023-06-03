# Agotando-riquezas-del-Amazonas-videos
Esta guía le permitirá ejecutar la librería para identificar objetos o situaciones en imagenes fragmentadas o videos a partir de inferencias o asociaciones con texto.
# Descripción general
Aunque en Colombia se ha procurado formalizar la extracción de recursos naturales para minimizar el impacto en el ecosistema, la informalidad e ilegalidad continúan siendo problemas que destruyen la riqueza de uno de los territorios más importantes del planeta; la Amazonía.
El equipo “Código Abierto del Amazonas” analizó y documentó algunas de las situaciones y elementos que generan impacto negativo en la región amazónica colombiana y pone a disposición de la Fuerza Aérea Colombiana y de la ciudadanía en general, un repositorio de código abierto que permita desarrollar funcionalidades de manera más ágil para la implementación de soluciones a la problemática planteada.
# Estrategia para el desarrollo del reto
Para el reto 
# Prerequisitos
Máquina: vCPU:16; RAM: 64; Amazon SageMaker Studio; JupyterLab;
# Clonación
Previo a la instalación, el usuario deberpa abrir la terminal $ git clone https://github.com/libgit2/libgit2 y correr el comando para clonar los archivos en la máquina local y poder instalar la librería.
# Instalación
a.	El usuario deberá instalar las dependencias de código abierto:
•	segment-geospatial;
•	groundingdino-py;
•	leafmap; y
•	localtileserver”.
Para ello deberá ingresar en la línea de código, lo siguiente: %pip install segment-geospatial groundingdino-py leafmap localtileserver
b.	Finalizada la instalación, se importarán las dependencias a utilizar.
# Ejecución
El usuario podrá cargar los fotogramas de su elección para poder realizar las inferencias.

La configuración de la clase langSAM puede tardar unos minutos, como quiera que con ella se configuran los pesos del modelo y se establecen los lineamientos para establecer las inferencias o asociaciones.

El usuario deberá ingresar el texto para realizar el procesamiento que permita identificar el elemento en interés que se encuentre en el fotograma.

Se sugiere introducir el texto en idioma inglés para mayor precisión en la asociación e identificación en la imagen, ej: si desea identificar un lago, introduzca “lake”, máquina “machine” o “engine”, edificaciones "building", carros "car", excavadora "digger", lancha “boat”, muelle “pier”, entre otros.
# Definición de parametos para ubicación
Este modelo permite establecer parámetros apropiados para la detección de objetos y la asociación de texto con los objetos detectados. Estos valores van de 0 a 1 y se establecen al llamar al método de predicción de la clase LangSAM.

box_threshold: este valor se utiliza para la detección de objetos en la imagen. Un valor más alto hace que el modelo sea más selectivo, identificando solo los objetos más confiables, generando menos detecciones generales. Por el contrario, un valor más bajo hace que el modelo sea más tolerante, lo que lleva a un aumento de las detecciones, incluidas las potencialmente menos seguras.

text_threshold: este valor asocia los objetos detectados con el mensaje de texto proporcionado. Un valor más alto requiere una asociación más fuerte entre el objeto y el mensaje de texto, lo que lleva a asociaciones más precisas, pero con menores resultados. Un valor más bajo permite asociaciones más flexibles, lo que podría aumentar el número de asociaciones pero también introducir coincidencias menos precisas.

Se recomienda al usuario probar diferentes valores dentro de los parámetros establecidos para los datos específicos, aclarando que el umbral óptimo puede variar según la calidad y la naturaleza de sus imágenes, así como la especificidad de sus mensajes de texto.

# Visualización
Una vez ejecutados los parámetros para la identificación o detección de objetos, el usuario podrá visualizar los resultados estableciendo cuadros delimitantes en el fotograma.

# Construido con
Ffpmg y redes neuronales
# Autores
Equipo "Código Abierto del Amazonas" Alejandro Ortiz Tique; Brayan Steven Martínez Toro; Maritza Alejandra Aguirre Fuentes; Mayra Alejandra Luna Ortíz.
# Licencias
Licencia de código abierto permisiva - Apache
# Agradecimientos
Agradecemos a la Fuerza Aérea Colombiana y a la Universidad de los Andes por la oportunidad de desarrollar este ejercicio en el marco del CodeFestADASTRA2023
