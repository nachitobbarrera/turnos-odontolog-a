# Informe de Discovery — Sistemas odontológicos de gestión de turnos y agenda

**Proyecto**: turnos-odontologia
**Fecha de relevamiento**: 2026-11-18
**Alcance**: Argentina (prioridad 1), Latinoamérica (prioridad 2), soluciones internacionales de referencia (prioridad 3)
**Método**: búsqueda web y extracción de cada sitio oficial con la skill `web-scraper`. Las notas por proveedor están en [`sources/`](sources/).
**Estado**: borrador para revisión. La sección "Verificación de fuentes" queda para completar por el equipo.

---

## Criterios de lectura

- **Comprobado**: la funcionalidad figura descrita de forma explícita en el sitio oficial, el centro de ayuda o la página de precios del proveedor, en la fecha de consulta.
- **Afirmación comercial**: cifras de clientes, porcentajes de mejora (por ejemplo, "-40 % de ausentismo"), calificaciones y superlativos ("número 1", "el mejor") publicados por el propio proveedor sin metodología visible. Se transcriben con la indicación *(autodeclarado)* y no se usan como evidencia funcional.
- **No evidenciado**: la característica no aparece en las fuentes públicas consultadas. Eso no significa que el producto no la tenga: significa que no puede afirmarse con fuentes públicas.
- **Fuente secundaria**: comparativas de terceros, en especial la de Odonthia, que es un competidor, y directorios como Capterra. Se indica siempre de forma expresa y no reemplaza a la fuente oficial.
- Todas las URL se consultaron el **2026-11-18**. Los precios en ARS se ven afectados por la inflación y deben revalidarse antes de cualquier decisión.

---

## A. Tabla comparativa (16 sistemas evaluados + 1 no evaluable, por relevancia para Argentina)

*DentalCore figura en la tabla pero es **no evaluable**: su sitio oficial no respondió en la fecha de consulta.*

La relevancia para Argentina pondera tres cosas: la adaptación local (obras sociales, ARCA, Mercado Pago, pesos), la presencia o adopción declarada en el país y el ajuste al segmento de consultorios y clínicas. **No equivale a la puntuación de la sección B.**

### A.1 Identificación, segmento, modalidad y modelo comercial

