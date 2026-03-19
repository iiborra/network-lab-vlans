## Análisis de tráfico (802.1Q)

Se ha realizado una simulación en Packet Tracer para observar el comportamiento de las tramas al atravesar un enlace trunk.

### Observaciones

- El tráfico ICMP generado desde un host llega al switch sin etiqueta VLAN.
- Al salir por el puerto trunk, el switch añade una etiqueta 802.1Q.
- Esta etiqueta permite identificar la VLAN del tráfico en el enlace entre switches.

### Detalles técnicos

- Tipo de encapsulación: 802.1Q
- TPID: 0x8100
- El frame incluye el identificador de VLAN correspondiente

### Trama construida

![Frame](images/8021q-frame.png)

### Resultado

Se confirma que el enlace trunk está funcionando correctamente, permitiendo el transporte de múltiples VLANs entre switches.

Test ping
![Trunk-ping](images/trunk-ping.png)