# Guía de Bastionado de BIOS/UEFI

## Introducción
La BIOS/UEFI son los primeros componentes que se ejecutan al encender un ordenador. Su función es reconocer el hardware instalado y determinar desde qué dispositivo se iniciará el sistema operativo.

Configurar correctamente la BIOS/UEFI es una medida fundamental para reforzar la seguridad del equipo, ya que permite controlar el acceso físico, evitar arranques no autorizados y proteger la integridad del sistema desde el momento del encendido.

## Contraseñas en BIOS/UEFI
El uso de contraseñas en la BIOS/UEFI es una de las medidas más sencillas y efectivas para proteger un dispositivo. Estas contraseñas permiten restringir el acceso tanto al arranque del sistema como a la propia configuración del firmware, evitando modificaciones no autorizadas o el uso del equipo por personas sin permiso.

Para ello, primero accederemos a la BIOS/UEFI de mi equipo ***HP Victus*** mediante la tecla "**F10**".
![Imagen Acceso BIOS/UEFI](./img/accesoBIOS-UEFI.jpg)

A partir de aqui, configuraremos los siguientes apartados de contraseñas de la BIOS/UEFI.

### Contraseña de usuario o Power-On
La **contraseña de usuario o Power-On** se solicita al encender el equipo y evita que personas no autorizadas puedan iniciar el sistema. Esta medida añade una capa de seguridad adicional, ya que impide el acceso incluso antes de que se cargue el sistema operativo.

Para configurar dicha contraseña en el equipo, estando en la BIOS/UEFI, debemos de ir al apartado ***Seguridad*** y hacer "**Enter**" en la opción ***Contraseña de arranque***.
![Imagen Contraseña usuario](./img/passwordUsuario.jpg)

En la siguiente "***ventana***" definiremos la contraseña de usuario, tiene que ser una contraseña robusta para mayor seguridad. Ejemplo: "***co3RCl9BBWaGLJ7TjO***"

![Imagen Contraseña usuario 2](./img/passwordUsuario2.jpg)

![Imagen Contraseña usuario 3](./img/passwordUsuario3.jpg)

![Imagen Contraseña usuario 4](./img/passwordUsuario4.jpg)
> Como podemos ver, se ha configurado la contraseña de usuario o Power-On correctamente.

Una vez realizado lo anteriormente, podemos hacer una prueba de la contraseña de usuario. Solo debemos de apagar el equipo, en el apartado ***Salir*** y en la opción **Guardar cambios y salir**. 

![Imagen Contraseña usuario 5](./img/apartadoGuardarSalir.jpg)

Al iniciar el equipo, primeramente pedirá la contraseña de usuario. Se mostrará de la siguiente manera:

![Imagen Contraseña usuario 6](./img/passwordUsuario6.jpg)

Y con esto hemos configurado la contraseña de usuario o Power-On correctamente en nuestro equipo.

### Contraseña de administrador
La **contraseña de administrador o Supervisor** protege el acceso a la configuración interna de la BIOS/UEFI. Gracias a ella, solo los usuarios autorizados pueden realizar cambios en los parámetros del sistema, como el orden de arranque o las opciones de seguridad.

Para configurar dicha contraseña en el equipo, debemos de ir al apartado ***Seguridad*** y hacer **Enter** en ***Contraseña de administrador***.
![Imagen Contraseña administrador](./img/passwordAdministrador.jpg)

En la siguiente "***ventana***" introduciremos la contraseña del administrador, tiene que ser una contraseña robusta para mayor seguridad. Ejemplo: "***4CvEZdqs2xFwiWKjni***"

![Imagen Contraseña administrador 2](./img/passwordAdministrador2.jpg)

![Imagen Contraseña administrador 3](./img/passwordAdministrador3.jpg)

![Imagen Contraseña administrador 4](./img/passwordAdministrador4.jpg)
> Como podemos ver, se ha configurado la contraseña de administrador correctamente.

Una vez realizado lo anteriormente, podemos hacer una prueba de la contraseña de administrador. Solo debemos de apagar el equipo, en el apartado ***Salir*** y en la opción **Guardar cambios y salir**.

![Imagen Contraseña administrador 5](./img/apartadoGuardarSalir.jpg)

Al iniciar el equipo, nos pedirá una de las dos contraseñas (usuario o administrador). Dependiendo de cual introduzcamos, deberemos de realizar más pasos o no:

- ***Opción Administrador:*** Si intentamos acceder a la BIOS/UEFI e introducimos primeramente la contraseña de administrador, podremos acceder directamente a ella.

![Imagen Contraseña administrador 6](./img/accesoBIOS-UEFI.jpg)

- ***Opción Usuario:*** Si intentamos acceder a la BIOS/UEFI e introducimos primeramente la contraseña de usuario, más tarde nos pedirá la contraseña de administrador, ya que no podemos acceder con permisos limitados (usuario).