| # | Producto / proveedor / país | URL oficial (consulta) | Segmento objetivo | Modalidad | Modelo comercial visible | Evidencia de adopción |
|---|---|---|---|---|---|---|
| 1 | **Bilog** / Bilog / Argentina | https://bilog.com.ar/ (2026-11-18) | Consultorio, clínica, obras sociales y gerenciadoras | Web + app móvil/tablet; archivos en la nube | Cuota mensual sin permanencia; configuración inicial sin costo; precios: No evidenciado; prueba: No evidenciado | +1.500 clínicas/consultorios, +5.000 usuarios, +150.000 turnos/mes *(autodeclarado)*; testimonios con nombre |
| 2 | **Dentalink** / Engenis SpA / Chile | https://www.softwaredentalink.com/ (2026-11-18) | Consultorio individual, clínica, multisucursal | SaaS 100 % en la nube | Planes Esencial/Pro/Titanium a cotizar; Contact Center IA USD 50/mes; prueba: No evidenciado | +15.000 clínicas, +20 países *(autodeclarado)* |
| 3 | **AgendaPro** / AgendaPro Inc. / Chile (regional) | https://agendapro.com/ar/dental/software-odontologico (2026-11-18) | Consultorio y clínica (plataforma multirrubro) | SaaS en la nube + apps iOS/Android | ARS con IVA, "desde $13.900/mes" en la página dental; prueba de 14 días; API USD 200/mes; WhatsApp y Recepcionista IA con costo adicional | +30.000 clínicas, +135.000 profesionales, 4,8 en +1.200 reseñas *(autodeclarado)* |
| 4 | **DentalTec** / Tándem Digital / Argentina (San Juan) | https://web.dentaltec.com.ar/ (2026-11-18) | Odontólogo independiente, círculos e instituciones | Web sin instalación | Precio del software: No evidenciado; packs de WhatsApp de USD 9 a 48; prueba: No evidenciado | +2.000 profesionales, +30 instituciones *(autodeclarado)*; testimonios de círculos (COSJ, Santiago del Estero, CORA) |
| 5 | **Dentia** / Dentia / Argentina | https://dentia.tech/ (2026-11-18) | Consultorio y clínica, varias sucursales | Web + PWA instalable | ARS $20.000 / $30.000 / $40.000 por mes; prueba de 30 días; anual con 2 meses gratis | "+100 clínicas" *(autodeclarado)*; sin casos con nombre |
| 6 | **DentalSoft** / DentalSoft / Argentina (La Plata y Rosario) | https://dentalsoft.com.ar/ (2026-11-18) | Consultorio y clínica; plan a medida para +10 profesionales | SaaS en la nube | Gratis 3 meses (50 turnos/mes); $30.000 y $60.000 por mes por profesional (moneda no explicitada) | 5,0 en 11 reseñas de Google |
| 7 | **Odonthia** / Genera Impacto / Argentina | https://odonthia.com/ (2026-11-18) | Odontólogo independiente y consultorio chico | 100 % web | Plan gratuito permanente; ARS $76.600 y $158.100 por mes con IVA (USD 47/97 en LatAm); créditos de IA | 4.471 consultorios *registrados* *(autodeclarado; registro ≠ uso)* |
| 8 | **Odonto.ar** / Odonto.ar / Argentina (inferido por dominio y moneda) | https://odonto.ar/ (2026-11-18) | Odontólogo, consultorio, clínica | Web (PC, tablet, celular) | USD 29 / 49 / 99 por mes por cantidad de usuarios; se paga en ARS por Mercado Pago; prueba de 30 días | No evidenciado |
| 9 | **DentalCore** / No evidenciado / Argentina (según título indexado) | https://dentalcore.app/ (2026-11-18; **sitio no accesible**) | No evidenciado | No evidenciado | No evidenciado (fuente secundaria: USD 50/mes con 2 usuarios) | No evidenciado |
| 10 | **Odonapp** / Odonapp / Argentina | https://www.odonapp.com/ (2026-11-18) | Círculos y asociaciones odontológicas (institucional) | No evidenciado | No evidenciado | +750 odontólogos *(autodeclarado)*; círculos nombrados (Neuquén, Mar del Plata, Pergamino, entre otros) |
| 11 | **Doctocliq** / Doctocliq / LatAm (origen no indicado en el sitio) | https://doctocliq.com/ (2026-11-18) | Consultorio y clínica dental y estética | SaaS + apps iOS/Android | Gratis (30 pacientes/mes); USD 19 / 29 / 49 por mes; prueba de 7 días; IA y facturación con costo adicional | +6.500 profesionales *(autodeclarado)* |
| 12 | **Clinic Cloud** / Doctoralia España (Docplanner) / España | https://clinic-cloud.com/ (2026-11-18) | Clínicas y profesionales sanitarios (generalista) | SaaS | EUR + IVA: 29 / 49 / 79 por mes; prueba gratuita; sin precios para Argentina | +12.000 doctores *(autodeclarado)* |
| 13 | **Dentidesk** / Dentidesk / Chile | https://dentidesk.com/ (2026-11-18) | Clínica, centro médico, instituciones educativas | Web + apps móviles | Precios: No evidenciado; prueba de 15 días | No evidenciado |
| 14 | **Medesk** / Medesk / No evidenciado | https://www.medesk.net/es/solutiones/odontologia (2026-11-18) | Clínica y consultorio dental | No evidenciado | Cotizador; prueba gratuita | 50 países, 15K médicos *(autodeclarado)* |
| 15 | **Dentrix Ascend** / Henry Schein One / EE. UU. | https://www.dentrixascend.com/ (2026-11-18) | Consultorio, multi-sede, DSO | SaaS 100 % cloud | Ascend Starter USD 199/mes; resto a medida | +80k usuarios *(autodeclarado)* |
| 16 | **Curve Dental** / CD Newco LLC / EE. UU. | https://www.curvedental.com/ (2026-11-18) | Independiente, multi-sede, startups | SaaS cloud-native | A cotizar | +100.000 usuarios, +6.000 sedes, 4,6 en +500 reseñas *(autodeclarado)* |
| 17 | **Open Dental** / Open Dental Software / EE. UU. | https://www.opendental.com/ (2026-11-18) | Consultorio de cualquier tamaño | No evidenciado en la home | Páginas de tarifas y prueba; monto: No evidenciado | No evidenciado |

### A.2 Agenda, turnos digitales y automatización

