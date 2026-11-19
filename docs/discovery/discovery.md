# Discovery — turnos-odontologia

**Fecha**: 2026-11-18
**Fuentes investigadas**: 16 sistemas evaluados + 1 no evaluable (DentalCore, sitio sin respuesta). Ver [`informe-discovery.md`](informe-discovery.md) y [`sources/`](sources/).
**Estado**: confirmado por el usuario en el cierre de la entrevista (2026-11-18).

## 1. Problema que resuelve

Los consultorios y clínicas odontológicas chicas que tienen varios profesionales y varios sillones o boxes coordinan los turnos sin controlar al mismo tiempo la disponibilidad del profesional y la del sillón. El resultado son superposiciones y huecos mal aprovechados. Casi ningún sistema del mercado documenta una agenda por sillón (informe, C.3, punto 6).

Se construye un SaaS argentino por suscripción, en el marco de un trabajo académico.

## 2. Usuarios / roles

Los roles se modelan en el dominio como **quién ejecuta cada operación**. No hay login en el MVP.

- **Administrador**: da de alta profesionales, sillones o boxes y prestaciones, y configura horarios.
- **Recepcionista**: crea, reprograma y cancela turnos de cualquier profesional.
- **Odontólogo**: consulta su agenda y carga sus propios bloqueos.
- **Paciente**: es un dato del turno; no opera el sistema.

## 3. Casos de uso

1. Como administrador, quiero registrar profesionales, sillones y prestaciones con su duración y compatibilidad, para que la agenda refleje los recursos reales.
2. Como recepcionista, quiero crear un turno eligiendo prestación, profesional, sillón y hora, y que el sistema rechace cualquier solapamiento.
3. Como recepcionista, quiero reprogramar o cancelar un turno respetando la anticipación mínima, para liberar el horario.
4. Como odontólogo, quiero bloquear franjas de mi agenda para que no se den turnos ahí.

*(Consultar huecos disponibles queda para después: ver el punto 6.)*

## 4. Competidores / soluciones existentes

Se relevaron **16 sistemas evaluados y 1 no evaluable** (DentalCore, cuyo sitio no respondió). La tabla completa y la matriz de puntuación están en el informe.

| Competidor | Por qué importa | Pricing | Diferenciador |
|---|---|---|---|
| Dentia (AR) | El más cercano a la propuesta "puente" según la evidencia pública | ARS 20.000 a 40.000 por mes | IA en WhatsApp + factura ARCA |
| Bilog (AR) | Incumbente local con mayor base declarada | No publicado | Liquidación de obras sociales, +20 años |
| DentalTec (AR) | Estándar en validación con obras sociales | No publicado (packs de WhatsApp en USD) | Web services con obras sociales y círculos |
| AgendaPro (regional) | Referencia de reserva multicanal; **única que documenta agenda por sillón** | ARS desde 13.900 por mes | Marketplace de pacientes + marketing |
| Dentalink (CL) | Suite regional más madura | A cotizar | ISO 27001, periodontograma, RX con IA |

**Notas**: solo DentalSoft documenta la detección de solapamientos y solo AgendaPro la agenda por sillón. Ninguno documenta el control combinado de profesional y sillón, que es la base del MVP.

## 5. Funcionalidades necesarias

MVP del roadmap:

- Alta de profesionales, sillones o boxes y prestaciones con duración variable.
- Crear, reprogramar y cancelar turnos con **prevención de solapamientos por profesional y por sillón**.
- Bloqueos de agenda.
- Entrega como API REST + frontend en TypeScript vanilla con Tailwind, con **tests automatizados**.

**Para la entrega del 25/11/2026 se implementa un único change**, que se elige en la fase de roadmap. El resto del MVP queda planificado en el roadmap.

## 6. Funcionalidades opcionales (para después)

- Consulta de huecos disponibles para una prestación (profesional y sillón compatibles libres).
- Lista de espera.
- Recordatorios (a través del adaptador de notificaciones).
- Reserva online por link.
- Ficha clínica y odontograma.
- Obras sociales, cobros, ARCA, Mercado Pago, API oficial de WhatsApp.
- Autenticación, multi-tenant, multi-sede.
- El resto de lo que la sección D.3 del informe ya dejaba para etapas posteriores.

## 7. Reglas de negocio

