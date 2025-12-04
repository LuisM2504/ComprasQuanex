# Sistema de Compras – Quanex Ciudad Juárez
### Solicitudes de Cotización • Requisiciones • Flujo de Aprobación • Proveedores • Auditoría

---

##  Resumen Ejecutivo

### **Descripción del Proyecto**
El presente sistema tiene como objetivo digitalizar y automatizar el proceso completo del área de Compras en Quanex Ciudad Juárez. Este flujo incluye la solicitud de cotizaciones, generación de requisiciones, autorización jerárquica, gestión de proveedores y reportes de auditoría.  

La solución busca reemplazar procesos manuales basados en Excel, correos electrónicos y una aplicación descontinuada de PowerApps, entregando un sistema robusto, auditable, trazable y escalable.

---

## Problema Identificado
Durante varios años, Quanex ha enfrentado problemas significativos en sus procesos de compras:

- Uso de **Excel** para solicitudes, cotizaciones y requisiciones → errores frecuentes.  
- Flujos de aprobación por **correo electrónico** → pérdida de trazabilidad y demoras.  
- La aplicación previa de **PowerApps quedó inhabilitada** por cambios de dominio/licencias.  
- No existe un sistema unificado que integre proveedores, requisiciones y aprobaciones.  
- Falta de auditoría, bitácoras y controles de seguridad.  

Este escenario genera riesgos operativos, falta de control, inconsistencias en datos y tiempos prolongados de procesamiento.

---

## Solución Propuesta
Se desarrollará un **sistema integral de compras**, construido con arquitectura MVC, que considera:

### Módulo de Solicitudes de Cotización  
Registrar solicitudes, seleccionar proveedores y realizar envíos automáticos por correo.

### Módulo de Requisiciones  
Generar requisiciones basadas en cotizaciones y administrar estados (borrador, enviada, aprobada, rechazada, cerrada).

### Flujo de Aprobaciones Automático  
Jerarquía basada en área y monto (gerente → contralor → director), con bitácora completa.

### Catálogo de Proveedores  
Alta, edición, baja, validación fiscal y migración desde archivos existentes.

### Gestión de Usuarios y Roles  
Control de accesos por rol: requisitor, aprobador, comprador y administrador de IT.

### Reportes y Auditoría  
Reportes exportables y registro de todas las acciones relevantes del sistema.

### Entregas por Etapas  
- **BETA (V1):** funcionamiento completo del ciclo de compras.  
- **GA (Versión Final):** optimización, dashboards, versión móvil, rendimiento avanzado.

Esta solución permite trazabilidad total, seguridad, confiabilidad y operación continua.

---

## Arquitectura del Sistema

### **Frontend**
- JSP / HTML5  
- Formularios y vistas del sistema  
- Validaciones básicas del lado del cliente  

### **Backend**
- Controladores (Servlets o Spring MVC)  
- Servicios de negocio:
  - Generación de folios  
  - Envío de correos  
  - Validación de flujos  
  - Manejo de usuarios y roles  
  - Bitácora de acciones  
- API interna entre módulos  

### **Base de Datos**
Tablas principales:
- Usuarios  
- Roles  
- Usuarios_Roles  
- Proveedores  
- SolicitudesCotizaciones / DetalleCotizaciones  
- Requisiciones / DetalleRequisiciones  
- Aprobaciones  
- Bitácora  

### **Infraestructura**
- Servidor de Aplicación: Apache Tomcat o GlassFish  
- Repositorio: GitHub  
- Integración Continua: Drone CI (o Travis CI si estuviera disponible)  
- Gestor de dependencias: Maven  
- IDE de Desarrollo: NetBeans  

---

## Tabla de Contenidos (ToC)

### **Documentación General**
- [1. Resumen Ejecutivo](#-resumen-ejecutivo)
- [2. Problema Identificado](#-problema-identificado)
- [3. Solución Propuesta](#-solución-propuesta)
- [4. Arquitectura del Sistema](#-arquitectura-del-sistema)
- [5. Alcance del Proyecto](https://github.com/usuario/repositorio/wiki/Alcance)
- [6. Requerimientos Funcionales y No Funcionales](https://github.com/usuario/repositorio/wiki/Requerimientos)
- [7. Modelo de Datos](https://github.com/usuario/repositorio/wiki/Modelo-de-Datos)
- [8. Guía de Instalación](https://github.com/usuario/repositorio/wiki/Instalacion)
- [9. Manual de Usuario](https://github.com/usuario/repositorio/wiki/Manual-de-Usuario)

### **Integración Continua**
- [Drone CI Pipeline](https://github.com/usuario/repositorio/wiki/CI)

### **Documentación Externa (opcional)**
- https://readthedocs.io/
- https://scrumguides.org/

---

## Créditos
Proyecto desarrollado como parte del **Proyecto Integrador – Quanex Ciudad Juárez**, Área de Compras.  
Autor: *Luis Martínez*
