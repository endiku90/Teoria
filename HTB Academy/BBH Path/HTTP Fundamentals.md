
# HTTP:

HTTP es un protocolo de la capa aplicación que se utiliza para navegar por internet. En la web se maneja todo con hyperlinks, que significa, textos con links para acceser a recursos.

La comunicación en HTTP consiste en un cliente que solicita al servidor un recurso. Utilizamos FQDN (FullY Qualified Domain Name) como un URL (Uniform Resource Locator) para alcanzar la website deseada. 

A los recursos se accede mediante URL, que tiene un esquema de esta forma:
![[Pasted image 20240203102931.png]]

Los campos necesarios son el schema y el host.

El funcionamiento de HTTP se basa en IPs. La primera vez que buscamos/solicitamos un recurso a una URL, esta petición se translada a un servidor DNS que nos dirá qué IP tiene el dominio que estamos buscando. Después nos regresará la información con la IP, y entonces podremos acceder a la URL. 

Existe una jerarquía. Primero buscará la IP en el archivo  */etc/host*, y después preguntará al DNS Server. 

Una vez mandada la petición, el servidor responderá a la petición. Por defecto, devuelve un archivo *index*.  Después el web browser renderizará la página index. 

# HTTPs 

El principal problema con HTTP es que la transmisión de datos se hace en texto claro. Para subsanar este problema, surge HTTPs, que es prácticamente lo mismo pero con cifrado. Toda página que visitemos que sea HTTPs, el tráfico con esta estará encriptado.

En cambio, si utilizamos un servidor DNS que no tiene encriptación, podemos revelar cierta información, aunque estemos traficando con HTTPs.

El flujo es:
	- Pregunto por HTTP (puerto 80).
	- Me redirigen a HTTPs(puerto 443)
	- Vuelvo a mandar paquete "client hello".
	- Servidor manda "server hello" + [key exchange] para intercambiar certificados SSL.
	- El cliente verifica la clave o el certificado y manda una propia.
	- Después se inicia *handshake* encriptado para verificar que la comunicación funciona y está encriptada.
	- Se inicia la comunicación/tráfico.


## Peticiones y respuestas:

La comunicación HTTP se basa en un cliente/browser que manda una petición y un servidor web que responde (una respuesta).  En la petición, el cliente manda los datos requeridos por el servidor para obtener el recurso buscado. Posteriormente, el servidor comprueba los datos y verifica si tiene autorización para obtener el recurso solicitado.

![[Pasted image 20240204095105.png]]

## Headers:

Cuatro tipos:
	- General: Describe el mensaje, no el contenido.
	- Entity: Describe el contenido. Puede estar en los headers de Response y Request.
	- Request
	- Respond
	- Security

![[Pasted image 20240205071419.png]]
#### General: 
Contextual, describe el mensaje pero no el contenido (p.e. Date, Connection).
Connection: *keep-alive* indica que se quiere seguir mandado datos y *close* para indicar que se cierra ya la conexión.
#### Entity:
Describe el contenido del paquete/mensaje

