# **Proxmox Infrastructure Lab**

This project involves a virtualized infrastructure lab deployed on **Proxmox VE**. The environment simulates a small corporate network, integrating **Linux and Windows servers**, centralized authentication, network services, and remote administration.

## **Overview**

This project presents a virtualized infrastructure lab deployed on **Proxmox VE**, designed to simulate a basic corporate environment. The lab integrates **Windows and Linux servers**, domain services, automatic IP address assignment, and remote administration.

The primary goal is to demonstrate practical knowledge in virtualization, networking, Active Directory, and technical documentation through a functional and validated environment.

---

## **Objectives**

The objectives of this project are to:

- Implement a virtualized environment using **Proxmox VE**.
- Configure **Windows Server 2016** as the domain controller.
- Implement **Active Directory, DNS, DHCP, and Remote Desktop (RDP)** services.
- Deploy an **Ubuntu Server** with SSH and Web services.
- Join a **Windows 7 client** to the domain.
- Validate connectivity and service functionality.
- Document the infrastructure with diagrams and evidence.

---

## **Architecture**

The infrastructure is hosted on **Proxmox VE**, using a bridge network (`vmbr0`) within the network `192.168.3.0/24`.

Windows Server 2016 acts as the central server, providing domain and network services, while Ubuntu Server provides Linux services. A Windows 7 client consumes the network services via DHCP and authenticates against the domain.

---

## **Virtual Machines**

Here are the virtual machines used in the lab:

### **Ubuntu Server**

| IP Address      | Services          | Role                           |
|-----------------|-------------------|--------------------------------|
| 192.168.3.16   | SSH and Web Server| Linux services server          |

---

### **Windows Server 2016**

| IP Address      | Services                                  | Role                                   |
|-----------------|-------------------------------------------|----------------------------------------|
| 192.168.3.18   | Active Directory services                 | Domain controller and network services|
|                 | DNS, DHCP                                  |                                        |
|                 | Remote Desktop (RDP)                      |                                        |
|                 | Domain: Portafolio.local, User: jose1     |                                        |

---

### **Windows 7 (Client)**

| IP Address      | Configuration                                             | Role                            |
|-----------------|------------------------------------------------------------|---------------------------------|
| Assigned by DHCP| Joined to domain `portafolio.local` with user `Jose1`      | Domain client                   |

---

## **Key Features**

Here are the key features of the infrastructure:

- Virtualized environment using **Proxmox VE** for efficient resource management.
- **Active Directory** implementation for centralized authentication and user management.
- **DNS and DHCP** services configured on Windows Server 2016 to manage network addressing.
- Remote server management using **RDP** (Remote Desktop Protocol).
- **Ubuntu Server** offering **SSH** and **Web** services for remote access and web hosting.
- **Windows 7** client joined to the domain for centralized authentication and network service access.
- Automatic IP assignment to clients via DHCP.
- Seamless integration of **Linux** and **Windows** systems within the same network environment.
- Full documentation with network diagrams and proof of functionality.

---

## **Evidence**

Here are some screenshots showcasing the configuration and functionality of the system:

![Proxmox](../screenshots/PROXMOX.png)

- **Description**: Proxmox VE dashboard showing the virtual machine setup.

![Ubuntu Page](../screenshots/PAGINA-UBUNTU.png)

- **Description**: Web page hosted on the Ubuntu Server.

![Ubuntu IP](../screenshots/UBUNTO-IP.png)

- **Description**: IP address of the Ubuntu Server.

![Ubuntu Ping to WDsv](../screenshots/ping-ubuntu.png)

- **Description**: Ping test from Ubuntu Server to Windows Server 2016 to check network connectivity.

![Active Directory](../screenshots/DOMINIO-WDSV.png)

- **Description**: Active Directory setup on Windows Server 2016.

![IP of WDsv](../screenshots/IP-WDSV.png)

- **Description**: IP configuration of the Windows Server 2016.

![Active Directory Roles](../screenshots/ROLES-WDSV.png)

- **Description**: Roles assigned to Windows Server 2016, such as domain controller, DNS, and DHCP services.

![User Creation](../screenshots/USUARIO-WDSV.png)

- **Description**: User creation in Active Directory for authentication.

![Ping to WDsv](../screenshots/ping-wdsv.png)

- **Description**: Ping test from a client (e.g., Windows 7) to the Windows Server 2016.

![Windows 7 User](../screenshots/USUARIO-WDS7.png)

- **Description**: User login on the Windows 7 client machine.

![Windows 7 Domain](../screenshots/DOMINIO-WDS7.png)

- **Description**: Windows 7 client successfully joined to the domain `portafolio.local`.

![Windows 7 IP](../screenshots/IP-WDS7.png)

- **Description**: IP configuration of the Windows 7 client.

![Windows 7 Ping](../screenshots/ping-wds7.png)

- **Description**: Ping test from Windows 7 client to verify connectivity to the domain controller.