| # | Producto (fuente · fecha) | Gestión de agenda | Turnos digitales | Automatización |
|---|---|---|---|---|
| 1 | Bilog (bilog.com.ar · 2026-11-18) | Vistas diaria/semanal/por profesional; multi-profesional; consultorios como recurso; sobreturnos (app); arrastrar y copiar turnos. Sillones, bloqueos y anti-solapamiento: No evidenciado | Reserva, cancelación y consulta por web, redes y WhatsApp; chatbot IA "iAngela"; confirmación. Reprogramación por el paciente y lista de espera: No evidenciado | Recordatorios y confirmaciones por WhatsApp, email o llamada. Recall y campañas: No evidenciado |
| 2 | Dentalink (softwaredentalink.com · 2026-11-18) | Módulo de agenda; detalle de vistas, sillones, bloqueos y solapamiento: No evidenciado | Agenda online 24/7, agendamiento por WhatsApp, Contact Center IA, confirmación automática, reagendamiento automático (Titanium). Lista de espera: No evidenciado | Tareas automáticas de citas y controles (recall), email marketing, cobranza automática |
| 3 | AgendaPro (agendapro.com/ar · 2026-11-18) | Agenda por odontólogo y **por sillón**; duración por práctica; multisede. Bloqueos y solapamiento: No evidenciado | 24/7, link, sitio de reservas, Instagram, Messenger, Google Maps, WhatsApp, asistente IA; confirmación, cancelación y reprogramación. Lista de espera: No evidenciado | Recordatorios por WhatsApp 1–3 días antes, con reenvío si el paciente no confirma; recall de controles; campañas por email y WhatsApp |
| 4 | DentalTec (web.dentaltec.com.ar · 2026-11-18) | Turnos configurables por odontólogo, día, horario e intervalo. Vistas, sillones y bloqueos: No evidenciado | Confirmación por WhatsApp. Reserva online por el paciente: No evidenciado | Recordatorios automáticos por WhatsApp. Recall y campañas: No evidenciado |
| 5 | Dentia (dentia.tech · 2026-11-18) | Disponibilidad por profesional; sobreturnos. Vistas, sillones, bloqueos y solapamiento: No evidenciado | Asistente IA en WhatsApp 24 h que agenda, reprograma y cancela; confirmación por WhatsApp. Link web y lista de espera: No evidenciado | Recordatorios (email y WhatsApp), cumpleaños, reseñas, cuotas; recall y campañas (plan Elite) |
| 6 | DentalSoft (dentalsoft.com.ar · 2026-11-18) | Vistas diaria/semanal/mensual; multi-profesional; multi-sucursal; bloqueos; sobreturnos con **detección de solapamiento**; arrastrar y soltar. Sillones: No evidenciado | Reserva 24/7 desde la web de la clínica con disponibilidad en tiempo real; chatbot; asistente de WhatsApp (Pro); cancelación y reprogramación. Lista de espera: No evidenciado | Recordatorios por WhatsApp y email (automáticos solo en Pro); recuperación de inactivos; cobro de deudas; pedido de reseñas |
| 7 | Odonthia (odonthia.com · 2026-11-18) | Agenda incluida en el plan gratuito; detalle: No evidenciado | Reserva online y portal del paciente aparecen solo como ítems de menú: No evidenciado | WhatsApp automático en planes pagos; resto: No evidenciado |
| 8 | Odonto.ar (odonto.ar · 2026-11-18) | Vistas día/semana/mes; agenda de equipo; duración por motivo de consulta | Link de reserva con reglas de quién reserva y cómo cancelar o reprogramar | No evidenciado |
| 9 | DentalCore (dentalcore.app · 2026-11-18, no accesible) | No evidenciado | No evidenciado | No evidenciado |
| 10 | Odonapp (odonapp.com · 2026-11-18) | No evidenciado | No evidenciado | No evidenciado (solo "comunicación automatizada" con el profesional) |
| 11 | Doctocliq (doctocliq.com · 2026-11-18) | Agendas por consultorio y doctor; detalle: No evidenciado | WhatsApp con IA "Soyla"; confirmación automática. Cancelación y reprogramación: No evidenciado | Recordatorios, tratamientos pendientes, campañas, segmentación |
| 12 | Clinic Cloud (clinic-cloud.com · 2026-11-18) | Multi-profesional y multisede | Reserva 24/7 vía Doctoralia; IA telefónica (Noa Reception) | Recordatorios y confirmaciones por WhatsApp, SMS y email |
| 13 | Dentidesk (dentidesk.com · 2026-11-18) | Agenda personalizable; reprogramación; multisucursal | Agendamiento online como integración; WhatsApp "próximamente" | Solo recordatorios internos |
| 14 | Medesk (medesk.net · 2026-11-18) | Agenda con detección de huecos | Reserva online desde la web | Confirmaciones y recordatorios automáticos (canal: No evidenciado) |
| 15 | Dentrix Ascend (dentrixascend.com · 2026-11-18) | Agenda inteligente; detalle: No evidenciado | Reserva online; mensajería bidireccional; confirmaciones | Recordatorios y recare |
| 16 | Curve Dental (curvedental.com · 2026-11-18) | Agenda; detalle: No evidenciado | Reserva online; confirmación | Recordatorios y recare |
| 17 | Open Dental (opendental.com · 2026-11-18) | Bloqueos; configuración de horarios por profesional | Web Sched, portal del paciente, mensajería de texto integrada | Mensajes automáticos y recall |

### A.3 Gestión odontológica, administración e integraciones

