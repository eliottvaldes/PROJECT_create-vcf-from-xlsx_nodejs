# Archivo README

Este es un código de Node.js que permite convertir un archivo de Excel en un archivo vCard.

## Requisitos
Para utilizar este código, debe tener instalado Node.js y los siguientes paquetes de npm:
 <!-- coloca los links de las tecnologias y su nombre -->

- [Node.js](https://nodejs.org/es/)
- [Express](https://expressjs.com/es/)
- [ExcelJS](https://www.npmjs.com/package/exceljs)
- [fs](https://www.npmjs.com/package/fs)
- [Multer](https://www.npmjs.com/package/multer)
- [Express Validator](https://www.npmjs.com/package/express-validator)

## Instalación
1. Clone el repositorio en su computadora
2. Abra una terminal y navegue hasta la carpeta del repositorio
3. Ejecute el comando `npm install` para instalar todas las dependencias necesarias
4. Ejecute el comando `npm start` para ejecutar el servidor

## Uso
1. Envíe una petición POST a `http://localhost:3000/export` con un archivo de Excel (solo archivos .xlsx son admitidos)
2. El servidor validará el archivo y, si es válido, lo convertirá en un archivo vCard y lo guardará en el mismo directorio.
3. Recibirá un mensaje de respuesta indicando el nombre del archivo vCard creado.

## Consideraciones importantes
- El archivo Excel debe tener al menos dos columnas: "nombre" y "telefono".
- La primera fila del archivo Excel no debe contener las palabras "NOMBRE", "TELEFONO", "NUMERO" o "CELULAR". De lo contrario, se eliminará esta fila antes de la conversión.
- Si el archivo Excel no contiene datos, se mostrará un error indicándolo.
- Si el archivo subido no cumple con los requisitos mencionados (extensión y tipo MIME), se mostrará un error indicándolo.
- El archivo vCard creado tendrá el mismo nombre que el archivo Excel subido, pero con la extensión .vcf.
