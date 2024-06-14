Esta es una vulnerabilidad que surge cuando una aplicación no restringe bien el acceso a ciertos datos o ciertas funciones.
Es decir, si se da esta vulnerabilidad se podría acceder a datos de otros usuarios o a funcionalidades especiales de la aplicación que están solo disponible para algunos usuarios (p.e. premium).

## Access Control:
Mecanismo usado para que usuarios o sistemas puedan acceder a ciertos recursos. 
### tipos de control de acceso:
	- Discretionary Access Control (DAC): El resource manager o el administrador decide a qué recursos se puede acceder y qué acciones se pueden hacer sobre éstos. 
	- Mandatory Access Control (MAC): El acceso a recursos o datos se establece mediante póliticas y reglas. Típico en entornos militares.
	- Role-based Access Control (RBAC): Sistema de roles. Dependiendo del rol tienes o no acceso a ciertos recursos. Típico en entornos empresariales.
	- Attribute-based Access Control (ABAC): El accesso se otorga en función de ciertos atributos que pueden ser temporales o situacionales. Por ejemplo, rol del usuario, device que está usando, lugar desde donde se conecta, etc.


### Mitigación:

	- Implementar sistema de roles.
	- Usar peticiones parametrizadas. 
	- Uso adecuado de sesiones. 