| # | Producto (fuente · fecha) | Gestión odontológica | Administración | Integraciones |
|---|---|---|---|---|
| 1 | Bilog (bilog.com.ar · 2026-11-18) | Ficha, odontograma, adjuntos y galería, presupuestos, consentimientos firmados, receta electrónica. Anamnesis y periodontograma: No evidenciado | Cobros, liquidación de obras sociales, reportes y KPIs. ARCA, caja, señas y Mercado Pago: No evidenciado | WhatsApp, firma electrónica (Ley 25.506). API oficial de WhatsApp, Google Calendar y API pública: No evidenciado |
| 2 | Dentalink (softwaredentalink.com · 2026-11-18) | Historia, odontograma, **periodontograma**, imágenes, RX con IA, presupuestos, planes, dictado por voz | Caja, cobros presenciales y online, liquidación a profesionales, reportes; módulo Argentina con obras sociales y conciliación (títulos del centro de ayuda). ARCA: No evidenciado | Firma electrónica, API (complemento), WhatsApp. Mercado Pago y ARCA: No evidenciado |
| 3 | AgendaPro (agendapro.com/ar · 2026-11-18) | Ficha, anamnesis, odontograma, imágenes adjuntas, presupuestos, consentimiento firmado. Periodontograma: No evidenciado | Caja, cobros, señas, Mercado Pago (links y cuotas), comisiones, reportes, inventario. Obras sociales: No evidenciado; facturación electrónica: "próximamente" | WhatsApp, Google Calendar, Google Maps, Instagram, Messenger, Meta y Google Ads, Mercado Pago, API paga |
| 4 | DentalTec (web.dentaltec.com.ar · 2026-11-18) | Historia con registro temporal, imágenes, odontograma con CIE-10. Presupuestos y periodontograma: No evidenciado | **Validación en línea con +15 obras sociales** (afiliado, nomenclador, topes, autorizaciones); planillas con **ARCA**; cierre multinivel; refacturación de rechazos; liquidación a prestadores | WhatsApp ("integración oficial"), ARCA, web services de obras sociales |
| 5 | Dentia (dentia.tech · 2026-11-18) | Ficha, historia configurable, odontograma, **periodontograma**, planes, presupuestos, consentimientos, laboratorio; IA de cefalometría y panorámicas | Caja con cierre, cobros, cuotas, **factura ARCA A/B/C**, señas, **Mercado Pago**, liquidación de obras sociales y prepagas, honorarios | WhatsApp Business (coexistencia), Instagram, Messenger, Google Calendar, Mercado Pago, ARCA, firma propia, importación Excel/CSV. API pública: No evidenciado |
| 6 | DentalSoft (dentalsoft.com.ar · 2026-11-18) | Ficha, odontograma FDI de 18 estados con historial, presupuestos, planes con prioridades, ortodoncia | Caja y cierre diario, señas, Mercado Pago (Pro), obras sociales con cobertura, liquidación de obras sociales y comisiones, reportes. ARCA: No evidenciado | Google Calendar, WhatsApp, Mercado Pago, exportación a PDF y Excel. API: No evidenciado |
| 7 | Odonthia (odonthia.com · 2026-11-18) | Ficha, odontograma FDI (incluye dientes temporales), historia versionada, consentimientos firmados | Tarifario por obra social con copago (comparativa propia). **Declara no hacer** liquidación, factura ARCA ni receta | Importación CSV; firma electrónica |
| 8 | Odonto.ar (odonto.ar · 2026-11-18) | Historia, odontograma con trazabilidad, radiografías, presupuestos | Cálculo de la parte de obra social y la del paciente; panel de finanzas. ARCA, caja y liquidación: No evidenciado | Importación desde Excel |
| 9 | DentalCore (dentalcore.app · 2026-11-18, no accesible) | No evidenciado | No evidenciado (fuente secundaria: ARCA y liquidación) | No evidenciado |
| 10 | Odonapp (odonapp.com · 2026-11-18) | Solo carga por pieza, cara y código de práctica | Obras sociales en una pantalla; circuito cargada → auditada → presentada → liquidada; cuenta corriente; ARCA; stock | ARCA |
| 11 | Doctocliq (doctocliq.com · 2026-11-18) | Historia, odontograma, presupuestos, planes, archivos | Caja, cobro multimoneda, comisiones, reportes; facturación electrónica solo en PE, MX, EC y CO | WhatsApp, Meta, Google, Kommo, API de agenda |
| 12 | Clinic Cloud (clinic-cloud.com · 2026-11-18) | Historia, consentimientos; odontograma solo en el plan Max | Caja, facturación española, mutuas, presupuestos, liquidaciones, pagos online | Doctoralia, Verifactu, TicketBAI |
| 13 | Dentidesk (dentidesk.com · 2026-11-18) | Fichas de especialidad, odontograma con nomenclatura configurable | Facturación SII (Chile), Alegra (República Dominicana), +20 reportes, stock | SII, Alegra |
| 14 | Medesk (medesk.net · 2026-11-18) | Odontograma, historial | Facturación electrónica, pagos, morosos, reportes | iCal, Google Calendar |
| 15 | Dentrix Ascend (dentrixascend.com · 2026-11-18) | Charting, notas por voz, imágenes con IA, planes | Elegibilidad, claims, pagos, KPIs (mercado de EE. UU.) | API Exchange, agentes MCP |
| 16 | Curve Dental (curvedental.com · 2026-11-18) | Charting, perio, imágenes con IA, planes, formularios | Facturación a seguros, elegibilidad, pagos, analytics | Directorio de partners |
| 17 | Open Dental (opendental.com · 2026-11-18) | Odontograma 3D | Claims (+20 clearinghouses), pagos, reportes y consultas | Cientos de bridges; conversiones desde +200 sistemas |

### A.4 Operación, seguridad, fortalezas y limitaciones

