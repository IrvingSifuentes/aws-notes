# IAM - Identity and Access Management

## ¿Qué es IAM?
- Servicio **global** de AWS (no depende de región)
- Controla **quién** puede acceder a **qué** en AWS

## Conceptos clave

### Usuarios y Grupos
- **Root account**: se crea por defecto, NUNCA usar ni compartir
- **Usuario**: representa a una persona real de la organización
- **Grupo**: contiene solo usuarios (no otros grupos)
- Un usuario puede pertenecer a varios grupos o a ninguno

### Políticas (Policies)
- Documentos **JSON** que definen permisos
- Se asignan a usuarios o grupos
- Principio de **mínimo privilegio**: dar solo los permisos necesarios

### Estructura de una política
- **Version**: siempre "2012-10-17"
- **Effect**: Allow o Deny
- **Action**: qué acciones se permiten (ej: ec2:Describe*)
- **Resource**: a qué recursos aplica

### MFA (Multi-Factor Authentication)
- Contraseña + dispositivo físico/virtual
- Opciones: Google Authenticator, Authy, YubiKey
- **Siempre activar en root y usuarios IAM**

### Formas de acceder a AWS
- **Consola**: usuario + contraseña + MFA
- **CLI**: Access Key ID + Secret Access Key
- **SDK**: Access Key ID + Secret Access Key (desde código)

### Roles IAM
- Permisos para **servicios de AWS** (no personas)
- Ejemplos: rol para EC2, Lambda, CloudFormation

## Buenas prácticas
- No usar root para el día a día
- Un usuario físico = un usuario AWS
- Activar MFA en todas las cuentas
- Rotar claves de acceso frecuentemente
- Nunca compartir usuarios ni claves

## Herramientas de auditoría
- **Credentials Report**: lista todos los usuarios y estado de credenciales
- **Access Advisor**: muestra últimos accesos por servicio