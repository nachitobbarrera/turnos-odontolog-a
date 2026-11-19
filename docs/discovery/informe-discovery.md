# Informe de Discovery

## Sistemas odontológicos de gestión de turnos y agenda: relevamiento de mercado y MVP recomendado

| | |
|---|---|
| **Materia** | Metodología I |
| **Proyecto** | turnos-odontologia |
| **Integrantes** | Juan Ignacio Barrera · Maximiliano Kotlik · Francisco Marsala · Octavio Guevara · Matias Barfi |
| **Fecha** | 18/11/2026 |

---

## Resumen ejecutivo

**Qué se investigó.** Se relevaron sistemas de gestión odontológica que permiten administrar turnos y la agenda de pacientes. La prioridad fue Argentina, después Latinoamérica y, por último, soluciones internacionales de referencia. Se consultaron solo fuentes públicas verificables: sitios oficiales, páginas de precios y centros de ayuda. Todas las consultas se hicieron el 18/11/2026. Se identificaron 17 sistemas: **16 evaluados y 1 no evaluable** (DentalCore, cuyo sitio no respondió). Cada sistema se comparó en siete criterios ponderados. Toda característica sin respaldo público figura como "No evidenciado".

**Principales hallazgos.**
1. El estándar de mercado ya incluye agenda multi-profesional, odontograma, recordatorios por WhatsApp, presupuestos, caja básica y modalidad SaaS.
2. El mercado argentino está partido en dos. Un grupo documenta el circuito administrativo local: validación con obras sociales, facturación ARCA y liquidación (DentalTec, Odonapp, Bilog). Otro grupo documenta la experiencia digital del paciente: reserva multicanal, automatización y marketing (AgendaPro, Doctocliq). Solo Dentia declara cubrir ambos, sin evidencia pública de adopción.
3. Hay vacíos que ningún sistema argentino documenta: el control combinado de disponibilidad del profesional y del sillón (solo AgendaPro documenta agenda por sillón y solo DentalSoft la detección de solapamientos), la lista de espera, la gestión explícita de ausentes y la forma en que se aplican las leyes 25.326 y 26.529.
4. La matriz de puntuación mide la **cobertura funcional documentada públicamente**, no la calidad real de cada producto. Los cinco competidores prioritarios (Dentia, Bilog, DentalTec, AgendaPro y Dentalink) deben validarse mediante demos.

**MVP recomendado (D.3.1).** Una agenda para consultorios y clínicas chicas con varios profesionales y varios sillones o boxes. Incluye alta de profesionales, sillones y prestaciones con duración variable; creación, reprogramación y cancelación de turnos con **prevención de solapamientos por profesional y por sillón**; y bloqueos de agenda. Se entrega como API REST con frontend en TypeScript vanilla y Tailwind, con tests automatizados, para una sola clínica y sin integraciones pagas. Para la entrega del 25/11/2026 se implementa un único change; el resto queda planificado en el roadmap.

---

## Criterios de lectura

- **Comprobado**: la funcionalidad figura descrita de forma explícita en el sitio oficial, el centro de ayuda o la página de precios del proveedor, en la fecha de consulta.
- **Afirmación comercial**: cifras de clientes, porcentajes de mejora (por ejemplo, "-40 % de ausentismo"), calificaciones y superlativos ("número 1", "el mejor") publicados por el propio proveedor sin metodología visible. Se transcriben con la indicación *(autodeclarado)* y no se usan como evidencia funcional.
- **Juicio del analista**: valoraciones propias de este informe. Se indican con *(juicio del analista)* y no son datos del proveedor.
- **No evidenciado**: la característica no aparece en las fuentes públicas consultadas. Eso no significa que el producto no la tenga: significa que no puede afirmarse con fuentes públicas. **No se deduce** a partir de indicios indirectos como el dominio, la moneda o el idioma; esos indicios se registran aparte, como pistas.
- **Fuente secundaria**: comparativas de terceros, en especial la de Odonthia, que es un competidor, y directorios como Capterra. Se indica siempre de forma expresa y no reemplaza a la fuente oficial.
- Todas las URL se consultaron el **18/11/2026**. Las notas de extracción por proveedor están en [`sources/`](sources/). Los precios en ARS se ven afectados por la inflación y deben revalidarse antes de cualquier decisión.

---

## A. Tabla comparativa (16 sistemas evaluados + 1 no evaluable, por relevancia para Argentina)

*DentalCore figura en la tabla pero es **no evaluable**: su sitio oficial no respondió en la fecha de consulta.*

La relevancia para Argentina pondera tres cosas: la adaptación local (obras sociales, ARCA, Mercado Pago, pesos), la presencia o adopción declarada en el país y el ajuste al segmento de consultorios y clínicas. **No equivale a la puntuación de la sección B.**

### A.1 Identificación, segmento, modalidad y modelo comercial

