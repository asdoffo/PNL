Para el desafio 2 utilice este dataset: https://www.kaggle.com/datasets/juanagsolano/spam-email-from-enron-dataset

Desafio 3:
Buenas tardes profesor, le adjunto el link del desafío 3.
En este desafío, creo que no pude hacer mucho. Tuve algunos inconveninentes y no lo logré hacer todas la pruebas que pensaba.

Con Colab, el uso de T4 esta muy restringido y me permite hacer solo unas pruebas por día.
Cambie el corpus y coloque el texto de La Biblia, no poque sea religioso, se me ocurrio por ser un libro disponible en la red y de gran extensión.
Y me encontre que rapidamente sobrepasaba la RAM de Colab. Por eso verá que me quede con la decima parte del texto.

Asimismo tambien tuve muchos problemas con la RAM, al terminar la época 1 se desbordaba.

Por eso reduje el batch size.

Con T4 cada época demora unos 6 minutos, con CPU demoran 25min, y es bastante complicado hacer pruebas variando parámetros con esos tiempos.

Por eso no pude hacer lo que pensaba, que era hacer un cuadro comparativo.

Finalmente, verá estos cambios:

- Cambie la capa SimpleRNN a una LSTM. Le puse 150 neuronas.
- En esta capa, cambie los dropout desde 0.1 a 0.2
- Cambie el optimizador a Adam
- Fije el max_context_size = 80
- Deje en entrenamiento en 10 épocas, ya que sino demoraba mucho y no podria hacer cambios
- Modifique la fucnión: def on_epoch_end(self, epoch, logs=None) para que procese los datos por batch

Así como quedo, puede ejecutar el entrenamiento.

