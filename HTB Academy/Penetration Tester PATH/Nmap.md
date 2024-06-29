## host discovery

```shell-session
endiku@htb[/htb]$ sudo nmap 10.129.2.0/24 -sn -oA tnet | grep for | cut -d" " -f5
```





`--packet-trace` muestra todos los paquetes mandados y recibidos.

`--PE` to ensure icmp echo requests are sent

`--reason` to know why nmap has marked the host as alive.

`--disable-arp-ping`  (por defecto, nmap detecta si los hosts están vivos con los arp pings)

`-Pn` disable the ICMP echo requests

`--stats-every=5s`  Shows the progress of the scan every 5 seconds.

`--script vuln`  Uses all related scripts from specified category.|

## Firewall and IDS/IPS evasion
IDS = intrusion detection system
IPS = intrusion prevention system

Firewall es una medida de seguridad que controla los intentos de conexión no deseados desde el exterior. Consta de un software que monitorea el tráfico entre el firewall y la información entrante y decide qué permite pasar y qué no basado en reglas previamente establecidas. 

### IDS/IPS
Componentes basadas en software:
	- **IDS** escanea la red en busca de posibles ataques, los analiza y reporta cualquier posible ataque. (p.e. Snort, Suricata, Bro)
	- **IPS** complementa a IDS, toma medidas defensivas si un ataque potencial fuera detectado. El análisis se basa en patrones y firmas.