| # | Producto / proveedor / país | URL oficial (consulta) | Segmento objetivo | Modalidad | Modelo comercial visible | Evidencia de adopción |
|---|---|---|---|---|---|---|
| 1 | **Bilog** / Bilog / Argentina | https://bilog.com.ar/ (18/11/2026) | Consultorio, clínica, obras sociales y gerenciadoras | Web + app móvil/tablet; archivos en la nube | Cuota mensual sin permanencia; configuración inicial sin costo; precios: No evidenciado; prueba: No evidenciado | +1.500 clínicas/consultorios, +5.000 usuarios, +150.000 turnos/mes *(autodeclarado)*; testimonios con nombre |
| 2 | **Dentalink** / Engenis SpA / Chile (sede publicada en Santiago) | https://www.softwaredentalink.com/ (18/11/2026) | Consultorio individual, clínica, multisucursal | SaaS 100 % en la nube | Planes Esencial/Pro/Titanium a cotizar; Contact Center IA USD 50/mes; prueba: No evidenciado | +15.000 clínicas, +20 países *(autodeclarado)* |
| 3 | **AgendaPro** / AgendaPro Inc. / No evidenciado (ver nota A.1-c) | https://agendapro.com/ar/dental/software-odontologico (18/11/2026) | Consultorio y clínica (plataforma multirrubro) | SaaS en la nube + apps iOS/Android | ARS con IVA, "desde $13.900/mes" en la página dental; prueba de 14 días; API USD 200/mes; WhatsApp y Recepcionista IA con costo adicional | +30.000 clínicas, +135.000 profesionales, 4,8 en +1.200 reseñas *(autodeclarado)* |
| 4 | **DentalTec** / Tándem Digital / Argentina (San Juan) | https://web.dentaltec.com.ar/ (18/11/2026) | Odontólogo independiente, círculos e instituciones | Web sin instalación | Precio del software: No evidenciado; packs de WhatsApp de USD 9 a 48; prueba: No evidenciado | +2.000 profesionales, +30 instituciones *(autodeclarado)*; testimonios de círculos (COSJ, Santiago del Estero, CORA) |
| 5 | **Dentia** / Dentia / Argentina ("Hecho en Argentina") | https://dentia.tech/ (18/11/2026) | Consultorio y clínica, varias sucursales | Web + PWA instalable | ARS $20.000 / $30.000 / $40.000 por mes; prueba de 30 días; anual con 2 meses gratis | "+100 clínicas" *(autodeclarado)*; sin casos con nombre |
| 6 | **DentalSoft** / DentalSoft / Argentina (La Plata y Rosario) | https://dentalsoft.com.ar/ (18/11/2026) | Consultorio y clínica; plan a medida para +10 profesionales | SaaS en la nube | Gratis 3 meses (50 turnos/mes); $30.000 y $60.000 por mes por profesional, **moneda no explicitada** (ver nota A.1-e) | 5,0 en 11 reseñas de Google |
| 7 | **Odonthia** / Genera Impacto / Argentina ("Hecho en Argentina") | https://odonthia.com/ (18/11/2026) | Odontólogo independiente y consultorio chico | 100 % web | Plan gratuito permanente; ARS $76.600 y $158.100 por mes con IVA (USD 47/97 en LatAm); créditos de IA | 4.471 consultorios *registrados* *(autodeclarado; registro ≠ uso)* |
| 8 | **Odonto.ar** / Odonto.ar / No evidenciado (ver nota A.1-a) | https://odonto.ar/ (18/11/2026) | Odontólogo, consultorio, clínica | Web (PC, tablet, celular) | USD 29 / 49 / 99 por mes por cantidad de usuarios; se paga en pesos por Mercado Pago; prueba de 30 días | No evidenciado |
| 9 | **DentalCore** / No evidenciado / No evidenciado (ver nota A.1-b) | https://dentalcore.app/ (18/11/2026; **sitio no accesible**) | No evidenciado | No evidenciado | No evidenciado (fuente secundaria: USD 50/mes con 2 usuarios) | No evidenciado |
| 10 | **Odonapp** / Odonapp / Argentina ("Hecho en Argentina") | https://www.odonapp.com/ (18/11/2026) | Círculos y asociaciones odontológicas (institucional) | No evidenciado | No evidenciado | +750 odontólogos *(autodeclarado)*; círculos nombrados (Neuquén, Mar del Plata, Pergamino, entre otros) |
| 11 | **Doctocliq** / Doctocliq / No evidenciado (ver nota A.1-a) | https://doctocliq.com/ (18/11/2026) | Consultorio y clínica dental y estética | SaaS + apps iOS/Android | Gratis (30 pacientes/mes); USD 19 / 29 / 49 por mes; prueba de 7 días; IA y facturación con costo adicional | +6.500 profesionales *(autodeclarado)* |
| 12 | **Clinic Cloud** / Doctoralia España SL (Docplanner) / España (sede publicada en Barcelona) | https://clinic-cloud.com/ (18/11/2026) | Clínicas y profesionales sanitarios (generalista) | SaaS | EUR + IVA: 29 / 49 / 79 por mes; prueba gratuita; sin precios para Argentina | +12.000 doctores *(autodeclarado)* |
| 13 | **Dentidesk** / Dentidesk / Chile (oficina publicada en Santiago) | https://dentidesk.com/ (18/11/2026) | Clínica, centro médico, instituciones educativas | Web + apps móviles | Precios: No evidenciado; prueba de 15 días | No evidenciado |
| 14 | **Medesk** / Medesk / No evidenciado | https://www.medesk.net/es/solutiones/odontologia (18/11/2026) | Clínica y consultorio dental | No evidenciado | Cotizador; prueba gratuita | 50 países, 15K médicos *(autodeclarado)* |
| 15 | **Dentrix Ascend** / Henry Schein One / EE. UU. (domicilio publicado en American Fork, Utah) | https://www.dentrixascend.com/ (18/11/2026) | Consultorio, multi-sede, DSO | SaaS 100 % cloud | Ascend Starter USD 199/mes; resto a medida | +80k usuarios *(autodeclarado)* |
| 16 | **Curve Dental** / CD Newco LLC / EE. UU. (sede publicada en Alpharetta, GA) | https://www.curvedental.com/ (18/11/2026) | Independiente, multi-sede, startups | SaaS cloud-native | A cotizar | +100.000 usuarios, +6.000 sedes, 4,6 en +500 reseñas *(autodeclarado)* |
| 17 | **Open Dental** / Open Dental Software / No evidenciado (ver nota A.1-d) | https://www.opendental.com/ (18/11/2026) | Consultorio de cualquier tamaño | No evidenciado en la home | Páginas de tarifas y prueba; monto: No evidenciado | No evidenciado |

