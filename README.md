# TECLADO-IA
# Teclado Virtual por Gestos y IA

Prototipo de un teclado virtual controlado por gestos manuales y un modelo de lenguaje predictivo, desarrollado para la materia de Inteligencia Artificial en la Universidad Veracruzana.

``

## Descripción

Este proyecto ofrece una solución de accesibilidad para personas con discapacidad motriz, permitiendo la entrada de texto en una computadora utilizando únicamente una cámara web. El sistema interpreta los gestos de la mano para controlar un puntero y seleccionar teclas, y utiliza un modelo de lenguaje (trigramas) para sugerir palabras y acelerar la escritura.

## Características Principales

- **Control sin Contacto:** Usa la punta del dedo índice para mover el puntero.
- **Selección por Permanencia:** Selecciona una tecla manteniendo el puntero sobre ella por 1 segundo.
- **Predicción de Texto:** Un modelo de trigramas sugiere hasta 3 palabras para autocompletar.
- **Gesto de Borrado Rápido:** Muestra la palma abierta a la cámara para borrar todo el texto.
- **Retroalimentación Audiovisual:** Resaltado de teclas y sonido de clic para confirmar acciones.

## Pila Tecnológica (Tech Stack)

- **Lenguaje:** Python 3
- **Visión por Computadora:** OpenCV, MediaPipe
- **Modelo de Lenguaje:** Modelo N-Gram (Trigramas) entrenado con un corpus propio.
- **Sonido:** Pygame

## Instalación y Ejecución

Sigue estos pasos para ejecutar el proyecto en tu máquina local.

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/TU_USUARIO/teclado-virtual-ia.git](https://github.com/TU_USUARIO/teclado-virtual-ia.git)
    cd teclado-virtual-ia
    ```

2.  **Crea y activa un entorno virtual:**
    ```bash
    python -m venv env
    # En Windows
    env\Scripts\activate
    # En macOS/Linux
    source env/bin/activate
    ```

3.  **Instala las dependencias:**
    (Primero, crea un archivo `requirements.txt` en tu máquina con el comando `pip freeze > requirements.txt` y súbelo a GitHub)
    ```bash
    pip install -r requirements.txt
    ```

4.  **Entrena el modelo de lenguaje:**
    (Asegúrate de que `corpus.txt` esté en la carpeta)
    ```bash
    python entrenar_trigramas.py
    ```
    Esto creará el archivo `modelo_trigramas.pkl`.

5.  **Ejecuta la aplicación principal:**
    ```bash
    python teclado_virtual.py
    ```
    Presiona la tecla `ESC` para salir.

## Uso

- **Apuntar:** Mueve tu dedo índice frente a la cámara.
- **Escribir:** Mantén el puntero sobre una tecla por 1 segundo.
- **Borrar Todo:** Muestra la palma de tu mano abierta a la cámara.
