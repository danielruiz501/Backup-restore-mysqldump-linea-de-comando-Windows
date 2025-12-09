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



3. Backup de todas las bases de datos

Para hacer un respaldo de todas las bases de datos escribir en la linea de comando el nombre usuario, el espacio para la contraseña, la ruta donde se guardara el archivo con todas las bases de datos y un nombre para el archivo. Se solicitara la contraseña:
mysqldump -uroot -p -all-databases > "C:\MyBackups\alldb.sql"


4. Backup de una base de datos

Para hacer un respaldo de una base de datos escribir en la linea de comando el nombre usuario, el espacio para la contraseña, la ruta donde se guardara el archivo con la base de datos y un nombre para el archivo. Se solicitara la contraseña:
mysqldump -uroot -p -all-databases > "C:\MyBackups\ecommercebackup.sql"


5. Restaurar base de datos
Para resturar una base de datos hay que crear un nueva base datos desde MySQL Workbench o MySQL Command Line y dejarla vacia, despues abrir una linea de comando en Windows. Ingresar el nombre de usuario, el espacio para la contraseña, el nombre de esta nueva base de datos y la ubicaciòn donde se encuentra el archivo. Se solicitara la contraseña:

mysqldump -uroot -p restoreecommerce < C:\MyBackups\ecommercebackup.sql


7. Backup de una sola tabla

Para hacer un respaldo de una tabla de una base de datos escribir en la linea de comando el nombre usuario, el espacio para la contraseña, el nombre de la base de datos que se quiere respaldar, el nombre de la tabla y un nombre para el archivo de la tabla. Se solicitara la contraseña:

mysqldump -uroot -p ecommerce custommers > "C:\MyBackups\customersbackup.sql"


7. Restaurar una tabla
Para restaurar una sola tabla hay que crear un nueva base datos desde MySQL Workbench o MySQL Command Line y dejarla vacia, despues abrir una linea de comando en Windows. Ingresar el nombre de usuario, el espacio para la contraseña, el nombre de esta nueva base de datos y la ubicaciòn donde se encuentra el archivo. Se solicitara la contraseña:

mysqldump -uroot -p restoreecomerce < C:\MyBackups\customersbackup.sql




