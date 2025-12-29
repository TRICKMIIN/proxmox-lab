# proxmox-lab
Laboratorio de infraestructura virtualizada desplegado sobre **Proxmox VE**, orientado a la simulación de un entorno empresarial pequeño con servicios centralizados de red, autenticación y administración remota.

El proyecto valida la integración de sistemas **Windows y Linux** dentro de una misma infraestructura virtualizada.

---

## 🔧 Alcance del Proyecto

Este laboratorio cubre los siguientes componentes técnicos:

- Virtualización de servidores mediante **Proxmox VE**
- Implementación de **Active Directory** como servicio de identidad
- Configuración de **DNS y DHCP** centralizados
- Integración de clientes Windows al dominio
- Servicios Linux para acceso remoto y web
- Pruebas de conectividad y validación de servicios

---

## 🧩 Componentes de Infraestructura

### Hipervisor

| Componente        | Detalle          |
|------------------|------------------|
| Plataforma        | Proxmox VE       |
| Tipo de red       | Bridge           |
| Interfaz de red   | `vmbr0`          |
| Segmento de red   | `192.168.3.0/24` |

---

### Máquinas Virtuales

| Nombre de la VM      | Sistema Operativo   | Dirección IP        | Servicios Principales              | Rol Técnico                                   |
|---------------------|---------------------|---------------------|------------------------------------|-----------------------------------------------|
| Windows Server 2016 | Windows Server 2016 | 192.168.3.18        | AD DS, DNS, DHCP, RDP              | Controlador de dominio y servicios de red     |
| Ubuntu Server       | Ubuntu Server       | 192.168.3.16        | SSH, Servidor Web (Apache)         | Servidor Linux de servicios                   |
| Windows 7 Client    | Windows 7           | Asignada por DHCP   | Cliente de dominio                 | Estación de trabajo del dominio               |

---

## 🌐 Configuración de Red

| Parámetro              | Configuración                               |
|------------------------|---------------------------------------------|
| Gateway                | Proxmox / Red local                         |
| Segmento de red        | `192.168.3.0/24`                            |
| Asignación IP          | Estática (servidores) / Dinámica (clientes)|
| Servicio DHCP          | Windows Server 2016                         |
| Servicio DNS           | Windows Server 2016                         |
| Método de conexión     | Bridge (`vmbr0`)                            |

---

## 🧪 Validaciones Técnicas

Las siguientes pruebas fueron realizadas para verificar el correcto funcionamiento del entorno:

- Conectividad ICMP entre todas las máquinas
- Resolución DNS interna
- Asignación correcta de direcciones IP por DHCP
- Autenticación de usuarios de dominio
- Acceso remoto vía RDP
- Acceso SSH al servidor Ubuntu
- Acceso HTTP al servidor web

---

## 📚 Propósito del Laboratorio

Este laboratorio fue creado con fines **educativos y de demostración técnica**, orientado a:

- Práctica de administración de sistemas
- Simulación de entornos corporativos
- Desarrollo de habilidades en infraestructura IT
- Presentación como proyecto de portafolio técnico