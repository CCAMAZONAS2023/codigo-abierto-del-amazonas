# Agotando-riquezas-del-amazonas
Esta guía le permitirá ejecutar la librería para identificar entidades nombradas en bases de datos de noticias. Este ejercicio se desarrolló con información sobre noticias de la amazonía
# Descripción general
Aunque en Colombia se ha procurado formalizar la extracción de recursos naturales para minimizar el impacto en el ecosistema, la informalidad e ilegalidad continúan siendo problemas que destruyen la riqueza de uno de los territorios más importantes del planeta; la Amazonía.
El equipo “Código Abierto del Amazonas” analizó y documentó algunas de las situaciones y elementos que generan impacto negativo en la región amazónica colombiana y pone a disposición de la Fuerza Aérea Colombiana y de la ciudadanía en general, un repositorio de código abierto que permita desarrollar funcionalidades de manera más ágil para la implementación de soluciones a la problemática planteada.
# Estrategia para el desarrollo del reto
a.	Se revisa que la base de datos suministrada esté completa. Al identificar que no está completa se realiza el registro de los datos faltantes y se organiza la información incluyendo formato y tipología.
b.	Se identifican en la base de datos las noticias relevantes para el reto, es decir aquellas relacionadas con deforestación, contaminación y minería. Adicionalmente se revisó el contenido de las mismas para evitar descartar información relevante. Se organizan las categorías de afectación incluyendo una denominada “otros” donde se compilan las demás tipologías que puedan identificarse con el código.
c.	Se convierte el archivo a formato .csv para efectuar el procesamiento en el código
# Prerequisitos
Máquina:
vCPU:16;
RAM: 64;
Amazon SageMaker Studio;
JupyterLab;
# Clonación
Previo a la instalación, el usuario deberpa abrir la terminal $ git clone https://github.com/libgit2/libgit2 y correr el comando para clonar los archivos en la máquina local y poder instalar la librería.
# Instalación
El usuario deberá instalar la librería spaCy. Adicionalmente, se importará Displacy, un módulo especial de spaCy para la visualización.

A continuación, el usuario deberá descargar el modelo en español (es_core_news_md), que procesará y hará predicciones los textos contenidos en las bases de datos.
# Ejecución 
Todas las entidades con nombre de nuestro documento se encuentran en la propiedad document.ents.

Para cada `entidad_con_nombre` en `document.ents`, el usuario podrá extraer la `entidad_con_nombre` y su correspondiente `entidad_con_nombre.label_`.

Para extraer sólo las entidades con nombre que se han identificado como `PER` (persona), el usuario podrá añadir una simple sentencia `if` a la descripción:
# Construido con
Spacy on Python
# Autores
Equipo "Código Abierto del Amazonas"
Alejandro Ortiz Tique;
Brayan Steven Martínez Toro;
Maritza Alejandra Aguirre Fuentes;
Mayra Alejandra Luna Ortíz.
# Licencias
Licencia de código abierto permisiva - Apache
# Agradecimientos
Agradecemos a la Fuerza Aérea Colombiana y a la Universidad de los Andes por la oportunidad de desarrollar este ejercicio en el marco del CodeFestADASTRA2023