**Notas de A.1: indicios no utilizados como evidencia.** Estos indicios se registran para que el equipo los verifique, pero **no se usaron para completar la tabla**.

- **A.1-a. Odonto.ar y Doctocliq.** Odonto.ar usa dominio `.ar`, muestra precios que se pagan en pesos y cobra por Mercado Pago, pero no declara su país. Doctocliq declara presencia en más de 20 países de Latinoamérica y adaptación fiscal en Perú, México, Ecuador y Colombia, pero no indica su país de origen; una comparativa de un tercero (Odonthia) lo ubica en Perú.
- **A.1-b. DentalCore.** El título del sitio indexado por el buscador dice "Software y Programa de Gestión Dental para Argentina", y una comparativa de un tercero (Odonthia) lo ubica en La Plata. El sitio no respondió, así que ningún dato pudo verificarse.
- **A.1-c. AgendaPro.** Se relevó la página para Argentina (`/ar`), que no indica el país de origen de la empresa.
- **A.1-d. Open Dental.** La home publica un teléfono con característica 503 y conexión con *clearinghouses* de seguros, pero no declara país.
- **A.1-e. DentalSoft.** La página muestra los montos con el signo "$" sin indicar la moneda. Solo usa "USD" de forma explícita para el costo de los mensajes de WhatsApp que cobra Meta. Una comparativa de un tercero (Odonthia) informa los mismos montos en ARS, pero no es una fuente oficial.

### A.2 Agenda, turnos digitales y automatización