| # | Producto (fuente · fecha) | Operación | Seguridad y cumplimiento | Fortalezas evidentes | Limitaciones evidentes |
|---|---|---|---|---|---|
| 1 | Bilog (bilog.com.ar · 2026-11-18) | Sucursales; soporte. Roles, auditoría y exportación: No evidenciado | Solo Ley 25.506 (firma). Ley 25.326, Ley 26.529 y backup: No evidenciado | Trayectoria y base instalada en Argentina; circuito de obras sociales; multicanal | Sin precios públicos; seguridad no documentada; ARCA no evidenciado |
| 2 | Dentalink (softwaredentalink.com · 2026-11-18) | Multisucursal (Pro); soporte | **ISO 27001**, AWS cifrado, respaldos diarios, prácticas HIPAA | Clínica completa y madura; certificación de seguridad | Sin precios; adaptación argentina parcial (sin ARCA evidenciado) |
| 3 | AgendaPro (agendapro.com/ar · 2026-11-18) | Multisede; soporte 24/7; migración gratuita. Roles y exportación: No evidenciado | AWS, cifrado, respaldos, **Ley 25.326 y Ley 26.529** declaradas | La mejor experiencia de reserva multicanal y marketing; precios en ARS | Generalista; sin obras sociales ni ARCA; muchos costos adicionales |
| 4 | DentalTec (web.dentaltec.com.ar · 2026-11-18) | 10 roles, **auditoría completa**, exportación PDF/Excel, soporte 24/7 | JWT, bcrypt, Helmet (detalle técnico); leyes y backup: No evidenciado | La integración más profunda con obras sociales y círculos | Débil en la experiencia del paciente (sin reserva online); sin precio |
| 5 | Dentia (dentia.tech · 2026-11-18) | Sucursales, 17 perfiles de rol, auditoría, **2FA**, exportación | Ley 25.326 declarada; Ley 26.529 y backup: No evidenciado | La cobertura funcional local más amplia según su sitio; precio en ARS | Producto joven, sin casos verificables; la amplitud declarada debe validarse en demo |
| 6 | DentalSoft (dentalsoft.com.ar · 2026-11-18) | Multi-sucursal, permisos por rol, historial de cambios, exportación, capacitación | Mención genérica de copias de seguridad; leyes: No evidenciado | La agenda mejor documentada (bloqueos, solapamiento); web de reserva integrada; precio en ARS | Sin ARCA; muestra de reseñas muy chica; homónimos en otros países |
| 7 | Odonthia (odonthia.com · 2026-11-18) | Registro de actividad, exportación | Respaldo; firma con hash, IP y dispositivo; leyes: No evidenciado | Gratuito y sin límite de pacientes; transparencia sobre lo que no hace | Sin obras sociales ni ARCA; muchas funciones solo como ítems de menú |
| 8 | Odonto.ar (odonto.ar · 2026-11-18) | Permisos por persona | No evidenciado (la pregunta frecuente de seguridad no muestra respuesta) | Planes simples, todas las funciones en todos los planes | Sin automatización evidenciada; precio en USD |
| 9 | DentalCore (dentalcore.app · 2026-11-18, no accesible) | No evidenciado | No evidenciado | No evidenciado | Sitio caído en la fecha de consulta |
| 10 | Odonapp (odonapp.com · 2026-11-18) | Auditoría de prestaciones, capacitación | No evidenciado | Circuito institucional de obras sociales | No es un sistema de turnos (fuera de segmento; potencial aliado) |
| 11 | Doctocliq (doctocliq.com · 2026-11-18) | Roles, exportación al darse de baja | Permisos por persona; resto: No evidenciado | Plan gratuito y precios en USD publicados | Sin adaptación argentina; inconsistencias en la página de precios |
| 12 | Clinic Cloud (clinic-cloud.com · 2026-11-18) | Multisede; soporte humano los 7 días; migración gratuita | **RGPD certificado**, cifrado, trazabilidad | Modelo marketplace + software (Doctoralia) | Orientado a España; odontograma solo en el plan superior |
| 13 | Dentidesk (dentidesk.com · 2026-11-18) | Multisucursal, administración de usuarios | Ley chilena mencionada | Fichas de especialidad | Sin WhatsApp; sin adaptación argentina |
| 14 | Medesk (medesk.net · 2026-11-18) | Roles | RGPD, backups automáticos | Agenda con detección de huecos | Sin presencia argentina evidenciada |
| 15 | Dentrix Ascend (dentrixascend.com · 2026-11-18) | Multi-sede, roles, academia | **SOC 2**, HIPAA, backups cifrados | Referencia de integraciones e IA | Mercado de EE. UU. |
| 16 | Curve Dental (curvedental.com · 2026-11-18) | Multi-sede, implementación y capacitación | Infraestructura HIPAA | Historia única del paciente; UX cloud | Sin precio; mercado de EE. UU. y Canadá |
| 17 | Open Dental (opendental.com · 2026-11-18) | Foros, webinars, documentación pública | No evidenciado | Profundidad funcional y ecosistema de integraciones | UX y mercado ajenos al contexto argentino |

---

## B. Matriz de puntuación ponderada (0 a 5)