- Un profesional no puede tener dos turnos superpuestos.
- Un sillón o box no puede tener dos turnos superpuestos.
- Los intervalos son **[inicio, fin)**: un turno que empieza exactamente cuando termina otro no se considera solapado.
- La duración de la prestación determina la hora de fin del turno.
- No se dan turnos en horarios bloqueados.
- Los turnos solo se crean dentro del horario laboral del profesional.
- Cada prestación define qué profesionales pueden hacerla y qué sillones sirven (compatibilidad).
- No se puede cancelar ni reprogramar con menos de N horas de anticipación (N configurable).
- Cancelar un turno libera el horario del profesional y del sillón.
- Los turnos empiezan en múltiplos de 5 minutos.

## 8. Integraciones

- Ninguna integración real en el MVP.
- Las notificaciones se modelan con un **puerto y un adaptador** simulado (email o registro), para conectar WhatsApp más adelante sin tocar el dominio.
- La API oficial de WhatsApp, ARCA y Mercado Pago quedan fuera del MVP: son servicios pagos o requieren verificaciones externas.

## 9. Restricciones

- Equipo de 5 estudiantes, trabajo académico.
- **Entrega: miércoles 25/11/2026** (una semana desde el inicio del Discovery).
- Se implementa un único change, según pide la cátedra.
- Stack definido por el grupo: backend Spring Boot con Gradle y PostgreSQL, corriendo en local con Docker Compose; frontend **obligatorio** en TypeScript vanilla con Tailwind.
- Interfaz gráfica obligatoria: API REST + frontend en TypeScript vanilla con Tailwind, con tests automatizados.
- Sin servicios pagos ni verificaciones externas.
- **Nunca datos reales de pacientes**, ni en el repositorio ni en los ejemplos.
- Las leyes 25.326 (datos personales) y 26.529 (derechos del paciente e historia clínica) son requisito de diseño.

### Decisiones cerradas

- La v1 es para **una sola clínica**, sin multi-tenant. El diseño no debe impedir agregarlo después.
- Zona horaria única: **America/Argentina/Buenos_Aires**.
- Una sola sede.
- Cada turno tiene exactamente **un profesional y un sillón**.
- Sin autenticación en el MVP: los roles se modelan en el dominio.
- **Stack**: backend Spring Boot con Gradle y PostgreSQL, corriendo en local con Docker Compose; frontend **obligatorio** en TypeScript vanilla con Tailwind.

## 10. Riesgos

- **Riesgo principal**: una semana para todo el trabajo (informe, fundación, change, video y reflexión). Cada fase tiene que quedar acotada y el change tiene que ser chico y verificable.
- **Supuesto sin probar**: que la agenda por sillón sea un dolor real de las clínicas. Se deduce de que los competidores no la documentan, no de entrevistas con usuarios.
- **Concurrencia**: dos reservas simultáneas sobre el mismo hueco es un caso fácil de subestimar.
- **Cumplimiento declarativo**: las leyes 25.326 y 26.529 pueden quedar como una mención si no se bajan a requisitos verificables (datos ficticios, auditoría, datos mínimos).

## 11. Preguntas abiertas

**Del dominio**
- ¿Cuál es el valor por defecto de N (horas de anticipación)? ¿Aplica igual a cancelar y a reprogramar?
- ¿Se puede bloquear una franja que ya tiene turnos asignados? ¿Qué pasa con esos turnos?
- ¿Cuál es el único change que se implementa para la entrega? Se decide en la fase de roadmap.

**Prevención de solapamientos** (ningún competidor documenta el control combinado de profesional y sillón)
- ¿Cómo se trata un sobreturno: se prohíbe o se permite con una marca explícita?
- ¿Cómo se resuelve la concurrencia entre dos operaciones sobre el mismo hueco?
- ¿Hay tiempo de preparación o limpieza del sillón entre turnos?

**Bloqueos** (solo DentalSoft y Open Dental los documentan; nadie describe su efecto sobre turnos existentes)
- ¿Los bloqueos son puntuales o también recurrentes?
- ¿Hay bloqueos por sillón (mantenimiento) además de por profesional?

**Cumplimiento normativo** (solo AgendaPro declara las leyes 25.326 y 26.529, y Dentia solo la 25.326; ninguno documenta cómo las aplica)
- ¿Qué datos mínimos del paciente guarda la v1?
- ¿Cómo se registra la auditoría de quién hizo cada operación?
- ¿Qué política de conservación y exportación de datos se adopta?

**Ausentismo y lista de espera** (ningún competidor argentino documenta lista de espera ni un flujo explícito de ausentes)
- ¿Qué política se adopta cuando lleguen al roadmap (orden, plazo para aceptar, seña para reincidentes)?

**Integraciones** (ningún producto argentino documenta una API pública; la API oficial de WhatsApp casi no está evidenciada)
- ¿Qué contrato tiene el puerto de notificaciones para que WhatsApp pueda conectarse sin cambiar el dominio?
