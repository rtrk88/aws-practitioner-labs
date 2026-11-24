# Laboratorio 01 - Fundamentos de IAM

## Objetivo

Aprender los conceptos básicos de AWS Identity and Access Management (IAM), creando usuarios, grupos, políticas y habilitando MFA.

## Servicios utilizados

- AWS IAM
- MFA (Multi-Factor Authentication)

## Arquitectura

Usuario → Grupo → Política

## Actividades realizadas

- Creación de usuario IAM
- Creación de grupo IAM
- Asignación de permisos
- Incorporación del usuario al grupo
- Habilitación de MFA

## Conceptos aprendidos

### IAM User

Identidad utilizada por una persona o aplicación para acceder a AWS.

### IAM Group

Conjunto de usuarios que comparten permisos.

### IAM Policy

Documento JSON que define permisos sobre recursos AWS.

### MFA

Método de autenticación adicional para mejorar la seguridad.

## Buenas prácticas

- Aplicar principio de mínimo privilegio (Least Privilege).
- Evitar utilizar la cuenta Root para tareas diarias.
- Habilitar MFA en todas las cuentas con acceso administrativo.

## Conceptos importantes para el examen SAA-C03

- Un Explicit Deny siempre tiene prioridad sobre un Allow.
- Los IAM Roles son preferibles a las Access Keys permanentes.
- MFA aumenta la seguridad de
