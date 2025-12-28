1. Planificación de la red es clave

Definir previamente el rango IP, las IPs estáticas de los servidores y el rol del DHCP evitó conflictos de red y reprocesos.

Aprendizaje:

Los servidores críticos (AD, DNS, Web) deben usar IP fija.

El cliente debe obtener IP vía DHCP para validar el servicio.

2. Active Directory es el núcleo del entorno

La correcta instalación de AD DS, DNS y DHCP en Windows Server 2016 permitió centralizar la autenticación y administración del entorno.

Aprendizaje:

AD depende fuertemente de DNS; una mala configuración rompe el dominio.

Probar autenticación desde un cliente valida que todo el flujo funcione.

3. Importancia de la virtualización con Proxmox

Proxmox permitió desplegar múltiples sistemas operativos en un solo host, facilitando pruebas, snapshots y recuperación ante errores.

Aprendizaje:

Los snapshots ayudan a experimentar sin miedo.

La red bridge (vmbr0) simplifica la comunicación entre VMs.

4. Integración de servicios heterogéneos

El uso de Ubuntu Server junto con Windows Server demostró cómo pueden coexistir servicios Linux y Windows en la misma red.

Aprendizaje:

Linux es ideal para servicios ligeros como SSH y Web.

La interoperabilidad es común en entornos empresariales reales.

5. Seguridad y buenas prácticas

Configurar accesos remotos (RDP y SSH) resaltó la necesidad de aplicar buenas prácticas de seguridad incluso en entornos de laboratorio.

Aprendizaje:

No exponer servicios innecesarios.

Usar contraseñas seguras y usuarios con permisos controlados.

6. Documentación y evidencias son tan importantes como la implementación

La captura de evidencias y la documentación en GitHub permitió transformar el laboratorio en un proyecto demostrable.

Aprendizaje:

Un proyecto sin documentación pierde valor.

Las evidencias visuales validan el funcionamiento real.

7. Uso de herramientas de diagramación

El uso de diagramas (Packet Tracer y diagramas lógicos) ayudó a entender y comunicar mejor la arquitectura del proyecto.

Aprendizaje:

Diagramar aclara ideas antes de implementar.

Packet Tracer es útil para documentación lógica, no para simular AD real.