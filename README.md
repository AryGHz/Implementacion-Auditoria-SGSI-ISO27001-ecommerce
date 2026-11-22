# Implementación de un SGSI y Auditoría Interna a E-commerce basada en ISO/IEC 27001:2022

![Static Badge](https://img.shields.io/badge/ISO%2FIEC%2027001%3A2022-3836b3) 
![Static Badge](https://img.shields.io/badge/GRC-c7c5f6)
![Static Badge](https://img.shields.io/badge/AUDITORÍA-2f2f38)
![Static Badge](https://img.shields.io/badge/SGSI-3836b3)
![Static Badge](https://img.shields.io/badge/GESTIÓN%2FDE%2FRIESGOS-ffffff)
![Static Badge](https://img.shields.io/badge/PENTESTING-3836b3)
![Static Badge](https://img.shields.io/badge/ISO%2027002-4b459b) 
![Static Badge](https://img.shields.io/badge/ISO%2027005-c7c5f6) 
![Static Badge](https://img.shields.io/badge/ISO%2031010-4338ca) 
![Static Badge](https://img.shields.io/badge/MAGERIT-2f2f37)
![Static Badge](https://img.shields.io/badge/NIST%20SSDF-ffffff)
![Static Badge](https://img.shields.io/badge/OWASP%20TOP%2010%3A2025-0f172a)

---

Este repositorio contiene el proyecto de implementación y Auditoría Interna de un Sistema de Gestión de Seguridad de la Información para una empresa de comercio electrónico ficticia, diseñado con el objetivo de lograr la certificación bajo la norma ISO/IEC 27001:2022.

La implementación se desarrolló siguiendo rigurosamente los lineamientos de la norma para garantizar el cumplimiento de todas sus cláusulas y controles aplicables. Con base en esta documentación y evidencia operativa, se ejecutó una segunda fase correspondiente a la auditoría interna.

---

## Contexto de la empresa 

Manufacturas Serdán, S.A. de C.V. es una empresa mexicana ficticia dedicada a la fabricación y comercialización al mayoreo de prendas de vestir básicas, cuya principal fuente de ingresos es su canal de comercio electrónico. La organización busca certificarse en ISO/IEC 27001:2022 para respaldar su incursión en mercados internacionales.

El entorno se diseñó respetando modelos realistas de arquitectura en PyMEs: combina la contratación de servicios de terceros para componentes críticos con desarrollo a medida en servicios específicos. Esto permite abarcar un espectro amplio de controles, desde gobernanza y gestión de riesgos de terceros hasta desarrollo seguro.

## Arquitectura Tecnológica y Alcance

La arquitectura de la organización centraliza sus servicios críticos en una plataforma ERP modular bajo modalidad PaaS, diseñada para emular ecosistemas ampliamente utilizados en el comercio electrónico actual como Odoo o ERPNext. Esta plataforma integra el canal de comercio electrónico, la gestión de clientes o CRM, finanzas, facturación, timbrado fiscal y la mesa de ayuda tanto para atención a clientes como para tickets de soporte interno. La base de datos opera dentro de la misma plataforma y se complementa con respaldos externos en AWS. A nivel operativo, la empresa trabaja en modalidad 100% presencial desde sus oficinas centrales, respaldada por un proveedor de servicios de seguridad administrada o MSSP y seguridad física privada.

Siguiendo las mejores prácticas de implementación en entornos reales, donde se recomienda acotar el alcance del SGSI únicamente a los procesos críticos del negocio, este se definió sobre la plataforma ERP de comercio electrónico, el personal que interactúa directamente con ella y las oficinas físicas donde desempeñan sus funciones.

Respetando este alcance, quedaron excluidos los procesos industriales, el WMS y las redes externas, al operar de manera independiente y mantener sus interfaces separadas del núcleo transaccional de la plataforma ERP.

---

## Proceso de implementación

El eje principal de la implementación se centra en la gobernanza, la gestión de riesgos y el cumplimiento regulatorio.

La evaluación de riesgos incorpora fuentes actuales y escenarios realistas acordes con las amenazas que afectan al sector e-commerce y al panorama de ciberseguridad en México.

El plan de seguridad pone especial énfasis en la cadena de suministro, dado que la empresa delega actividades críticas a plataformas externas. Este enfoque refleja una problemática real del comercio electrónico actual, que consiste en mantener despliegues ágiles sin sacrificar resiliencia operativa ni exponerse a pérdidas económicas.

Se documentaron actividades operativas propias de un entorno productivo, destacando un ejercicio de pentesting simulado sobre una red interna realista. Para garantizar la independencia técnica exigida por la norma, esta evaluación se simuló a través de una consultora externa ficticia denominada Delta Ciberseguridad.

---

## Proceso de auditoría interna

En un entorno real, quien diseña e implementa el SGSI no debe participar en el proceso de auditoría. Para respetar la imparcialidad y evitar conflictos de interés, se simuló la participación de una consultora externa independiente denominada AG Consultoría, quien realizó las actividades del rol de Auditor Líder.

Durante esta fase se revisó la documentación rectora, las evaluaciones y planes de tratamiento de riesgos, así como la evidencia operativa de los controles aplicables según la Declaración de Aplicabilidad o SoA.

### Resultados del Informe de Auditoría Interna
* **No Conformidades Mayores:** `0`
* **No Conformidades Menores:** `3`
* **Oportunidades de Mejora:** `4`

---

## Marcos de referencia y estándares aplicados

| Dominio | Marcos Aplicados | Aplicación en el Proyecto |
| :--- | :--- | :--- |
| **Gobernanza y Controles** | `ISO/IEC 27001:2022`, `ISO/IEC 27002` | Estructura del SGSI, cláusulas de gestión y selección de controles del Anexo A. |
| **Gestión de Riesgos** | `ISO/IEC 27005`, `ISO/IEC 31010`, `MAGERIT`,`OWASP Top 10:2025 `  | Metodología de identificación, análisis, evaluación y tratamiento de riesgos sobre activos. |
| **Métricas y Auditoría** | `ISO/IEC 27004`, `ISO/IEC 27007`, `ISO 19011` | Medición de eficacia de controles, planificación y ejecución de la auditoría interna. |
| **Desarrollo Seguro** | `NIST SSDF`| Lineamientos de desarrollo seguro para servicios a medida y revisión de código. |
| **Controles Específicos** | `NIST SP 800-63B`, `NIST SP 800-88` | Criterios técnicos para contraseñas seguras y sanitización de medios. |

---

## Estructura del repositorio

El proyecto integra un total de 48 documentos redactados y evidencias, organizados en cinco directorios principales:

* **`Documentos Obligatorios`:** Son los componentes indispensables para la certificación y constituyen el núcleo del SGSI. 
* **`Políticas`:** Marco de gobernanza de alto nivel mediante el cual la organización rige su seguridad de la información.
* **`Lineamientos y Procedimientos`:** Guías técnicas y procedimientos operativos que establecen el flujo de trabajo paso a paso para actividades críticas, por ejemplo, respuesta a incidentes y recuperación ante desastres.
* **`Evidencias`:** Registros operativos que sustentan el cumplimiento real de la Declaración de Aplicabilidad, como reportes periódicos, capturas técnicas, informes de pentesting, contratos y acuerdos firmados.
* **`Regulatorios`:** Marco legal y contractual aplicable a la organización, incluyendo la matriz de requisitos legales, contratos, avisos de privacidad y acuerdos de confidencialidad.

> **Nota de navegación:** Dentro de cada carpeta encontrarás una **tabla maestra de documentos** con el índice, tipo de documento y una breve descripción de su contenido.

---

## Sobre el autor

**Aracely Gonzalez Hernandez**  
* Auditor Interno Certificado ISO/IEC 27001 | Analista GRC*

*Manufacturas Serdán, S.A. de C.V., AG Consultoría y Delta Ciberseguridad son entidades ficticias creadas con fines de apoyo al portafolio profesional.*