| # | Producto · fuente específica (consulta) | Gestión de agenda | Turnos digitales | Automatización |
|---|---|---|---|---|
| 1 | Bilog · https://bilog.com.ar/ (secciones de funcionalidades de la home) (18/11/2026) | Vistas diaria/semanal/por profesional; multi-profesional; consultorios como recurso; sobreturnos (app); arrastrar y copiar turnos. Sillones, bloqueos y anti-solapamiento: No evidenciado | Reserva, cancelación y consulta por web, redes y WhatsApp; chatbot IA "iAngela"; confirmación. Reprogramación por el paciente y lista de espera: No evidenciado | Recordatorios y confirmaciones por WhatsApp, email o llamada. Recall y campañas: No evidenciado |
| 2 | Dentalink · https://www.softwaredentalink.com/ (módulos, planes y FAQ de la home) (18/11/2026) | Módulo de agenda; detalle de vistas, sillones, bloqueos y solapamiento: No evidenciado | Agenda online 24/7, agendamiento por WhatsApp, Contact Center IA, confirmación automática, reagendamiento automático (Titanium). Lista de espera: No evidenciado | Tareas automáticas de citas y controles (recall), email marketing, cobranza automática |
| 3 | AgendaPro · https://agendapro.com/ar/dental/software-odontologico (18/11/2026) | Agenda por odontólogo y **por sillón**; duración por práctica; multisede. Bloqueos y solapamiento: No evidenciado | 24/7, link, sitio de reservas, Instagram, Messenger, Google Maps, WhatsApp, asistente IA; confirmación, cancelación y reprogramación. Lista de espera: No evidenciado | Recordatorios por WhatsApp 1–3 días antes (FAQ de la misma página), con reenvío si el paciente no confirma; recall de controles; campañas por email y WhatsApp |
| 4 | DentalTec · https://web.dentaltec.com.ar/funcionalidades (agenda) y https://web.dentaltec.com.ar/ (confirmación) (18/11/2026) | Turnos configurables por odontólogo, día, horario e intervalo. Vistas, sillones y bloqueos: No evidenciado | Confirmación por WhatsApp. Reserva online por el paciente: No evidenciado | Recordatorios automáticos por WhatsApp. Recall y campañas: No evidenciado |
| 5 | Dentia · https://dentia.tech/ (funcionalidades y https://dentia.tech/#precios) (18/11/2026) | Disponibilidad por profesional; sobreturnos. Vistas, sillones, bloqueos y solapamiento: No evidenciado | Asistente IA en WhatsApp 24 h que agenda, reprograma y cancela; confirmación por WhatsApp. Link web y lista de espera: No evidenciado | Recordatorios (email y WhatsApp), cumpleaños, reseñas, cuotas; recall y campañas (plan Elite, según https://dentia.tech/#precios) |
| 6 | DentalSoft · https://dentalsoft.com.ar/ (secciones de funcionalidades y planes de la home) (18/11/2026) | Vistas diaria/semanal/mensual; multi-profesional; multi-sucursal; bloqueos; sobreturnos con **detección de solapamiento**; arrastrar y soltar. Sillones: No evidenciado | Reserva 24/7 desde la web de la clínica con disponibilidad en tiempo real; chatbot; asistente de WhatsApp (Pro); cancelación y reprogramación. Lista de espera: No evidenciado | Recordatorios por WhatsApp y email (automáticos solo en Pro); recuperación de inactivos; cobro de deudas; pedido de reseñas |
| 7 | Odonthia · https://odonthia.com/ (18/11/2026) | Agenda incluida en el plan gratuito; detalle: No evidenciado | Reserva online y portal del paciente aparecen solo como ítems de menú: No evidenciado | WhatsApp automático en planes pagos (sección de planes); resto: No evidenciado |
| 8 | Odonto.ar · https://odonto.ar/ (18/11/2026) | Vistas día/semana/mes; agenda de equipo; duración por motivo de consulta | Link de reserva con reglas de quién reserva y cómo cancelar o reprogramar | No evidenciado |
| 9 | DentalCore · https://dentalcore.app/ (18/11/2026, no accesible) | No evidenciado | No evidenciado | No evidenciado |
| 10 | Odonapp · https://www.odonapp.com/ (18/11/2026) | No evidenciado | No evidenciado | No evidenciado (solo "comunicación automatizada" con el profesional) |
| 11 | Doctocliq · https://doctocliq.com/ y https://doctocliq.com/planes-y-precios (recordatorios por plan) (18/11/2026) | Agendas por consultorio y doctor; detalle: No evidenciado | WhatsApp con IA "Soyla"; confirmación automática. Cancelación y reprogramación: No evidenciado | Recordatorios (cupo de WhatsApp de 50 a 150 por mes según el plan), tratamientos pendientes, campañas, segmentación |
| 12 | Clinic Cloud · https://clinic-cloud.com/ y https://clinic-cloud.com/tarifas/ (18/11/2026) | Multi-profesional y multisede; agendas por plan (1, 3 o 5) | Reserva 24/7 vía Doctoralia (incluida desde el plan Mini, según tarifas); IA telefónica (Noa Reception) | Recordatorios y confirmaciones por WhatsApp, SMS y email; el SMS es un extra a convenir |
| 13 | Dentidesk · https://dentidesk.com/ (18/11/2026) | Agenda personalizable; reprogramación; multisucursal | Agendamiento online como integración; WhatsApp "próximamente" | Solo recordatorios internos |
| 14 | Medesk · https://www.medesk.net/es/solutiones/odontologia (18/11/2026) | Agenda con detección de huecos | Reserva online desde la web | Confirmaciones y recordatorios automáticos (canal: No evidenciado) |
| 15 | Dentrix Ascend · https://www.dentrixascend.com/ (enlaza a /dental-solutions/marketing-and-patient-experience/) (18/11/2026) | Agenda inteligente; detalle: No evidenciado | Reserva online; mensajería bidireccional; confirmaciones | Recordatorios y recare |
| 16 | Curve Dental · https://www.curvedental.com/ (enlaza a /dental-scheduling-software y /dental-patient-engagement-software) (18/11/2026) | Agenda; detalle: No evidenciado | Reserva online; confirmación | Recordatorios y recare |
| 17 | Open Dental · https://www.opendental.com/ (enlaza a site/websched.html, site/patientportal.html, site/textintegrated.html, site/ereminders.html) (18/11/2026) | Bloqueos; configuración de horarios por profesional (notas de versión 26.3 en la home) | Web Sched, portal del paciente, mensajería de texto integrada | Mensajes automáticos y recall |

### A.3 Gestión odontológica, administración e integraciones