![Imagen Contraseña administrador 7](./img/passwordAdministrador7.jpg)

En conclusión, deberemos de acceder con la contraseña de administrador a la BIOS/UEFI para poder realizar cualquier configuración.

## Control de arranques externos
Limitar los arranques desde dispositivos externos, como memorias USB, reduce el riesgo de que se ejecute software no autorizado o malicioso fuera del sistema operativo principal. Esta configuración es esencial para impedir ataques que aprovechan medios extraíbles para eludir medidas de seguridad.

Para configurar nuestro equipo para que no permita arranques desde dispositivos externos o mediante red, estando en la BIOS/UEFI, debemos de ir al apartado ***Opciones de arranque***.

![Imagen control arranque](./img/apartadoOpcionesArranque.jpg)

Ahora, debemos de cambiar la opción ***Arranque USB*** de "**Activado**" a "**Desactivado**".

![Imagen control arranque 2](./img/controlArranque2.jpg)

También, debemos de cambiar la opción ***Arranque de red*** de "**Activado**" a "**Desactivado**".

![Imagen control arranque 3](./img/controlArranque3.jpg)

Esta sería la configuración final, desactivando tanto el arranque USB como el arranque de red.

![Imagen control arranque 4](./img/controlArranque4.jpg)

Solo nos queda guardar la configuración desde el apartado ***Salir***, y en la opción **Guardar cambios y salir**.

![Imagen control arranque 5](./img/apartadoGuardarSalir.jpg)

Configurado estas opciones, nuestro equipo ya no permitirá arrancar mediante dispositivos externos ni por red.

## Orden de arranque seguro
El orden de arranque define la prioridad con la que el sistema busca dispositivos para iniciar el sistema operativo. Configurarlo de manera segura asegura que el equipo solo intente arrancar desde unidades confiables, evitando el uso de dispositivos externos o redes que puedan ser manipuladas por un atacante.

Primero, estando en la BIOS/UEFI, accederemos al apartado ***Opciones de arranque***.

![Imagen orden arranque](./img/apartadoOpcionesArranque.jpg)

Ahora, al final de este apartado, tenemos una sección llamada "**Orden de arranque UEFI**", en él iremos configurando el orden de manera segura. El orden más seguro para este equipo sería el siguiente.

![Imagen orden arranque 2](./img/ordenArranque2.jpg)
> Este es el orden más seguro, ya que garantiza que el equipo solo arranque desde el disco interno confiable y evita que dispositivos externos o de red puedan usarse para ejecutar software no autorizado o manipular el sistema.

## Otras opciones de seguridad
Además de las contraseñas y el control del arranque, la BIOS/UEFI ofrece otras funciones de seguridad que complementan el bastionado del sistema. Entre ellas se incluyen **Secure Boot** y **TPM**. Estas opciones ayudan a mantener la integridad del sistema.

- ***Secure Boot***

Para habilitar esta función de seguridad, estando en la BIOS/UEFI, debemos de ir al apartado ***Opciones de arranque***.

![Imagen Secure Boot](./img/apartadoOpcionesArranque.jpg)

Primero debemos de **Cargar las claves predeterminadas de HP** para poder habilitar la opción de **Secure Boot**.

![Imagen Secure Boot 2](./img/secureBoot2.jpg)

![Imagen Secure Boot 3](./img/secureBoot3.jpg)

Solo nos queda guardar la configuración desde el apartado ***Salir***, y en la opción **Guardar cambios y salir**.

![Imagen Secure Boot 4](./img/apartadoGuardarSalir.jpg)

Configurado Secure Boot en UEFI, nuestro equipo solo permitirá arrancar el sistema operativo legítimo, rechazando cualquier software no autorizado.

- ***TPM*** (Trusted Platform Module)

Para habilitar esta función de seguridad, estando en la BIOS/UEFI, debemos de ir al apartado ***Seguridad***.

![Imagen TPM](./img/apartadoSeguridad.jpg)

Ahora, debemos de cambiar la opción ***Dispositivo TPM*** de "**Oculto**" a "**Disponible**".

![Imagen TPM 2](./img/tpm2.jpg)

Solo nos queda guardar la configuración desde el apartado ***Salir***, y en la opción **Guardar cambios y salir**.

![Imagen TPM 3](./img/apartadoGuardarSalir.jpg)

Con el TPM activado, el equipo protege de forma segura las claves de cifrado y los datos sensibles, fortaleciendo la integridad del sistema y garantizando que funciones como Secure Boot o BitLocker funcionen correctamente desde el arranque.

## Conclusiones
El bastionado de la BIOS/UEFI representa el primer paso para asegurar un equipo de forma integral. Configurar contraseñas, restringir el arranque externo, establecer un orden seguro y activar opciones adicionales como Secure Boot o TPM permite reducir de forma significativa las vulnerabilidades a nivel de firmware y proteger la información del dispositivo desde el inicio.
