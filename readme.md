# API envio de correos
La API permite a todos los usuarios enviar correos electrónicos con una solicitud HTTP a través del  método POST.Esta API está configurada para recibir datos en  JSON y enviar un correo electrónico al webmaster.
## Cómo hacer la solicitud
### Formato
La solicitud debe ser de tipo POST y el código debe  estar en formato JSON.
### Cuerpo de la Solicitud
```json
POST http://dominio/api/v1/endpoint-webservice/
Content-Type: "application/json"
{
"name": "desconocido",
"email": "tandemrobertoaranjuez@gmail.com",
"message": "Hola Roberto."
}
```
# Respuestas recibidas
### Respuesta con exito
Cuando  los datos están  ya rellenados y son correctos, la respuesta es exitosa y se muestra así:
````json
{
"status": "success",
"message": "Correo enviado correctamente."
}
````
### Respuesta  no válida
Cuando los datos están incompletos o no son correctos se devuelve esta respuesta:
````json
{
"status": "error",
"message": "Datos inválidos."
}
````
### Respuesta  Error
Cuando hay un error de conexión con el servidor la respuesta que devuelve es la siguiente:
````json
{
"status": "error",
"message": "Error al enviar el correo."
}
````