| # | Producto · fuente específica (consulta) | Gestión odontológica | Administración | Integraciones |
|---|---|---|---|---|
| 1 | Bilog · https://bilog.com.ar/ (home); https://bilog.com.ar/soluciones/consultorios (confirma la ausencia de precios y de detalle por plan) (18/11/2026) | Ficha, odontograma, adjuntos y galería, presupuestos, consentimientos firmados, receta electrónica. Anamnesis y periodontograma: No evidenciado | Cobros, liquidación de obras sociales, reportes y KPIs. ARCA, caja, señas y Mercado Pago: No evidenciado | WhatsApp, firma electrónica (Ley 25.506). API oficial de WhatsApp, Google Calendar y API pública: No evidenciado |
| 2 | Dentalink · https://www.softwaredentalink.com/ (home); https://ayuda.softwaredentalink.com/es/collections/19196578-modulo-exclusivo-para-argentina (obras sociales y receta) (18/11/2026) | Historia, odontograma, **periodontograma**, imágenes, RX con IA, presupuestos, planes, dictado por voz | Caja, cobros presenciales y online, liquidación a profesionales, reportes. Módulo Argentina con alta de obras sociales, recaudación y conciliación (títulos de artículos del centro de ayuda). ARCA: No evidenciado | Firma electrónica, API (complemento), WhatsApp. Mercado Pago y ARCA: No evidenciado |
| 3 | AgendaPro · https://agendapro.com/ar/dental/software-odontologico (funcionalidades); https://agendapro.com/ar/planes (API paga, facturación "próximamente") (18/11/2026) | Ficha, anamnesis, odontograma, imágenes adjuntas, presupuestos, consentimiento firmado. Periodontograma: No evidenciado | Caja, cobros, señas, Mercado Pago (links y cuotas), comisiones, reportes, inventario. Obras sociales: No evidenciado; facturación electrónica: "próximamente" | WhatsApp, Google Calendar, Google Maps, Instagram, Messenger, Meta y Google Ads, Mercado Pago, API (USD 200/mes) |
| 4 | DentalTec · https://web.dentaltec.com.ar/funcionalidades (18/11/2026) | Historia con registro temporal, imágenes, odontograma con CIE-10. Presupuestos y periodontograma: No evidenciado | **Validación en línea con +15 obras sociales** (afiliado, nomenclador, topes, autorizaciones); planillas con **ARCA**; cierre multinivel; refacturación de rechazos; liquidación a prestadores | WhatsApp ("integración oficial", home), ARCA, web services de obras sociales |
| 5 | Dentia · https://dentia.tech/ (funcionalidades y https://dentia.tech/#precios) (18/11/2026) | Ficha, historia configurable, odontograma, **periodontograma**, planes, presupuestos, consentimientos, laboratorio; IA de cefalometría y panorámicas | Caja con cierre, cobros, cuotas, **factura ARCA A/B/C**, señas, **Mercado Pago**, liquidación de obras sociales y prepagas, honorarios | WhatsApp Business (coexistencia), Instagram, Messenger, Google Calendar, Mercado Pago, ARCA, firma propia, importación Excel/CSV. API pública: No evidenciado |
| 6 | DentalSoft · https://dentalsoft.com.ar/ (secciones de funcionalidades y planes de la home) (18/11/2026) | Ficha, odontograma FDI de 18 estados con historial, presupuestos, planes con prioridades, ortodoncia | Caja y cierre diario, señas, Mercado Pago (Pro), obras sociales con cobertura, liquidación de obras sociales y comisiones, reportes. ARCA: No evidenciado | Google Calendar, WhatsApp, Mercado Pago, exportación a PDF y Excel. API: No evidenciado |
| 7 | Odonthia · https://odonthia.com/ (funcionalidades); https://odonthia.com/blog/mejores-software-odontologicos-argentina-2026 (lo que declara no hacer; tarifario por obra social) (18/11/2026) | Ficha, odontograma FDI (incluye dientes temporales), historia versionada, consentimientos firmados | Tarifario por obra social con copago (comparativa propia). **Declara no hacer** liquidación, factura ARCA ni receta | Importación CSV; firma electrónica |
| 8 | Odonto.ar · https://odonto.ar/ (18/11/2026) | Historia, odontograma con trazabilidad, radiografías, presupuestos | Cálculo de la parte de obra social y la del paciente; panel de finanzas. ARCA, caja y liquidación: No evidenciado | Importación desde Excel |
| 9 | DentalCore · https://dentalcore.app/ (18/11/2026, no accesible) | No evidenciado | No evidenciado (fuente secundaria: ARCA y liquidación) | No evidenciado |
| 10 | Odonapp · https://www.odonapp.com/ (18/11/2026) | Solo carga por pieza, cara y código de práctica | Obras sociales en una pantalla; circuito cargada → auditada → presentada → liquidada; cuenta corriente; ARCA; stock | ARCA |
| 11 | Doctocliq · https://doctocliq.com/ (funcionalidades); https://doctocliq.com/planes-y-precios (facturación como adicional y países) (18/11/2026) | Historia, odontograma (en todos los planes), presupuestos, planes, archivos | Caja, cobro multimoneda, comisiones, reportes; facturación electrónica como adicional, solo en PE, MX, EC y CO | WhatsApp, Meta, Google, Kommo, API de agenda |
| 12 | Clinic Cloud · https://clinic-cloud.com/ (funcionalidades); https://clinic-cloud.com/tarifas/ (odontograma en Max, pagos online y liquidaciones en Pro) (18/11/2026) | Historia, consentimientos; odontograma solo en el plan Max | Caja, facturación española, mutuas, presupuestos y liquidaciones (Pro), pagos online (Pro) | Doctoralia, Verifactu, TicketBAI |
| 13 | Dentidesk · https://dentidesk.com/ (18/11/2026) | Fichas de especialidad, odontograma con nomenclatura configurable | Facturación SII (Chile), Alegra (República Dominicana), +20 reportes, stock | SII, Alegra |
| 14 | Medesk · https://www.medesk.net/es/solutiones/odontologia (18/11/2026) | Odontograma, historial | Facturación electrónica, pagos, morosos, reportes | iCal, Google Calendar |
| 15 | Dentrix Ascend · https://www.dentrixascend.com/ (enlaza a /dental-solutions/charting-imaging-and-clinical-ai/ y /dental-solutions/dental-insurance-billing-and-collections/) (18/11/2026) | Charting, notas por voz, imágenes con IA, planes | Elegibilidad, claims, pagos, KPIs (seguros de EE. UU.) | API Exchange, agentes MCP |
| 16 | Curve Dental · https://www.curvedental.com/ (enlaza a /dental-charting-software, /perio-charting, /dental-image-software, /treatment-plan, /dental-billing-software, /partner-list) (18/11/2026) | Charting, perio, imágenes con IA, planes, formularios | Facturación a seguros, elegibilidad, pagos, analytics | Directorio de partners |
| 17 | Open Dental · https://www.opendental.com/ (enlaza a site/0_clearinghouses.html, site/0_reports.html, site/programbridges.html, site/conversions.html) (18/11/2026) | Odontograma 3D | Claims (+20 clearinghouses), pagos, reportes y consultas | Cientos de bridges; conversiones desde +200 sistemas |

