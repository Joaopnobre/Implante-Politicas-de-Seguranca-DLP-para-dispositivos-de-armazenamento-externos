# Implante-Politicas-de-Seguranca-DLP-para-dispositivos-de-armazenamento-externos
Proyecto 4geeks - Implante-Pol-ticas-de-Seguran-a-DLP-para-dispositivos-de-armazenamento-externos
# Prevención contra la Pérdida de Datos (DLP)

## Introducción

La Prevención contra la Pérdida de Datos (Data Loss Prevention - DLP) consiste en políticas, procesos y tecnologías diseñadas para impedir la fuga, pérdida o acceso no autorizado a información sensible dentro de una organización.

Su objetivo principal es proteger datos almacenados, datos en tránsito y datos en uso, reduciendo riesgos internos y externos. La implementación de DLP fortalece la seguridad corporativa, mejora el control de acceso y ayuda al cumplimiento de normativas como GDPR y PCI DSS.

---

# Parte 1 – Políticas de Seguridad DLP

## 1. Clasificación de Datos

La organización adoptará tres niveles de clasificación:

### Datos Públicos

Información que puede divulgarse externamente.

**Ejemplos:**

- Sitio web institucional  
- Material de marketing  
- Comunicados oficiales  

### Datos Internos

Información restringida para uso interno.

**Ejemplos:**

- Procedimientos internos  
- Informes operativos  
- Organigramas  

### Datos Sensibles

Información crítica y confidencial.

**Ejemplos:**

- Datos de clientes  
- Información financiera  
- Contratos  
- Credenciales  
- Estrategias comerciales  

### Herramientas utilizadas:

- Microsoft Information Protection  
- Titus Classification Suite  
- Boldon James Classifier  
- Varonis Data Classification Engine  
- BigID Data Intelligence  

---

## 2. Acceso y Control

Se aplicará el Principio del Menor Privilegio, garantizando que cada colaborador tenga acceso únicamente a los recursos necesarios para desempeñar su función.

### Reglas:

- Recursos Humanos accede a datos de empleados.  
- Finanzas accede a información financiera.  
- TI administra sistemas y permisos.  
- Usuarios comunes acceden solo a sus archivos y carpetas asignadas.  

### Herramientas de Control de Acceso:

- Active Directory  
- OpenLDAP  
- AWS IAM  
- Azure AD  
- Okta  

### Revisión de Permisos:

- Revisión mensual de cuentas inactivas.  
- Revisión trimestral por departamento.  
- Revocación inmediata en caso de baja laboral o cambio de puesto.  

---

## 3. Monitoreo y Auditoría

La organización utilizará herramientas de monitoreo para registrar actividades sospechosas y detectar incidentes.

### Herramientas:

- Microsoft Sentinel  
- Splunk  
- Symantec DLP  
- Forcepoint DLP  
- McAfee DLP Endpoint  

### Controles:

- Registro de accesos a archivos sensibles.  
- Alertas por copia masiva de datos.  
- Monitoreo del uso de dispositivos USB.  
- Auditoría de cambios en permisos.  
- Detección de transferencias no autorizadas por correo electrónico o nube.  

---

## 4. Prevención de Fugas de Datos

Se implementarán medidas técnicas para impedir la exfiltración de información.

### Protección de datos en reposo:

- BitLocker  
- FileVault  
- VeraCrypt  
- LUKS  
- AWS Key Management Service (KMS)

### Protección de datos en tránsito:

- SSL/TLS  
- VPN  
- IPsec  
- SFTP  
- HTTPS

### Medidas adicionales:

- Uso de OpenVPN para accesos remotos seguros.  
- Bloqueo del envío externo de archivos sensibles.  
- Restricción de impresión de documentos confidenciales.  
- Control y bloqueo de memorias USB no autorizadas.  

---

## 5. Educación y Concienciación

Todos los empleados recibirán formación periódica sobre seguridad de la información.

### Contenido:

- Uso de contraseñas seguras.  
- Detección de phishing.  
- Ingeniería social.  
- Protección de datos sensibles.  
- Uso correcto de dispositivos removibles.  
- Procedimientos de reporte de incidentes.  

La formación se realizará mediante sesiones semestrales y campañas internas continuas.

---

# Parte 2 – Restricción de Dispositivos USB en Windows

## Objetivo

Implementar una política práctica de DLP para impedir el uso no autorizado de dispositivos USB dentro de un entorno corporativo.

## Entorno Utilizado

- Oracle VirtualBox  
- Máquina virtual Windows 10 Pro  
- Editor de Directivas de Grupo Local (gpedit.msc)

## Configuración Realizada

Se accedió al Editor de Directivas de Grupo Local mediante:

```text
gpedit.msc
