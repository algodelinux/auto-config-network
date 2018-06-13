auto-config-network
==================

Configura automáticamente las interfaces de red del equipo   

Este script borra el fichero /etc/udev/rules.d/70-persistent-rules por si se hubiera clonado el equipo y lo vuelve a regenerar detectando las interfaces de red de la máquina.   
Por otro lado, hace una copia el fichero /etc/network/interfaces en /etc/network/interfaces.old y lo regenera automáticamente, configurando:
# La interfaz localhost   
# Con IP estática, las interfaces con link configuradas para servir DHCP en el fichero /etc/default/isc-dhcp-server   
# Con IP dinámica, las interfaces con link no configuradas para servir DHCP   
   
Esteban M. Navas <algodelinux@gmail.com>   
Fecha creación:      12/06/2018   
Última modificación: 13/06/2018   

Instalación
-----------

La forma más sencilla de instalarlo es ejecutar los siguientes comandos:

   wget --no-check-certificate -O /usr/local/sbin/auto-config-network https://raw.githubusercontent.com/algodelinux/auto-config-network/master/auto-config-network  
   chmod 755 /usr/local/sbin/auto-config-network   
  
Uso                   
---

   auto-config-network   
