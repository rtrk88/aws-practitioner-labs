# Laboratorio IAM

## Objetivo

Aprender cómo funciona AWS Identity and Access Management (IAM) y comprender cómo AWS controla el acceso a los recursos mediante usuarios, grupos, roles y políticas.

---

## Servicios Utilizados

- IAM

---

## Actividades Realizadas

- Crear usuario IAM
- Crear grupo IAM
- Crear políticas IAM
- Asignar permisos
- Probar acceso al panel de AWS

---

## Conceptos Aprendidos

- Usuarios IAM
- Grupos IAM
- Políticas IAM
- Roles IAM
- Principio de mínimo privilegio

---

## Conocimientos para AWS Cloud Practitioner

- Gestión de identidades y accesos
- Control de permisos
- Seguridad en AWS
- Usuarios y grupos
- Políticas de acceso
- Autenticación y autorización

---

## Capturas

Las capturas de pantalla de este laboratorio se encuentran en la carpeta `screenshots`.

---

## Reflexión Personal

En este laboratorio aprendí cómo AWS gestiona el acceso a los recursos mediante IAM.

Comprendí la importancia de otorgar únicamente los permisos necesarios a cada usuario siguiendo el principio de mínimo privilegio, uno de los conceptos fundamentales de seguridad en la nube.

---

## Estado del Laboratorio

🟡 En progreso

---

## Avances Realizados

- Limpieza de usuarios y grupos de pruebas anteriores.
- Se mantuvo únicamente el usuario administrativo principal: admin-franz.
- Preparación del entorno para realizar el laboratorio IAM desde cero.
- Creación del grupo IAM "Administradores".
- Verificación de que el grupo fue creado inicialmente sin usuarios ni permisos asignados.

### Creación de un Grupo IAM

Se creó el grupo "Administradores" para comprender cómo AWS permite administrar permisos de manera centralizada.

Inicialmente el grupo fue creado sin usuarios ni políticas asociadas para entender la diferencia entre grupos y permisos.

### Evidencia

![Grupo Administradores](screenshots/grupo-administradores.png)

### Asignación de Política al Grupo IAM

Se asignó la política administrada por AWS denominada `AdministratorAccess`
al grupo `Administradores`.

Esta política proporciona acceso completo a los recursos de AWS y permite
comprender cómo los permisos son heredados por los usuarios pertenecientes a un grupo.

### Evidencia

![Política Grupo](screenshots/politica-grupo.png)

### Creación de Usuario IAM

Se creó el usuario `soporte-01` para comprender la administración de identidades en AWS mediante IAM.

El usuario recibió acceso a la consola de administración de AWS para realizar pruebas de autenticación y permisos.

### Evidencia

![Usuario IAM](screenshots/usuario-soporte01.png)

### Asociación de Usuario a Grupo IAM

Se agregó el usuario `soporte-01` al grupo `Administradores`.

Los permisos no fueron asignados directamente al usuario. En su lugar,
el usuario hereda la política `AdministratorAccess` a través del grupo IAM,
siguiendo las buenas prácticas recomendadas por AWS para la administración
de accesos.

### Evidencia

![Usuario en Grupo](screenshots/usuario-en-grupo.png)

### Validación de Acceso

Se inició sesión correctamente con el usuario `soporte-01`.

Se verificó que el usuario heredó la política `AdministratorAccess`
a través del grupo `Administradores`, pudiendo acceder a los servicios
autorizados dentro de la cuenta AWS.

### Evidencia

![Login Correcto](screenshots/login-soporte01.png)
