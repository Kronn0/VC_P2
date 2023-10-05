# VC_P2

**TAREA 1: Realiza la cuenta de píxeles blancos por filas, determina el máximo para filas y columnas (uno para cada) y muestra el número de valores que superan en cada caso 0.95*máximo.**

 Basicamete como en el ejemplo anterior, hemos hecho lo mismo pero hemos medido los pixeles blancos de las filas. Hemos hecho la grafica. Luego hemos cogido tanto la columna como las filas y hemos calculado el Maximo de cada uno, y hemos recorrido los arrays buscando los valores que sean mayor o igual que Maximo*0.95.


**TAREA 2: Elige otra imagen, muestra el contenido de alguna de las imágenes resultado de Sobel antes y después de ajustar la escala**

Basicamente enseñamos la nueva imagen (es una portada del Kingdom Hearts 2) primero la hemos mostrado, luego la hemos pasado a una escala de grises y luego hemos cogido el ejemplo del sobel y hemos puesto nuestra foto a escala de grises.

**TAREA 3: Aplica umbralizado a la imagen resultante de Sobel (valores 0 a 255 y convertida a 8 bits por ejemplo sobel8 = np.uint8(sobel)), y posteriormente realiza el conteo por filas y columnas similar al realizado en el ejemplo con la salida de Canny. Calcula los máximos por filas y columnas, y determina las filas y columnas por encima del 0.95*máximo. Remarca con alguna primitiva gráfica dichas filas y columnas sobre la imagen ¿Cómo se comparan los resultados obtenidos a partir de Sobel y Canny?**
 
 Hemos covertido a 8 bits el ejemplo del sobel, para luego sobre esta aplicar el umbralizado a un umbral de 125. Luego hemos contado los pixeles blancos tanto en las columnas como en las filas y las hemos mostrado graficamete como en la primera Tarea. 

 Luego hemos cogido tanto la columna como las filas y hemos calculado el Maximo de cada uno, y hemos recorrido los arrays buscando los valores que sean mayor o igual que Maximo*0.95.


**TAREA 4: Asumiendo que quieren mostrar a personas que no forman parte del curso de VC el comportamiento de una o varias funcioens de las vistas hasta este momento aplicadas sobre la entrada de la webcam. ¿Cuál(es) escogerían?**

Hemos reutilizado el filtro de la tarea 4 de la primera semana, ya que es interesante y sorprende a la visa de personas.

Se ha hecho un cambio del espacio del color BGR -> HSV para poder jugar con la saturación de los colores y así poder aislarlos dentro de un rango que se ha definido. Luego se realiza una operacion AND a cada bit de cada color para así crear una máscara que luego se aplicará al frame y dará como resultado el aislamiento de cada color. Se presenta con tres ventanas, una normal de la cámara, otra con la máscara y la última con la máscara aplicada al frame para una sencilla comparación.

Fuente de la idea: https://docs.opencv.org/4.x/df/d9d/tutorial_py_colorspaces.html

**TAREA 5: Asumiendo que quieren mostrar a personas que no forman parte del curso de VC el comportamiento de una o varias funcioens de las vistas hasta este momento aplicadas sobre la entrada de la webcam. ¿Cuál(es) escogerían?**

IMPORTANTE: Es necesario installar pyautogui en el enviaroment de la practica para que funcione.

 En esta tarea hemos creado una forma nueva y divertida (quizás) de jugar al juego del dinosaurio del Chrome cuando no tienes conexión a internet. 
  Para ello hemos creado un subframe en el que usando la mano podremos controlar si el dinosaurio salta o no. Esto lo hemos conseguido aplicando una máscara para reconocer la mano (utilizando un fondo blanco para que la detección sea más eficaz), aplicando correción de ruido para poder encontrar los bordes y luego utilizando estos para calcular el área que crean y así poder determinar si la mano está abierta o cerrada. Para convertir los inputs de la mano en inputs en el propio ordenador hemos usado la librería pyautogui que hace muy sencillo este proceso.
  Recomendación: Abrir el juego en el navegador, ejecutar el programa y cambiar a la ventana del juego para que los inputs los detecte el navegador.

  Documentación de OpenCV
  https://github.com/SinghalHarsh/OpenCV-Projects/tree/master
