Cómo Usar el Archivo de Configuración (config.yaml)
Ubicación del Archivo

El archivo config.yaml debe estar ubicado en el directorio raíz del proyecto.

Estructura del Archivo A continuación, se muestra un ejemplo de cómo debería verse el archivo config.yaml:

yaml
Copiar código
ocr:
  tesseract_path: "C:\\Program Files\\Tesseract-OCR\\tesseract.exe"
  psm: 6
  whitelist: "0123456789."

image_processing:
  x_min: 200
  x_max: 900
  y_min: 700
  y_max: 900

model_training:
  img_size: 128
  batch_size: 64
  epochs: 20

evaluation:
  ground_truth: "2024.11.14"
Descripción de los Parámetros

OCR:

tesseract_path: Ruta al ejecutable de Tesseract OCR en tu sistema.
psm: Modo de segmentación de páginas para el OCR.
whitelist: Lista de caracteres permitidos para el reconocimiento de texto.
Image Processing (Procesamiento de Imágenes):
x_min, x_max, y_min, y_max: Coordenadas que definen la región de interés (ROI) en la imagen.

Model Training (Entrenamiento del Modelo):

img_size: Tamaño de las imágenes para entrenamiento.
batch_size: Tamaño de los lotes de datos.
epochs: Número de épocas para entrenar el modelo.

Evaluation (Evaluación):
ground_truth: Texto de referencia para evaluar la precisión del reconocimiento OCR.

Editar el Archivo
Abra config.yaml con cualquier editor de texto (por ejemplo, VS Code, Notepad++, o un editor integrado como nano o vim).
Cambie los valores según sus necesidades específicas.

Ventajas del Uso de YAML
Flexibilidad: Facilita la personalización de parámetros clave.
Reusabilidad: Permite mantener un código base genérico para diferentes configuraciones.
Simplicidad: Es fácil de leer y escribir incluso para usuarios sin experiencia técnica.