### A.4 Operación, seguridad, fortalezas y limitaciones

Las columnas de fortalezas y limitaciones son *(juicio del analista)* sobre la evidencia de A.1 a A.3.

| # | Producto · fuente específica (consulta) | Operación | Seguridad y cumplimiento | Fortalezas evidentes | Limitaciones evidentes |
|---|---|---|---|---|---|
| 1 | Bilog · https://bilog.com.ar/ y https://bilog.com.ar/soluciones/consultorios (18/11/2026) | Sucursales; soporte. Roles, auditoría y exportación: No evidenciado | Solo Ley 25.506 (firma). Ley 25.326, Ley 26.529 y backup: No evidenciado | Trayectoria declarada de más de 20 años y base instalada en Argentina *(autodeclarado)*; circuito de obras sociales; multicanal | Sin precios públicos; seguridad no documentada; ARCA no evidenciado |
| 2 | Dentalink · https://www.softwaredentalink.com/ (secciones de seguridad y FAQ) (18/11/2026) | Multisucursal (Pro); soporte | **ISO 27001**, AWS cifrado, respaldos diarios, prácticas HIPAA | Cobertura clínica amplia (periodontograma, RX con IA, planes); certificación de seguridad publicada | Sin precios; adaptación argentina parcial (sin ARCA evidenciado) |
| 3 | AgendaPro · https://agendapro.com/ar/dental/software-odontologico (seguridad y soporte); https://agendapro.com/ar/planes (costos adicionales) (18/11/2026) | Multisede; soporte 24/7; migración gratuita. Roles y exportación: No evidenciado | AWS, cifrado, respaldos, **Ley 25.326 y Ley 26.529** declaradas | Mayor cantidad de canales de reserva documentados entre los sistemas relevados (link, sitio, Instagram, Messenger, Google Maps, WhatsApp) y marketing integrado; precios en ARS | Generalista; sin obras sociales ni ARCA; varios costos adicionales (WhatsApp, Recepcionista IA, API) |
| 4 | DentalTec · https://web.dentaltec.com.ar/funcionalidades (roles, auditoría, seguridad) y https://web.dentaltec.com.ar/ (soporte) (18/11/2026) | 10 roles, **auditoría completa**, exportación PDF/Excel, soporte 24/7 | JWT, bcrypt, Helmet (detalle técnico); leyes y backup: No evidenciado | Único sistema relevado que documenta validación en línea con obras sociales y circuito de círculos y federaciones | Débil en la experiencia del paciente (sin reserva online); sin precio |
| 5 | Dentia · https://dentia.tech/ (funcionalidades y https://dentia.tech/#faq) (18/11/2026) | Sucursales, 17 perfiles de rol, auditoría, **2FA**, exportación | Ley 25.326 declarada; Ley 26.529 y backup: No evidenciado | Es el sistema argentino relevado que documenta más subítems de la consigna; precio en ARS | Sin casos de clientes con nombre ni cifras de adopción verificables; la amplitud declarada debe validarse en una demo |
| 6 | DentalSoft · https://dentalsoft.com.ar/ (secciones de funcionalidades y FAQ de la home) (18/11/2026) | Multi-sucursal, permisos por rol, historial de cambios, exportación, capacitación | Mención genérica de copias de seguridad; leyes: No evidenciado | Único sistema relevado que documenta bloqueos de agenda junto con detección de solapamientos; web de reserva integrada; precios publicados y período gratuito de 3 meses | Sin ARCA; moneda de los precios no explicitada; muestra de reseñas muy chica; homónimos en otros países |
| 7 | Odonthia · https://odonthia.com/ y https://odonthia.com/blog/mejores-software-odontologicos-argentina-2026 (18/11/2026) | Registro de actividad, exportación | Respaldo; firma con hash, IP y dispositivo; leyes: No evidenciado | Gratuito y sin límite de pacientes; declara de forma explícita lo que no hace | Sin obras sociales ni ARCA; muchas funciones solo como ítems de menú |
| 8 | Odonto.ar · https://odonto.ar/ (18/11/2026) | Permisos por persona | No evidenciado (la pregunta frecuente de seguridad no muestra respuesta) | Planes simples, todas las funciones en todos los planes | Sin automatización evidenciada; precio en USD |
| 9 | DentalCore · https://dentalcore.app/ (18/11/2026, no accesible) | No evidenciado | No evidenciado | No evidenciado | Sitio caído en la fecha de consulta |
| 10 | Odonapp · https://www.odonapp.com/ (18/11/2026) | Auditoría de prestaciones, capacitación | No evidenciado | Circuito institucional de obras sociales | No es un sistema de turnos (fuera de segmento; potencial aliado) |
| 11 | Doctocliq · https://doctocliq.com/ (roles, exportación) y https://doctocliq.com/planes-y-precios (18/11/2026) | Roles, exportación al darse de baja | Permisos por persona; resto: No evidenciado | Plan gratuito y precios en USD publicados | Sin adaptación argentina; inconsistencias en la página de precios |
| 12 | Clinic Cloud · https://clinic-cloud.com/ (seguridad y soporte) y https://clinic-cloud.com/tarifas/ (18/11/2026) | Multisede; soporte humano los 7 días; migración gratuita | **RGPD certificado**, cifrado, trazabilidad | Modelo marketplace + software (Doctoralia) | Orientado a España; odontograma solo en el plan superior |
| 13 | Dentidesk · https://dentidesk.com/ (18/11/2026) | Multisucursal, administración de usuarios | Ley chilena mencionada | Fichas de especialidad | Sin WhatsApp; sin adaptación argentina |
| 14 | Medesk · https://www.medesk.net/es/solutiones/odontologia (18/11/2026) | Roles | RGPD, backups automáticos | Agenda con detección de huecos | Sin presencia argentina evidenciada |
| 15 | Dentrix Ascend · https://www.dentrixascend.com/ (enlaza a /support/ y /dental-solutions/dentrix-ascend-packages-and-suites/) (18/11/2026) | Multi-sede, roles, academia | **SOC 2**, HIPAA, backups cifrados | Referencia de integraciones (API Exchange) e IA | Orientado a seguros de EE. UU. |
| 16 | Curve Dental · https://www.curvedental.com/ (enlaza a /implementation, /training, /customer-service, /pricing) (18/11/2026) | Multi-sede, implementación y capacitación | Infraestructura HIPAA | Historia única del paciente; UX cloud | Sin precio; mercado de EE. UU. y Canadá |
| 17 | Open Dental · https://www.opendental.com/ (enlaza a site/webinars.html, site/documentation.html, site/fees.html) (18/11/2026) | Foros, webinars, documentación pública | No evidenciado | Profundidad funcional y ecosistema de integraciones | UX y mercado ajenos al contexto argentino |