| Sistema | Turnos y automatización (25 %) | Clínica odontológica (20 %) | Integraciones locales y WhatsApp (15 %) | Administración, cobros y facturación (15 %) | Experiencia del paciente (10 %) | Seguridad, exportación y trazabilidad (10 %) | Precio y adopción (5 %) | **Total ponderado** |
|---|---|---|---|---|---|---|---|---|
| Dentia | 4 | 5 | 5 | 5 | 4 | 4 | 5 | **4,55** |
| AgendaPro | 5 | 3 | 4 | 3 | 5 | 4 | 4 | **4,00** |
| Dentalink | 4 | 5 | 3 | 3 | 4 | 5 | 2 | **3,90** |
| DentalSoft | 5 | 3 | 3 | 4 | 4 | 3 | 5 | **3,85** |
| Dentrix Ascend | 4 | 4 | 1 | 4 | 4 | 5 | 3 | **3,60** |
| Curve Dental | 4 | 5 | 1 | 4 | 4 | 3 | 1 | **3,50** |
| Bilog | 4 | 3 | 3 | 3 | 4 | 1 | 2 | **3,10** |
| Clinic Cloud | 3 | 2 | 2 | 3 | 4 | 4 | 3 | **2,85** |
| Open Dental | 4 | 3 | 1 | 3 | 4 | 1 | 2 | **2,80** |
| DentalTec | 2 | 2 | 4 | 4 | 2 | 4 | 1 | **2,75** |
| Doctocliq | 3 | 3 | 2 | 2 | 3 | 2 | 5 | **2,70** |
| Odonto.ar | 3 | 3 | 1 | 2 | 3 | 2 | 4 | **2,50** |
| Medesk | 3 | 2 | 1 | 3 | 3 | 3 | 2 | **2,45** |
| Odonthia | 2 | 3 | 1 | 1 | 2 | 3 | 5 | **2,15** |
| Dentidesk | 2 | 3 | 1 | 2 | 1 | 1 | 2 | **1,85** |
| Odonapp | 0 | 1 | 2 | 4 | 0 | 2 | 1 | **1,35** |
| DentalCore | — | — | — | — | — | — | — | **No evaluable** |

### Nota metodológica

- **Qué mide cada nota.** 0 = sin ninguna evidencia pública en el criterio. 1 = evidencia mínima o tangencial. 2 = cobertura básica de pocos subítems. 3 = cobertura intermedia, con huecos relevantes. 4 = cobertura amplia, con uno o dos subítems sin evidencia. 5 = cobertura completa o casi completa de los subítems del criterio, según la consigna. El total es Σ (nota × peso) y su máximo es 5,00.
- **Tratamiento de "No evidenciado".** Un subítem no evidenciado **puntúa como ausente**: no se imputa ni se promedia. La matriz mide entonces **cobertura funcional demostrada públicamente**, no la calidad real del producto. Esto beneficia a los proveedores que documentan en detalle (Dentia, DentalSoft) y castiga a los que venden por demo (Bilog, Dentalink, Curve). Por eso las posiciones 1 a 7 deben confirmarse con demos antes de sacar conclusiones.
- **Fuentes secundarias** (la comparativa de Odonthia y Capterra) no suman puntos. DentalCore queda **No evaluable** porque su sitio oficial no respondió.
- **"Integraciones locales y WhatsApp"** premia de forma explícita lo argentino: ARCA, Mercado Pago, obras sociales y WhatsApp. Por eso los productos de EE. UU. reciben 1 aunque tengan ecosistemas de integración amplios.
- **"Precio y adopción"** premia los precios publicados en ARS, el plan gratuito o la prueba sin tarjeta. Un precio a cotizar reduce la facilidad de adopción.
- Las notas son juicio del analista sobre las fuentes citadas en la tabla A y pueden revisarse por criterio.

---

## C. Análisis competitivo

### C.1 Funcionalidades que ya son estándar de mercado

Aparecen comprobadas en la mayoría de los sistemas relevantes para Argentina:

- Agenda multi-profesional con vista diaria y semanal, en la web y en el celular.
- Historia clínica digital con **odontograma** (en notación FDI en los productos locales).
- **Recordatorios por WhatsApp** y confirmación de asistencia. Su ausencia, como en Dentidesk, ya es una desventaja visible.
- Presupuestos.
- Caja y registro de cobros, con reportes básicos.
- Multi-sucursal en los planes medios o superiores.
- SaaS sin instalación, con prueba gratuita o demo.

### C.2 Funcionalidades diferenciadoras reales (comprobadas, presentes en pocos)

- **Validación en línea con obras sociales** (afiliado, nomenclador, topes, autorizaciones) y circuito de círculos y federaciones: solo DentalTec (comprobado) y Odonapp (institucional).
- **Factura electrónica ARCA integrada al flujo clínico**: Dentia y DentalTec comprobados. Odonapp, en el ámbito institucional. AgendaPro todavía la anuncia como "próximamente".
- **Asistente conversacional que gestiona turnos de punta a punta por WhatsApp** (agenda, reprograma y cancela): Dentia, Dentalink, Doctocliq, AgendaPro y Bilog lo declaran. La calidad real **no es verificable sin demo**.
- **Agenda por sillón o box**: solo AgendaPro lo documenta, aunque es clave para clínicas.
- **Prevención explícita de solapamientos con sobreturnos controlados**: solo DentalSoft lo documenta.
- **Seguridad certificada** (ISO 27001 o SOC 2): solo Dentalink y Dentrix Ascend.
- **Marketplace de pacientes** (AgendaPro, Doctoralia/Clinic Cloud): genera demanda nueva, no solo gestiona la existente.

### C.3 Vacíos frecuentes del mercado argentino

