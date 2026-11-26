## Laboratorio 02: IAM Roles y STS

### Qué aprendí
- Usar un **IAM Role** (con *instance profile*) para que una instancia **EC2** acceda a **S3** de forma segura sin guardar *access keys* fijas ni credenciales en el código.
- Configurar la **Trust relationship** para permitir que `ec2.amazonaws.com` ejecute `sts:AssumeRole` y obtenga credenciales temporales.

### Evidencia
![Trust relationship de EC2-S3-ReadOnly-Role](screenshots/03-trust-relationship.png)

### Clave para el examen (SAA-C03)
- **EC2 o Lambda accediendo a S3 o DynamoDB:** usar siempre un **IAM Role** (nunca *access keys* hardcodeadas).
- **Acceso entre cuentas:** rol en la cuenta destino con *trust policy* y `sts:AssumeRole`.

# Laboratorio 03: Amazon S3

## Qué aprendí

- Crear buckets S3
- Subir objetos
- Entender almacenamiento de objetos
- Aplicar buenas prácticas de seguridad usando Block Public Access

## Conceptos clave para el examen

- S3 es almacenamiento de objetos.
- Durabilidad de 99.999999999% (11 nueves).
- Es un servicio regional.
- Escala prácticamente de forma ilimitada.