---

## B. Matriz de puntuación ponderada (0 a 5)

| Sistema | Turnos y automatización (25 %) | Clínica odontológica (20 %) | Integraciones locales y WhatsApp (15 %) | Administración, cobros y facturación (15 %) | Experiencia del paciente (10 %) | Seguridad, exportación y trazabilidad (10 %) | Precio y adopción (5 %) | **Total ponderado** |
|---|---|---|---|---|---|---|---|---|
| Dentia | 4 | 5 | 5 | 5 | 4 | 4 | 5 | **4,55** |
| AgendaPro | 5 | 3 | 4 | 3 | 5 | 4 | 4 | **4,00** |
| Dentalink | 4 | 5 | 3 | 3 | 4 | 5 | 2 | **3,90** |
| DentalSoft | 5 | 3 | 3 | 4 | 4 | 3 | 4 | **3,80** |
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
- **"Integraciones locales y WhatsApp"** premia de forma explícita lo argentino: ARCA, Mercado Pago, obras sociales y WhatsApp. Por eso los productos internacionales (Dentrix Ascend, Curve Dental, Open Dental) reciben 1 aunque tengan ecosistemas de integración amplios.
- **"Precio y adopción"** premia los precios publicados con moneda explícita, el plan gratuito o la prueba sin tarjeta. Un precio a cotizar reduce la facilidad de adopción. **Ajuste en la revisión:** DentalSoft pasó de 5 a 4 porque publica montos pero no explicita la moneda (nota A.1-e). Su total pasó de 3,85 a 3,80; su posición en el ranking no cambia.
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
5. **Precios opacos**: los sistemas locales centrados en obras sociales (Bilog, DentalTec, Odonapp) no publican precios, lo que frena la adopción autónoma de consultorios chicos.
6. **Agenda por recurso físico** (sillón o box, equipamiento): casi no se documenta, aunque es determinante en clínicas.
7. **Interoperabilidad**: no hay APIs públicas documentadas en los productos argentinos. Solo AgendaPro (paga) y Dentalink (complemento) mencionan una API.

### C.4 Oportunidades de innovación

- **Producto puente**: una experiencia de turnos completa (reserva multicanal, WhatsApp, recordatorios) con el circuito argentino resuelto (obras sociales, copago, ARCA, Mercado Pago) en un solo flujo, desde la reserva hasta la liquidación.
- **Motor de agenda centrado en recursos**: profesional × sillón × duración por prestación, con prevención de solapamientos y sobreturnos con reglas.
- **Recuperación de huecos**: lista de espera automática que ofrece por WhatsApp el turno liberado por una cancelación.
- **Política de ausentismo configurable**: seña obligatoria para reincidentes, confirmación escalonada y reportes de ausentismo por profesional y por obra social.
- **Cumplimiento como diferencial de venta**: documentar públicamente cómo se aplican la Ley 25.326 y la Ley 26.529, con auditoría de accesos, exportación del paciente y backups verificables.
- **Precio transparente en ARS** con plan de entrada para el odontólogo independiente.
- **Alianzas con círculos odontológicos**: integrarse con Odonapp o DentalTec en lugar de competir en su terreno institucional.

