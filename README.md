# CleanERP para Limpro Químicos

Sistema **CleanERP** para **Limpro Químicos, S.A. de C.V.**, desarrollado por **TechPyme Soluciones**.

CleanERP es una plataforma empresarial orientada a la gestión integral de procesos administrativos, comerciales, operativos e inventarios de Limpro Químicos. El proyecto busca centralizar la información del negocio, mejorar la trazabilidad de las operaciones y facilitar la integración con procesos de punto de venta, facturación electrónica e inventario.

> **Estado del proyecto:** En desarrollo  
> **Organización:** TechPyme Soluciones  
> **Cliente:** Limpro Químicos, S.A. de C.V.

---

## Tabla de contenidos

- [Descripción del proyecto](#descripción-del-proyecto)
- [Objetivos](#objetivos)
- [Estrategia de ramas](#estrategia-de-ramas)
- [Reglas de Pull Requests y revisión de código](#reglas-de-pull-requests-y-revisión-de-código)
- [Convención de commits](#convención-de-commits)
- [Flujo de trabajo recomendado](#flujo-de-trabajo-recomendado)
- [Cumplimiento legal y normativo](#cumplimiento-legal-y-normativo)
- [Contribución](#contribución)
- [Contacto](#contacto)
- [Licencia](#licencia)

---

## Descripción del proyecto

**CleanERP** es un sistema empresarial diseñado para apoyar la operación de Limpro Químicos, S.A. de C.V. Su propósito es proporcionar una base tecnológica organizada, escalable y mantenible para la administración de información y procesos internos.

Entre las áreas contempladas por el sistema se incluyen:

- Gestión de productos e inventarios.
- Control de entradas y salidas de mercancía.
- Operación de punto de venta.
- Procesos comerciales y administrativos.
- Facturación electrónica y CFDI 4.0.
- Reportes y consulta de información operativa.
- Trazabilidad de operaciones y movimientos.
- Administración de usuarios y permisos.

La implementación y configuración de cada módulo deberá realizarse de acuerdo con los requerimientos funcionales y operativos definidos para el proyecto.

---

## Objetivos

- Centralizar la información operativa y administrativa de la empresa.
- Mejorar el control y la trazabilidad del inventario.
- Facilitar la operación del punto de venta.
- Apoyar los procesos relacionados con CFDI 4.0.
- Reducir errores derivados de procesos manuales.
- Mantener una arquitectura organizada y preparada para futuras ampliaciones.
- Aplicar buenas prácticas de desarrollo, revisión y control de cambios.
- Proteger la información conforme a las obligaciones legales y normativas aplicables.

---

## Estrategia de ramas

El proyecto utiliza una estrategia de ramas orientada a separar el código estable, la integración de cambios y el desarrollo de características específicas.

### Ramas principales

| Rama | Propósito |
|------|-----------|
| `main` | Contiene el código estable destinado a producción. |
| `develop` | Rama de integración para validar cambios antes de incorporarlos a producción. |

### Ramas de características

Las nuevas funcionalidades deben desarrollarse en ramas independientes con el prefijo `feature/`.

Ramas de características contempladas:

- `feature/nom018-inventory`: Desarrollo de funcionalidades relacionadas con inventarios y los requerimientos asociados a NOM-018.
- `feature/pos-cfdi40`: Desarrollo de funcionalidades de punto de venta y facturación electrónica conforme a CFDI 4.0.

Para nuevas características, se recomienda utilizar nombres descriptivos siguiendo el siguiente formato:

```text
feature/nombre-de-la-funcionalidad
```

### Flujo de ramas

El flujo general de trabajo es el siguiente:

1. Crear una rama de característica a partir de `develop`.
2. Implementar los cambios y realizar commits siguiendo la convención establecida.
3. Ejecutar las pruebas unitarias y validaciones correspondientes.
4. Abrir un Pull Request hacia `develop`.
5. Atender los comentarios derivados de la revisión de código.
6. Integrar los cambios una vez cumplidas todas las reglas de aprobación.
7. Promover los cambios de `develop` hacia `main` mediante un Pull Request de liberación.
8. Desplegar a producción únicamente desde `main`.

---

## Reglas de Pull Requests y revisión de código

Todos los cambios deben integrarse mediante un **Pull Request**. No se deben realizar cambios directamente sobre la rama `main`.

Para que un Pull Request pueda ser aprobado, debe cumplir obligatoriamente con los siguientes requisitos:

- Contar con un mínimo de **1 revisión simulada**.
- Tener las **pruebas unitarias aprobadas**.
- No presentar **conflictos con la rama `main`**.
- Incluir una descripción clara del cambio realizado.
- Identificar, cuando corresponda, los módulos o procesos afectados.
- Mantener el alcance del cambio limitado al objetivo del Pull Request.
- Incluir evidencia de las pruebas realizadas cuando sea necesario.
- Corregir los comentarios o hallazgos identificados durante la revisión.
- Mantener actualizado el código con respecto a la rama destino antes de la aprobación final.

### Recomendaciones para Pull Requests

Cada Pull Request debería incluir:

- Resumen funcional y técnico.
- Motivo del cambio.
- Lista de archivos o componentes principales modificados.
- Instrucciones para validar el cambio.
- Resultado de las pruebas unitarias.
- Consideraciones de seguridad, privacidad o cumplimiento normativo.
- Capturas de pantalla o evidencias, cuando se trate de cambios visuales.

### Criterios de rechazo

Un Pull Request deberá regresar a desarrollo si:

- No incluye pruebas o las pruebas fallan.
- Tiene conflictos con la rama `main`.
- No cuenta con la revisión simulada requerida.
- Introduce cambios no relacionados con el objetivo descrito.
- Contiene información sensible, credenciales o datos personales reales.
- Incumple la convención de commits o las prácticas de calidad del proyecto.
- Presenta riesgos no documentados para la operación, seguridad o cumplimiento legal.

---

## Convención de commits

Los mensajes de commit deben ser breves, claros y consistentes. Se utilizarán los siguientes prefijos:

| Prefijo | Uso |
|---------|-----|
| `feat:` | Incorporación de una nueva funcionalidad. |
| `fix:` | Corrección de un error o comportamiento inesperado. |
| `docs:` | Cambios en documentación. |
| `style:` | Cambios de formato, estilo o presentación que no modifican la lógica funcional. |

### Formato

```text
tipo: descripción breve del cambio
```

### Ejemplos

```text
feat: agregar consulta de existencias por almacén
```

```text
fix: corregir cálculo del total en el punto de venta
```

```text
docs: actualizar instrucciones de instalación
```

```text
style: ajustar formato de componentes de inventario
```

### Recomendaciones

- Utilizar verbos en infinitivo o una descripción directa y consistente.
- Mantener el mensaje enfocado en un solo cambio.
- Evitar mensajes genéricos como `cambios`, `avance` o `actualización`.
- No incluir contraseñas, tokens, claves privadas u otros datos sensibles.
- Dividir cambios grandes en commits pequeños y coherentes.

---

## Flujo de trabajo recomendado

```bash
# Cambiar a la rama de integración
git checkout develop

# Obtener los cambios más recientes
git pull origin develop

# Crear una rama de característica
git checkout -b feature/nombre-de-la-funcionalidad

# Realizar cambios y agregarlos al área de preparación
git add .

# Crear un commit siguiendo la convención
git commit -m "feat: agregar nueva funcionalidad"

# Publicar la rama
git push origin feature/nombre-de-la-funcionalidad
```

Después de publicar la rama:

1. Crear un Pull Request hacia `develop`.
2. Ejecutar y documentar las pruebas correspondientes.
3. Solicitar la revisión simulada obligatoria.
4. Resolver los comentarios recibidos.
5. Verificar que no existan conflictos con `main`.
6. Integrar el cambio únicamente cuando se cumplan todos los requisitos.

---

## Cumplimiento legal y normativo

El desarrollo y operación de CleanERP deberá considerar las obligaciones legales y normativas aplicables a Limpro Químicos, S.A. de C.V.

### Protección de datos personales

El sistema debe diseñarse considerando la **Ley Federal de Protección de Datos Personales en Posesión de los Particulares (LFPDPPP)** y sus disposiciones aplicables.

Esto incluye, entre otros aspectos:

- Protección de datos personales y sensibles.
- Control de acceso conforme a las responsabilidades de cada usuario.
- Manejo seguro de credenciales.
- Minimización de la información recopilada.
- Trazabilidad de accesos y operaciones relevantes.
- Respeto a los avisos de privacidad y finalidades autorizadas.
- Implementación de medidas de seguridad administrativas, técnicas y físicas.
- Evitar el almacenamiento de información personal innecesaria.

No deben incorporarse al repositorio datos personales reales, archivos de configuración con secretos, contraseñas, tokens, certificados privados ni información confidencial del cliente.

### Facturación electrónica

Los procesos relacionados con facturación electrónica deberán considerar el **Anexo 20 del SAT** y las disposiciones fiscales aplicables, incluyendo los requerimientos relacionados con CFDI 4.0.

Las integraciones de facturación deberán validarse funcionalmente y mantenerse actualizadas conforme a los criterios, catálogos, especificaciones y disposiciones vigentes de la autoridad fiscal.

> La mención de estos marcos legales y normativos no sustituye la revisión de un especialista fiscal, legal o de protección de datos. Antes de liberar funcionalidades relacionadas con datos personales o facturación electrónica, se deberá realizar la validación correspondiente con los responsables designados por la empresa.

---

## Contribución

Para contribuir al proyecto:

1. Revisar la documentación disponible.
2. Crear una rama de característica a partir de `develop`.
3. Implementar el cambio manteniendo el alcance definido.
4. Agregar o actualizar las pruebas correspondientes.
5. Utilizar la convención de commits.
6. Abrir un Pull Request hacia `develop`.
7. Atender la revisión simulada y cualquier comentario de calidad.
8. Verificar que las pruebas estén aprobadas y que no existan conflictos con `main`.

Toda contribución debe respetar los principios de seguridad, privacidad, mantenibilidad y cumplimiento establecidos para el proyecto.

---

## Seguridad

Si se identifica una vulnerabilidad de seguridad, no se deben publicar detalles sensibles en un issue público. El hallazgo debe comunicarse directamente a los responsables del proyecto para su análisis y atención.

Nunca se deben incluir en el repositorio:

- Contraseñas.
- Tokens de acceso.
- Claves API.
- Certificados privados.
- Datos personales reales.
- Información fiscal confidencial.
- Respaldos de bases de datos con información productiva.
- Archivos de configuración con secretos.

---

## Contacto

**TechPyme Soluciones**  
Desarrollo y soporte del sistema CleanERP para Limpro Químicos, S.A. de C.V.

Para asuntos relacionados con el proyecto, consultar los canales internos definidos por TechPyme Soluciones y Limpro Químicos.

---

## Licencia

Este proyecto contiene software desarrollado para **Limpro Químicos, S.A. de C.V.** por **TechPyme Soluciones**.

Los derechos de uso, modificación, distribución y explotación del sistema se encuentran sujetos a los acuerdos comerciales y legales establecidos entre las partes. No se autoriza la redistribución o uso externo sin la autorización correspondiente.