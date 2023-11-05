# Formas básicas de interrumpir la ejecución de un proceso en Linux

1. **Cierre ordenado**: En un entorno gráfico, como el ejemplo de Emacs, puedes cerrar un proceso de manera ordenada haciendo clic en el botón de cierre de la aplicación. Esto finaliza el proceso adecuadamente.

2. **Cierre no ordenado (interrupción propiamente dicha)**: La forma más básica de interrumpir un proceso en Linux es utilizando la combinación de teclas `Control+C`. Esto provoca la interrupción abrupta del proceso en ejecución.

3. **Suspensión de un proceso**: Puedes suspender un proceso en ejecución utilizando la combinación de teclas `Control+Z`. Esto detiene el proceso y lo coloca en un estado de pausa o segundo plano, donde no puede recibir eventos o entradas. Esto puede ser útil para detener temporalmente un proceso que consume muchos recursos sin terminarlo por completo.

4. **Reanudar un proceso en segundo plano**: Puedes reanudar un proceso suspendido en segundo plano utilizando el comando `bg`. Esto hará que el proceso continúe su ejecución, y puedes volver a interactuar con la aplicación gráfica si es relevante.

La suspensión y reanudación de procesos en segundo plano pueden ser útiles para gestionar la ejecución de múltiples procesos en una terminal y permitir que otros procesos consuman recursos cuando sea necesario.

Este es solo un resumen de los conceptos básicos relacionados con la interrupción de procesos en Linux. Más adelante, puedes explorar señales y otras formas avanzadas de gestionar procesos 