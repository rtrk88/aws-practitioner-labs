# EC2 Accessing S3 Using IAM Role

## Objetivo

Demostrar el acceso seguro desde una instancia Amazon EC2 a un bucket Amazon S3 utilizando un IAM Role en lugar de Access Keys.

## Servicios utilizados

- Amazon EC2
- Amazon S3
- AWS IAM
- AWS STS

## Actividades realizadas

- Creación de IAM Role para EC2
- Asignación de permisos sobre S3
- Lanzamiento de instancia EC2
- Asociación del IAM Role
- Verificación de identidad mediante STS
- Acceso a bucket S3 sin credenciales estáticas

## Evidencias

### IAM Role creado

![IAM Role](screenshots/01-iam-role-created.png)

### Instancia EC2

![EC2](screenshots/ec2-instance.png)

### Verificación STS

![STS](screenshots/sts-identity.png)

### Acceso a S3

![S3](screenshots/s3-access.png)

## Aprendizajes

- IAM Roles entregan credenciales temporales.
- No es necesario almacenar Access Keys en servidores.
- STS proporciona credenciales temporales y seguras.
- EC2 puede acceder a servicios AWS utilizando un rol asignado.
