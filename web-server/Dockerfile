# ** Los comando de docker se deben ejecutar estando en la carpeta del proyecto **
# Instalo la version de Python que requiere el proyecto
FROM python:3.11.5

# Se debe crear este espacio de trabajo
WORKDIR /app

# Copio el archivo de requerimientos desde mi carpeta local a el contenedor
COPY requirements.txt /app/requirements.txt

# Se ejecuta este comando en el bash del contenedor
RUN pip3 install --no-cache-dir --upgrade -r /app/requirements.txt

# Copio todo lo de mi carpeta local app a la carpeta app del contenedor
COPY . /app

# Esto va a levantar el sercivio en unpuerto especifico para que se consuman los endpoint
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]