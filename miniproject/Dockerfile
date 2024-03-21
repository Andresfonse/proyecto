# Usa una imagen base de Python
FROM python:3

# Establece el directorio de trabajo en /app
WORKDIR /app

# Copia el archivo requirements.txt al directorio de trabajo
COPY requeriments.txt .

# Instala las dependencias del proyecto
RUN pip install -r requeriments.txt

# Copia el contenido del directorio actual al directorio de trabajo del contenedor
COPY . /app

# Expone el puerto 2927
EXPOSE 2927

# Comando para ejecutar el servidor Django
CMD ["gunicorn", "--bind", "0.0.0.0:2927", "miniproject.wsgi:application"]
