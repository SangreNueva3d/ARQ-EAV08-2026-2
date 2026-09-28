# ARQ-EAV08-2026-2
Repositorio para entregables propios de la materia de Arquitectura de Software del equipo avanzado 8 de la edición 26-2 de CodeF@ctory, equipo conformado por:

YEPES JARAMILLO ANGEL SIMON: angel.yepes2@udea.edu.co
CONTRERAS PUELLO SAMUEL ESTEBAN: samuel.contreras@udea.edu.co
ALBORNOZ VILLADIEGO JOSÉ FERNANDO: jose.albornoz@udea.edu.co

# Contexto:



## Contexto de negocio
Las regulaciones de open banking impulsan la apertura de los sistemas financieros para que terceros desarrollen nuevos servicios a partir de información bancaria, siempre con el consentimiento del usuario. Para habilitar este ecosistema, las instituciones financieras deben ofrecer APIs que permitan a aplicaciones externas consultar información y ejecutar ciertas operaciones de forma controlada.

## Problema a resolver
BackendBank busca ser la capa tecnológica que expone servicios bancarios mediante APIs seguras, permitiendo que aplicaciones externas interactúen con ellos bajo reglas claras de acceso y trazabilidad.

## Alcance funcional
- **Registro de aplicaciones externas** .
- **Gestión de credenciales y autenticación** .
- **Exposición de APIs** .
- **Control de permisos y consentimiento** .
- **Registro de solicitudes** .
- **Reportes** .

## Estado actual
El módulo implementado es la **gestión de clientes**, base para el resto de la plataforma:
- Registro de clientes (`POST /clientes`)
- Ingreso con validación de credenciales y estado (`POST /clientes/ingreso`)
- Actualización de datos por un administrador (`PUT /clientes/{id}`)
- Cambio de estado activo/inactivo por un administrador (`PATCH /clientes/{id}/estado`)

Incluye roles (`CLIENTE`, `ADMINISTRADOR`) y estados (`activo`, `inactivo`, `bloqueado`, `pendiente_de_validacion`).
  
Este módulo corresponde a las hu's comprometidas en el sprint 1 que fueron:
- Registrar un nuevo cliente
- Actualizar datos del perfil de un cliente
- Cambiar el estado de un cliente (activo/inactivo)
- Autenticarse en el sistema
- Restringir acciones según el rol del usuario
  
Se debe contemplar algunas recomendaciones que nos hicieron en la review como el manejo de las contraseñas de los clientes que es algo que esta planteado corregirse para el sprint2

En el siguiente video se puede ver como funciona el back que realizamos y como las ejecuciones se reflejan correctamente en la bd:
https://drive.google.com/file/d/1mA1mIw5pobcbCp0FEJ88T2emUkaHuXbK/view?usp=sharing


---
# Diagrama de paquetes

![Diagrama de paquetes](./Diagramas/diagrama_de_paquetes_EAV08.drawio.png)

---
# Diagrama de despliegue

![Diagrama de paquetes](./Diagramas/diagrama_de_desplique_EAV08.drawio.png)

---

# Diagrama de componentes
![Diagrama de paquetes](./Diagramas/diagrama_de_componentes_EAV08.drawio.png)

---
# ADRs


