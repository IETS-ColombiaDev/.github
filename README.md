<div align="center">

<img src="https://avatars.githubusercontent.com/u/93724030?v=4" alt="Logo IETS" width="90">

# IETS-ColombiaDev · Espacio de miembros

**Repositorios, convenciones y reglas de trabajo del equipo de desarrollo del IETS**

![Solo miembros](https://img.shields.io/badge/vista-solo%20miembros-003189?style=flat-square)
![Soporte](https://img.shields.io/badge/tickets-soporte%40iets.org.co-32B4A8?style=flat-square)

</div>

> Esta vista solo la ven los miembros de la organización. Aquí puede ir información interna; el perfil público vive en el repositorio `.github`.

## Primeros pasos

1. **Cuenta.** Usa una cuenta de GitHub con verificación en dos pasos activa y asocia tu correo institucional `@iets.org.co`.
2. **Acceso.** Solicita acceso a repositorios o equipos mediante ticket a [soporte@iets.org.co](mailto:soporte@iets.org.co), indicando el repositorio y el nivel de permiso que necesitas (lectura o escritura).
3. **Antes de ejecutar un proyecto.** Lee su `README`, copia `.env.example` a `.env` y pide las credenciales por ticket. Las credenciales nunca se comparten por chat ni por correo abierto.

## Mapa de repositorios

Repositorios destacados, agrupados por área. El catálogo completo está en la pestaña **Repositories**, donde puedes filtrar por *topic* escribiendo, por ejemplo, `topic:legacy` en el buscador.

### Evaluación de tecnologías y evidencia

| Repositorio | Descripción | Stack | Visibilidad |
|---|---|---|---|
| [mapa-evidencia-cannabis](https://github.com/IETS-ColombiaDev/mapa-evidencia-cannabis) | Mapa de evidencia y brechas en cannabis medicinal | Python · Flask | Público |
| [Sis_HS_IETS](https://github.com/IETS-ColombiaDev/Sis_HS_IETS) | Plataforma de escaneo de horizonte de tecnologías emergentes | FastAPI · React | Público |
| [riets_python](https://github.com/IETS-ColombiaDev/riets_python) | Costeo representativo de procedimientos PBS; migración a Python del paquete R rIETS | Python | Privado |

### Gestión de proyectos

| Repositorio | Descripción | Stack | Visibilidad |
|---|---|---|---|
| [Sistema-de-Gestion-de-Proyectos-del-IETS](https://github.com/IETS-ColombiaDev/Sistema-de-Gestion-de-Proyectos-del-IETS) | Sistema institucional de gestión de proyectos | TypeScript | Privado |

### Gestión documental

| Repositorio | Descripción | Stack | Visibilidad |
|---|---|---|---|
| [GD](https://github.com/IETS-ColombiaDev/GD) | Sistema de gestión documental | ASP.NET | Privado |
| [BusquedasCorrespondencia](https://github.com/IETS-ColombiaDev/BusquedasCorrespondencia) | Consultas de correspondencia | VB.NET · `legacy` | Privado |

### Soporte IT

| Repositorio | Descripción | Stack | Visibilidad |
|---|---|---|---|
| [GC](https://github.com/IETS-ColombiaDev/GC) | Base de conocimiento de soporte TI | C# | Privado |

### Herramientas internas

| Repositorio | Descripción | Stack | Visibilidad |
|---|---|---|---|
| [RRHH](https://github.com/IETS-ColombiaDev/RRHH) | Herramientas internas de talento humano | JavaScript | Privado |
| [Generador_Certificados](https://github.com/IETS-ColombiaDev/Generador_Certificados) | Generador de certificados | HTML · MIT | Privado |

## Convenciones

### Nombres de repositorio

Los repositorios nuevos se nombran en **kebab-case**, en español y sin tildes, con un nombre que explique qué es el sistema: `sistema-gestion-proyectos`, `generador-certificados`. Evita siglas sueltas como `GC` o `GD`, que no dicen nada a quien llega por primera vez.

Los repositorios existentes **no se renombran sin coordinarlo** con la Coordinación de Gestión de Tecnologías y Comunicaciones, porque despliegues, integraciones y clones locales pueden depender del nombre actual.

### Descripción

Toda descripción sigue el formato `[Área] qué hace el sistema en una frase`. Las áreas en uso son `[Soporte IT]`, `[Gestión Documental]` y `[Herramientas Internas]`; reutilízalas antes de crear una nueva.

Ejemplo: `[Soporte IT] Base de conocimiento de soporte técnico`

### Topics

Cada repositorio lleva al menos un *topic* de cada tipo:

| Tipo | Valores en uso |
|---|---|
| Lenguaje o framework | `python`, `typescript`, `javascript`, `c-sharp`, `vb-net`, `asp-net`, `html`, `css` |
| Dominio | `document-management`, `human-resources`, `knowledge-base`, `internal-tools` |
| Estado o alcance | `legacy`, `internal` |

Usa `javascript` en lugar de `js` para que el filtro por *topic* agrupe todos los proyectos.

### Visibilidad

Todo repositorio se crea **privado**. Para hacerlo público se necesita:

1. Aprobación de la Coordinación de Gestión de Tecnologías y Comunicaciones.
2. Revisión de que **todo el historial** esté libre de secretos, datos personales y datos de salud (Ley 1581 de 2012). Borrar un archivo en el último commit no lo elimina del historial.
3. Una licencia definida en `LICENSE`.
4. Un `README` completo.

### Contenido mínimo de cada repositorio

`README.md` con propósito, stack, instrucciones de ejecución, forma de despliegue y responsable; `.gitignore` adecuado al lenguaje; `.env.example` con las variables necesarias sin valores reales; y `LICENSE` si el repositorio es público.

### Ramas y cambios

La rama `main` está protegida y los cambios entran por *pull request* con al menos una revisión. Se sugiere redactar los commits con prefijos de [Conventional Commits](https://www.conventionalcommits.org/es/): `feat:`, `fix:`, `docs:`, `refactor:`.

## Secretos y datos

Nunca se suben al repositorio archivos `.env`, llaves de API, cuentas de servicio, cadenas de conexión a bases de datos ni archivos con datos personales o de pacientes.

Si un secreto llega a publicarse, **rótalo de inmediato** en el servicio de origen y reporta el incidente por ticket con el asunto `[Seguridad]`. Eliminar el commit no basta: la credencial debe considerarse comprometida.

## Sistemas legacy

Los repositorios con el *topic* `legacy` corresponden a sistemas en .NET (ASP.NET, VB.NET) que siguen en operación. Antes de intervenirlos, revisa su documentación, coordina el cambio con la Coordinación y pruébalo en un entorno distinto al de producción.

## Soporte

Accesos, incidentes y solicitudes de nuevos desarrollos se gestionan por ticket a [soporte@iets.org.co](mailto:soporte@iets.org.co) y se atienden según el Acuerdo de Nivel de Servicio (SLA) de la Coordinación de Gestión de Tecnologías y Comunicaciones.

<div align="center">
<sub>Coordinación de Gestión de Tecnologías y Comunicaciones · IETS</sub>
</div>