---

## D. Recomendación final

### D.1 Cinco competidores prioritarios para analizar mediante demo

1. **Dentia**: tiene el puntaje más alto de la matriz B (cobertura documentada). *(Juicio del analista:)* es el más cercano a la propuesta "puente". Hay que validar en la demo si su amplitud es real y qué tan robusto es el asistente de WhatsApp.
2. **Bilog**: es el sistema local con la mayor base de clientes declarada *(autodeclarado)*. Hay que entender su circuito de obras sociales, su precio real y por qué retiene clientes.
3. **DentalTec**: es el único que documenta validación en línea con obras sociales y el circuito de círculos. *(Juicio del analista:)* define el estándar administrativo a igualar o integrar.
4. **AgendaPro**: es el que documenta más canales de reserva, junto con automatización y marketing, con precios en ARS. *(Juicio del analista:)* es el competidor más probable para un consultorio que prioriza la captación de pacientes.
5. **Dentalink**: documenta cobertura clínica amplia y certificación ISO 27001. Hay que validar la profundidad real de su módulo para Argentina.

### D.2 Tres productos de referencia para la experiencia de usuario

*(Juicio del analista.)*

1. **AgendaPro**: flujo de reserva del paciente, multicanal, recordatorios con reenvío.
2. **Curve Dental**: historia única del paciente que integra agenda, clínica y cobro en una sola vista cloud.
3. **Clinic Cloud / Doctoralia**: modelo de marketplace más software, con confirmaciones multicanal.

*(Dentrix Ascend queda como referencia secundaria de arquitectura de integraciones y API.)*

### D.3 MVP sugerido

#### D.3.1 MVP ajustado al proyecto (vigente)

Este es el MVP que adopta el roadmap. Surge de la entrevista de Discovery del 18/11/2026 ([`discovery.md`](discovery.md)).

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

## Referencias

Todas las URL se consultaron el 18/11/2026.

**Fuentes oficiales, por proveedor**

- **Bilog**: https://bilog.com.ar/ · https://bilog.com.ar/soluciones/consultorios
- **Dentalink**: https://www.softwaredentalink.com/ · https://ayuda.softwaredentalink.com/es/collections/19196578-modulo-exclusivo-para-argentina
- **AgendaPro**: https://agendapro.com/ar/dental/software-odontologico · https://agendapro.com/ar/planes
- **DentalTec**: https://web.dentaltec.com.ar/ · https://web.dentaltec.com.ar/funcionalidades
- **Dentia**: https://dentia.tech/ · https://dentia.tech/#precios · https://dentia.tech/#faq
- **DentalSoft**: https://dentalsoft.com.ar/
- **Odonthia**: https://odonthia.com/
- **Odonto.ar**: https://odonto.ar/
- **DentalCore**: https://dentalcore.app/ (no accesible)
- **Odonapp**: https://www.odonapp.com/
- **Doctocliq**: https://doctocliq.com/ · https://doctocliq.com/planes-y-precios
- **Clinic Cloud**: https://clinic-cloud.com/ · https://clinic-cloud.com/tarifas/
- **Dentidesk**: https://dentidesk.com/
- **Medesk**: https://www.medesk.net/es/solutiones/odontologia
- **Dentrix Ascend**: https://www.dentrixascend.com/ (con enlaces relevados a /dental-solutions/charting-imaging-and-clinical-ai/, /dental-solutions/dental-insurance-billing-and-collections/, /dental-solutions/marketing-and-patient-experience/, /dental-solutions/dentrix-ascend-packages-and-suites/ y /support/)
- **Curve Dental**: https://www.curvedental.com/ (con enlaces relevados a /dental-scheduling-software, /dental-patient-engagement-software, /dental-charting-software, /perio-charting, /dental-image-software, /treatment-plan, /dental-billing-software, /partner-list, /implementation, /training, /customer-service y /pricing)
- **Open Dental**: https://www.opendental.com/ (con enlaces relevados a site/websched.html, site/patientportal.html, site/textintegrated.html, site/ereminders.html, site/0_clearinghouses.html, site/0_reports.html, site/programbridges.html, site/conversions.html, site/webinars.html, site/documentation.html y site/fees.html)

Para Dentrix Ascend, Curve Dental y Open Dental, los datos se extrajeron de la home, que enlaza a esas páginas internas; las páginas internas no se consultaron de forma individual.

**Fuentes secundarias (no puntúan)**

- https://odonthia.com/blog/mejores-software-odontologicos-argentina-2026 (comparativa de un competidor; datos relevados por Odonthia el 09/10/2026)
- https://www.capterra.es/software/196361/dentalink
- https://www.capterra.es/software/184029/dentidesk

**No accesibles en la fecha de consulta**

- https://dentalcore.app/
- https://www.doctoralia.com.ar/
- https://www.infomed.es/ (Gesden)

Por eso Doctoralia y Gesden quedaron fuera de la tabla.

---

## Verificación de fuentes

