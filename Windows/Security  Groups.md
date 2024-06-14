Es otro [[Security Principals]]. Pueden ser un conjunto de usuarios, máquinas o una mezcla de ambos. Algunos se crean por defecto. Grupos típicos:
	- Domain Admins: tienen privilegio administrativo sobre todo el dominio. Pueden administrar cualquier pc e incluso el [[Domain Controller]].
	- Server Operators: Pueden administrar [[Domain Controller]]s, pero no pueden modificar la pertenencia a grupos.
	- Backup operators: Pueden acceder a cualquier archivo, ignorando permisos. 
	- Account Operators: Pueden crear y modificar otras cuentas del dominio.
	- Domain Users: Incluye todos los usuarios en el dominio.
	- Domain Computers: Incluye todos los pcs del dominio.
	- Domain Controles: Incluye todos los DCs que hay.