1. **Nadie combina bien las dos mitades.** Los fuertes en obras sociales y ARCA (DentalTec, Odonapp, Bilog) son débiles o no documentan la experiencia digital del paciente. Los fuertes en reserva, automatización y UX (AgendaPro, Doctocliq) no resuelven obras sociales ni ARCA. Dentia declara cubrir ambas, pero sin evidencia de adopción.
2. **Lista de espera y reasignación automática de huecos liberados**: no evidenciada en **ningún** sistema argentino.
3. **Gestión de ausentes** (seguimiento, política de penalización o seña obligatoria para reincidentes): ningún proveedor la documenta como flujo explícito; los proveedores muestran solo porcentajes de reducción *(autodeclarados)*.
4. **Cumplimiento normativo documentado**: solo AgendaPro declara la Ley 25.326 y la Ley 26.529, y Dentia la 25.326. Nadie documenta conservación de la historia clínica, consentimiento para el tratamiento de datos sensibles, registro de bases de datos ni política de backup verificable.
5. **Precios opacos**: los líderes locales en obras sociales (Bilog, DentalTec, Odonapp) no publican precios, lo que frena la adopción autónoma de consultorios chicos.
6. **Agenda por recurso físico** (sillón o box, equipamiento): casi no se documenta, aunque es determinante en clínicas.
7. **Interoperabilidad**: no hay APIs públicas documentadas en los productos argentinos. Solo AgendaPro (paga) y Dentalink (complemento) mencionan una API.

### C.4 Oportunidades de innovación

- **Producto puente**: una experiencia de turnos de primer nivel (reserva multicanal, WhatsApp, recordatorios inteligentes) con el circuito argentino resuelto (obras sociales, copago, ARCA, Mercado Pago) en un solo flujo, desde la reserva hasta la liquidación.
- **Motor de agenda centrado en recursos**: profesional × sillón × duración por prestación, con prevención de solapamientos y sobreturnos con reglas.
- **Recuperación de huecos**: lista de espera automática que ofrece por WhatsApp el turno liberado por una cancelación.
- **Política de ausentismo configurable**: seña obligatoria para reincidentes, confirmación escalonada y reportes de ausentismo por profesional y por obra social.
- **Cumplimiento como diferencial de venta**: documentar públicamente cómo se aplican la Ley 25.326 y la Ley 26.529, con auditoría de accesos, exportación del paciente y backups verificables.
- **Precio transparente en ARS** con plan de entrada para el odontólogo independiente.
- **Alianzas con círculos odontológicos**: integrarse con Odonapp o DentalTec en lugar de competir en su terreno institucional.

---

## D. Recomendación final

### D.1 Cinco competidores prioritarios para analizar mediante demo

1. **Dentia**: es el que mejor puntúa por evidencia pública y el más cercano a la propuesta "puente". Hay que validar en la demo si su amplitud es real y qué tan robusto es el asistente de WhatsApp.
2. **Bilog**: el incumbente local con mayor base declarada. Hay que entender su circuito de obras sociales, su precio real y por qué retiene clientes.
3. **DentalTec**: es la referencia en validación con obras sociales y en el circuito de círculos. Define el estándar administrativo a igualar o integrar.
4. **AgendaPro**: es la referencia de reserva multicanal, automatización y marketing en ARS. Es el competidor más probable para un consultorio que prioriza la captación de pacientes.
5. **Dentalink**: es la suite regional más madura, con seguridad certificada. Hay que validar la profundidad real de su módulo para Argentina.

### D.2 Tres productos de referencia para la experiencia de usuario

1. **AgendaPro**: flujo de reserva del paciente, multicanal, recordatorios con reenvío.
2. **Curve Dental**: historia única del paciente que integra agenda, clínica y cobro en una sola vista cloud.
3. **Clinic Cloud / Doctoralia**: modelo de marketplace más software, con confirmaciones multicanal.

*(Dentrix Ascend queda como referencia secundaria de arquitectura de integraciones y API.)*

### D.3 MVP sugerido

#### D.3.1 MVP ajustado al proyecto (vigente)

Este es el MVP que adopta el roadmap. Surge de la entrevista de Discovery del 2026-11-18 ([`discovery.md`](discovery.md)).

**Imprescindibles (MVP)**
- Alta de profesionales, sillones o boxes y prestaciones con duración variable.
- Crear, reprogramar y cancelar turnos con **prevención de solapamientos por profesional y por sillón** (intervalos [inicio, fin), inicio en múltiplos de 5 minutos, compatibilidad entre prestación, profesional y sillón, horario laboral y anticipación mínima configurable).
- Bloqueos de agenda.
- Entrega como API REST + frontend en TypeScript vanilla con Tailwind, con tests automatizados.
- Una sola clínica y una sola sede, zona horaria America/Argentina/Buenos_Aires. Roles modelados en el dominio, sin autenticación.
- Datos ficticios únicamente. Las leyes 25.326 y 26.529 como requisito de diseño.

**Para la entrega del 25/11/2026 se implementa un único change** de este MVP. El resto queda planificado en el roadmap.

**Para después**
- Consulta de huecos disponibles, lista de espera y recordatorios (las notificaciones se modelan con un puerto y un adaptador simulado).
- Reserva online por link, ficha clínica y odontograma, obras sociales, cobros.
- Todo lo que D.3.2 ya dejaba para etapas posteriores.

