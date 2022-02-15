# Dropbear

Conexion VPN por Medio del Servicio Dropbear

# INICIO:

sudo su

cd

apt-get update && apt-get upgrade -y

apt-get install dropbear -y


# Abrir y Editar el Archivo dropbear:

nano /etc/default/dropbear


NO_START=1

DROPBEAR_PORT=22

DROPBEAR_EXTRA_ARGS=

DROPBEAR_RECEIVE_WINDOW=65536



# Modificar Las Siguientes Lineas:

NO_START=1 (Activar el servicio Modificando el numero 1 por el 0)

NO_START=0



DROPBEAR_PORT=22 (Cambiar el Puerto 22 Por el Puerto a usar en Dropbear)

DROPBEAR_PORT=443



DROPBEAR_EXTRA_ARGS= (Opcional, solo modificar si necesita mas puertos en el servicio Dropbear)

DROPBEAR_EXTRA_ARGS="-p 80 -p 110 "


# Resultado:

NO_START=0

DROPBEAR_PORT=443

DROPBEAR_EXTRA_ARGS="-p 80 -p 110 "

DROPBEAR_RECEIVE_WINDOW=65536


# Guardar el Archivo dropbear:

[CONTROL] + [X]
yes
[ENTER]

# Reiniciar el Servicio:

service dropbear restart

# Detener el Servicio:

service dropbear stop

# Iniciar el Servicio:

service dropbear start

# Revizar el Estado del Servicio:

service dropbear status



# Revizar los Puertos y Servicios Activos:

netstat -tnlp


@XhokitoPe


* Compatible con Ubuntu 14, 16, 18



