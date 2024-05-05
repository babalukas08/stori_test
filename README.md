Stori Test
Este proyecto es un sistema que procesa un archivo de transacciones bancarias, guarda la información en una base de datos PostgreSQL y envía un resumen de las transacciones por correo electrónico. Utiliza Python para el procesamiento de datos, psycopg2 para la interacción con la base de datos PostgreSQL, y smtplib para enviar correos electrónicos.

Descripción
El proyecto consta de los siguientes componentes:

app/: Contiene el código fuente de la aplicación.
data/: Contiene los archivos CSV de transacciones y usuarios.
docs/: Contiene la documentación relacionada con el proyecto.
.env: Archivo de configuración para variables de entorno.
requirements.txt: Lista de dependencias del proyecto.

Instalación

Para ejecutar el proyecto, sigue estos pasos:

1.- Instalar Python: Si no tienes Python instalado, descárgalo desde python.org. https://www.python.org/downloads/
2.- Instalar PostgreSQL: Si no tienes PostgreSQL instalado, descarga e instala la versión adecuada para tu sistema operativo desde postgresql.org. https://www.postgresql.org/download/
3.- Clonar el repositorio: Clona este repositorio en tu máquina local.

git clone https://github.com/tu_usuario/stori_test.git

4.- Instalar dependencias: Navega al directorio raíz del proyecto y ejecuta el script setup_project.sh para instalar las dependencias.

cd stori_test
chmod +x setup_project.sh
./setup_project.sh

5.- Configurar la base de datos: Ejecuta el script setup_database.sh para crear la base de datos y configurar los permisos.

chmod +x setup_database.sh
./setup_database.sh

6.- Ejecutar el script principal: Una vez instaladas las dependencias y configurada la base de datos, ejecuta el script principal para procesar el archivo de transacciones.

python app/process_file.py data/transactions.csv

Uso
El script process_file.py procesa el archivo CSV de transacciones y guarda la información en la base de datos. El resumen de las transacciones se envía por correo electrónico utilizando la función send_email_summary() del archivo email.py.