> **Nota: qué se movió respecto de la recomendación original y por qué**
>
> | Elemento | Original (D.3.2) | Ajustado (D.3.1) | Motivo |
> |---|---|---|---|
> | Agenda por sillón o box | Diferenciador (v1 o v1.1) | **Imprescindible** | El segmento elegido (consultorio o clínica chica con varios sillones) lo necesita; además es un vacío documentado del mercado (C.3, punto 6) |
> | Reserva online por link | Imprescindible | Para después | Plazo de una semana y equipo de 5 |
> | Recordatorios por WhatsApp | Imprescindible (API oficial) | Para después, a través de un adaptador simulado | La API oficial de WhatsApp es paga y requiere verificar la empresa ante Meta; queda prohibido usar servicios pagos o verificaciones externas |
> | Ficha, anamnesis y odontograma FDI | Imprescindible | Para después | Plazo; el núcleo del producto es la agenda |
> | Obra social y copago | Imprescindible | Para después | Plazo; depende de nomencladores que exceden el MVP |
> | Roles, auditoría y exportación | Imprescindible | Roles en el dominio sin login; auditoría y exportación como preguntas abiertas | Sin autenticación en el MVP; el alcance de la auditoría se define en la knowledge base |
> | Precio en ARS | Imprescindible | Fuera del alcance académico | No hay comercialización en la entrega |
> | Lista de espera | Diferenciador | Para después | Plazo de una semana |
> | Seña para ausentismo con Mercado Pago | Diferenciador | Para después | Mercado Pago es un servicio externo |
> | Consulta de huecos disponibles | No figuraba | Para después | Decisión del usuario en la entrevista |
>
> **En síntesis**: el MVP se achicó por tres razones: el **equipo** (5 estudiantes), el **plazo** (entrega el 25/11/2026, en una semana, con un solo change implementado) y el **costo de las integraciones** (WhatsApp, ARCA y Mercado Pago requieren pagos o verificaciones externas). Se mantuvo la tesis del informe, turnos primero, y se profundizó en el vacío de la agenda por sillón.

#### D.3.2 Recomendación original del análisis (se conserva como referencia)

**Imprescindibles (v1)**
- Agenda multi-profesional con vistas diaria y semanal, duración por prestación, bloqueos y **prevención de solapamientos**.
- Reserva online del paciente por link web, con confirmación, cancelación y reprogramación según reglas configurables.
- Recordatorios y confirmación por WhatsApp (API oficial) y email.
- Ficha del paciente con anamnesis y odontograma FDI.
- Registro de obra social o prepaga del paciente y cálculo de copago.
- Roles y permisos básicos, registro de auditoría de accesos y cambios, exportación de datos del paciente.
- Precio publicado en ARS.

**Diferenciadores (v1 o v1.1)**
- Agenda por **sillón o box**.
- **Lista de espera automática** que ofrece por WhatsApp los turnos liberados.
- Política de ausentismo configurable (seña con Mercado Pago para reincidentes y reportes de ausentismo).
- Documentación pública de cumplimiento (Ley 25.326 y Ley 26.529).

**Para etapas posteriores**
- Facturación electrónica ARCA.
- Liquidación y validación en línea con obras sociales (o integración con DentalTec u Odonapp).
- Periodontograma, imágenes y RX, IA clínica.
- Asistente conversacional con IA.
- Marketing y campañas, recall avanzado.
- Multi-sucursal, API pública, receta electrónica, firma digital.

> D.3.2 fue la **propuesta del analista** basada solo en el relevamiento, sin conocer el equipo ni el plazo. El alcance vigente es D.3.1.

---

## Fuentes consultadas (2026-11-18)

**Oficiales**: https://bilog.com.ar/ · https://bilog.com.ar/soluciones/consultorios · https://web.dentaltec.com.ar/ · https://web.dentaltec.com.ar/funcionalidades · https://dentalsoft.com.ar/ · https://dentia.tech/ · https://odonthia.com/ · https://odonto.ar/ · https://www.odonapp.com/ · https://dentalcore.app/ (no accesible) · https://agendapro.com/ar/dental/software-odontologico · https://agendapro.com/ar/planes · https://www.softwaredentalink.com/ · https://ayuda.softwaredentalink.com/es/collections/19196578-modulo-exclusivo-para-argentina · https://doctocliq.com/ · https://doctocliq.com/planes-y-precios · https://dentidesk.com/ · https://clinic-cloud.com/ · https://clinic-cloud.com/tarifas/ · https://www.medesk.net/es/solutiones/odontologia · https://www.dentrixascend.com/ · https://www.curvedental.com/ · https://www.opendental.com/

**Secundarias (no puntúan)**: https://odonthia.com/blog/mejores-software-odontologicos-argentina-2026 (comparativa de un competidor) · https://www.capterra.es/software/196361/dentalink · https://www.capterra.es/software/184029/dentidesk

**No accesibles en la fecha**: https://dentalcore.app/ · https://www.doctoralia.com.ar/ · https://www.infomed.es/ (Gesden). Por eso Doctoralia y Gesden quedaron fuera de la tabla.

---

## Verificación de fuentes

