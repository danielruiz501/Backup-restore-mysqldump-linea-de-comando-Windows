1. Abrir la terminal

Opción A – CMD

Presionar: Win + R

Escribir: cmd

Pulsar Enter

Opción B – PowerShell

Clic derecho en el botón Inicio

Elegir Windows PowerShell o Terminal

2. Ir a la carpeta donde está mysqldump

Normalmente está en:

C:\Program Files\MySQL\MySQL Server 8.0\bin


En la terminal escribir:

cd "C:\Program Files\MySQL\MySQL Server 8.0\bin"


Y probar que funcione:

mysqldump --version

3. Usar mysqldump (Ejemplo básico)

Para hacer un respaldo de una base de datos:

mysqldump -u root -p ecommerce > ecommerce_backup.sql


Ingresar contraseña y generará el archivo respaldo.sql en la carpeta actual.



4. Exportar mysqldump

Para exportar base de datos en la terminal:

mysql -u root -p ecommerce < ecommerce_backup.sql

