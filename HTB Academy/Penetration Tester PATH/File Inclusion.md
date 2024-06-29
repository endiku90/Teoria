Commons places = web templates
Por qué? Porque para hacer que las webs sean dinámicas, se apoyan en una web estática y modifican ciertos campos. 
Por ejemplo, es normal encontrarnos en index.html y que al querer ir a la página *about* veamos *index.html?page=about*, donde veremos una página que usará el mismo template que index pero que tendrá alguna cosa cambiada. Ahí es donde podremos intentar el File Inclusion.

## Local File Inclusion

#### ==El básico es un path traversal.==
Puede tener un prefijo (/languaje/$injec) o una extensión (.php)

Ataques de segundo orden:
En resumen, uno envenena el log y otro usuario intenta sacar ese archivo. Como está envenenado, sacará donde haya apuntado el otro.
P.e. me pongo subo una imagen para mi perfil que se llama ```../../../etc/passwd``` y luego, otro usuario visita mi perfil y ejecuta el log poisoning.


