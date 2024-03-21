# Análisis cualitativo de los corpus COREC y COSER utilizando el modelo Whisper y la métrica WER

En este repositorio hemos almacenado los errores cometidos por Whisper Large-v2 en una serie de audios, obtenidos de los corpus COSER (Corpus Oral y Sonoro del Español Rural) y COREC (Corpus Oral de Referencia de Español en Contacto). 

Para cada uno de los audios de los dos dataset hemos descargado la transcripción hecha a mano, disponible en ambos corpus, y hemos transcrito de forma automática, por medio de whisper, el contenido del audio. Después, hemos preprocesado ambos textos para tenerlos escritos sin marcas (anotaciones de los transcriptores, signos de puntuación, etc.). Una vez tenemos los textos limpios, los hemos pasado por la métrica WER (Word Error Rate), que se encarga de decirnos cómo de bien hecha está la transcripción automática, teniendo como referencia la manual. Lo que hace esta métrica es contar el número de palabras eliminadas, insertadas y sustituidas que hay respecto al número total de palabras transcritas. Teniendo esta información como referencia hemos creado el csv errores.csv, que tiene el número de cada uno de estos tipos de errores de todos los audios de los dos corpus. 

Además, hemos visto que algunos de los audios obtienen resultados mucho peores que el resto. En concreto, los audios 01_02_03 y 03_03_05 del COREC y los audios 3308-01 y 1709-01 del COSER. Hemos decidido hacer un análisis más exhaustivo de estos 4 audios, por los que hemos creado una carpeta relativa a cada uno de ellos y allí hemos almacenado distintos archivos: en primer lugar, hemos la transcripción manual y la transcripción automática de cada uno de ellos (llamadas original y transcrito, seguido del nombre del archivo, respectivamente). Después, hemos obtenido un fichero para cada uno de los tres tipos de errores, en el que listamos todas las palabras correspondientes a dichos fallos (para nombrarlos hemos puesto en primer lugar el tipo de error (delete, insert o substitute) seguido del nombre del audio). Por último, podemos encontrar el fichero .ipynb con el que hemos obtenido estos datos.
