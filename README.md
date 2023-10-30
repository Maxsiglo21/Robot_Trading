# Robot_Trading
Este Robot Traiding intenta ser capaz de tomar decisiones de compra y venta de Bitcoinhttps://github.com/Maxsiglo21/Robot_Trading/blob/main/README.md


Este es mi primer desafío en la programación con el lenguaje Python gracias a los conocimientos adquiridos en Alura para realizar este proyecto de un Robot Traiding que sea capaz de tomar decisiones de compra y venta de Bitcoin en tiempo real. 
Python es un lenguaje de alto nivel y adecuado para recopilar datos con Web Scraping. 
Se han utilizado bibliotecas, para analizar y extraer los datos de documentos HTML y XML con los métodos y funciones que esas bibliotecas proporcionan para localizar y extraer los datos de la web.
Scrapy es un framework de Python para Web Scraping que proporciona una serie de funcionalidades y herramientas que facilita el trabajo de rastrear el código de la web
El proceso fue realizado siguiendo los siguientes pasos:
1.- Configuración del ambiente: Comenzamos a utilizar un entorno virtual como Google Colaboratory, asegurándonos de tener instalada la versión Python 3.x o superior en nuestra computadora, que es esencial para este proyecto.
En el proyecto se usaron cinco variables que serán definidas como globales. También se necesita instalar algunas librerías de Python que son esenciales para este proyecto como Pandas, Numpy, Matplotlib, etc.
Debemos asegurarnos de tener nuestro ambiente listo y en forma ejecutando líneas de código para comprobar que todas las bibliotecas utilizadas sean las compatibles.
2.- Obtención de los datos: Creamos la función para importar la base de bitcoin, dentro de la cual definimos las variables globales
Se utiliza la biblioteca yfinance de Python para extraer el histórico de precios del Bitcoin en dólares de los últimos siete días en intervalos de cinco minutos. Este histórico es guardado en un dataframe
Utilizamos la biblioteca BeautifulSoup para el Web Scraping de la página https://coinmarkercap.com/ para obtener el precio actual del Bitcoin en dólares y la variación de su precio en la última hora, la que se guarda en una variable “precio_actual”. En la variable “tendencia” se guarda el valor ‘baja’ si la variación del precio es negativa, sino se guarda el valor ‘alta’.
3.- Limpieza de datos: En la función “limpieza_datos()” definimos las variables globales con sus códigos.
Antes de limpiar la base, se crea una copia de esta para que se pueda realizar la limpieza sin modificar la base original, además de entender su contenido.
Para la limpieza se utilizan los atributos “Datatime”, “Close” y “Volume”.
Se analiza la base limpia, identifica duplicados en el índice y se tratan para quedar con índices únicos.
Se tratan los valores nulos en la columna ‘Close’ y ‘Volume’
Verificar que todos los registros de la base tengan un ‘Volume’ de transacción mayor a cero, caso contrario, se eliminan.
Se identifican y eliminan los outliers en el precio del Bitcoin en la columna ‘Close’, y se utiliza un gráfico boxplot para identificarlos
Se filtran e identifican los registros cuyos precios ‘Close’ se encuentren dentro del primer y tercer cuartil del boxplot
Finalmente se calcula el precio promedio de ‘Close’ y se guarda en variable media_bitcoin.
4.- Tomar decisiones: El momento de generar la función ‘tomar_decision’,  con las variables globales y construimos el algoritmo de decisión
Este algoritmo de decisión es simple, que ayuda a los clientes inexpertos a conocer el mejor momento de comprar, vender o esperar para operar el Bitcoin 
5.- Visualización: En la función ‘visualización()’ definimos nuevamente las variables globales, adicionamos una nueva columna (promedio) al dataframe original y almacena el valor de nuestra ‘media_bitcoin’.
Configuramos el tamaño del gráfico
Adicionamos el título del gráfico
Usamos el método plot() para dibujar una línea del gráfico con los datos del índice y la columna ‘Close’ de la base df_bitcoin
Dibujamos el promedio de la base de datos
Mostramos el mensaje de la decisión del algoritmo con el método ‘annotate()’
Finalmente, mostramos el gráfico que acabamos de configurar con el método ‘show()’
6.- Automatización: El trabajo de un Data Scientist sólo termina cuando la solución al problema está automatizada, esto permite soluciones automáticas para nuevos lotes de información.
El resultado de este código será un gráfico mostrando el histórico de precios del Bitcoin y la decisión del algoritmo en tiempo real, basado en datos normalizados y limpios, que se actualizarán cada cinco minutos.
Conclusión: 
Este desafío sólo fue una demostración de un proyecto real, donde vemos el poder de los datos para la toma de decisiones y la importancia que tiene el tratamiento de los datos para evitar tomar decisiones equivocadas.
Todavía me falta un camino para adquirir nuevas herramientas y habilidades para lograr llevar este proyecto a un nuevo nivel.


 #aluraChallengeRobotTrading.*
