# 2. Cómo funciona la industria hoy y sus economics

Convención: **[V]** dato verificado en una fuente. **[I]** inferencia o regla general. Varias cifras [V] vienen de blogs de proveedores, sirven como orden de magnitud.

## 2.1 El principio que explica todo: el margen sigue al conocimiento, no al volumen

| Capa | Ejemplo | Ingresos | Margen bruto | Margen operativo |
|---|---|---|---|---|
| Distribuidor de componentes | Arrow FY2024 | $27.9B | 11.8% | ~2.8% |
| Distribuidor | Avnet FY2025 | $22.2B | 10.7% | 2.3% |
| EMS gigante | Jabil FY2025 | $29.8B | ~8.9% | 5.4% (core) |
| EMS gigante | Flex FY2025 | $25.8B | n/d | 5.7% (ajustado) |
| EMS de alta mezcla | Plexus FY2025 | $4.03B | 10.1% | 5.0% |
| EMS mediano | Kimball Electronics FY2025 | $1.49B | n/d | 3.1% |
| EMS con diseño (India) | Kaynes FY25 | ~$320M | n/d | EBITDA 15.1% |
| EMS sin diseño (India) | Syrma SGS FY25 | ~$450M | n/d | EBITDA 8.6% |
| Solo diseño | Tata Elxsi FY25 | ~$440M | n/d | EBITDA 26.1% |
| Plataforma online PCB+ensamble | JLC (JLCPCB) 2024 | ~$1.1B | 28.8% | neto ~13% |

Todo [V]. Fuentes: [Arrow](https://www.businesswire.com/news/home/20250206456512/en), [Avnet 10-K](https://www.sec.gov/Archives/edgar/data/8858/000000885825000028/avt-20250628x10k.htm), [Jabil](https://www.sec.gov/Archives/edgar/data/898293/000162828025042693/jbl-20250925ex991.htm), [Flex](https://investors.flex.com/news/news-details/2025/FLEX-REPORTS-FOURTH-QUARTER-AND-FISCAL-2025-RESULTS/default.aspx), [Plexus](https://investor.plexus.com/news/news-details/2025/Plexus-Announces-Fiscal-Fourth-Quarter-and-Fiscal-Year-2025-Financial-Results/default.aspx), [Kimball](https://www.businesswire.com/news/home/20250813325066/en), [Kaynes](https://www.businesstoday.in/markets/stocks/story/kaynes-technology-shares-jump-9-on-strong-q4-fy25-numbers-476509-2025-05-16), [Syrma](https://quartr.com/events/syrma-sgs-technology-limited-syrma-q4-24-25_F419qUIp), [Tata Elxsi](https://www.tataelxsi.com/news-and-events/tata-elxsi-operating-revenue-at-rs-3-729-crores-for-fy-25-with-full-year-pbt-at-26-3), [JLC](https://finance.eastmoney.com/a/202605133735813762.html). Conversiones a USD aproximadas.

**Por qué fabricar deja tan poco:** el fabricante factura el costo de los componentes, que son 50 a 80% de la cotización [V] ([Atlas PCB](https://atlaspcb.com/blog/pcba-assembly-cost-breakdown-bom-nre-testing-2026)). Es dinero que entra y sale. Sobre lo que realmente agrega (mano de obra, proceso) gana bien, pero sobre el ingreso total queda 4 a 6%.

**Tres lecturas de la tabla:**
1. Diseñar deja 4 a 5 veces el margen de ensamblar.
2. Un EMS que también diseña (Kaynes) casi duplica el margen de uno que solo ensambla (Syrma).
3. La automatización con software (JLC) triplica el margen bruto de un EMS tradicional. El software aplicado a manufactura de bajo volumen es donde aparece margen nuevo.

## 2.2 Tamaños de mercado

- EMS global: ~$650B en 2025 [V] ([MarketsandMarkets](https://www.marketsandmarkets.com/Market-Reports/electronics-manufacturing-services-market-123721672.html)).
- PCB sin ensamblar: $85.8B en 2025, +16.7% por servidores de IA [V] ([Prismark vía TechNews](https://technews.tw/2026/06/12/pcb-prismark-report-2025/)).
- Servicios de diseño de PCB: $3.9B a $6.2B según quién lo mida [V] ([QYResearch](https://www.qyresearch.com/reports/6304250/pcb-design-services)). Cifra poco confiable.
- Ingeniería subcontratada (ER&D): de ~$280B hoy a ~$775B en 2030 según BCG [V] ([BCG](https://web-assets.bcg.com/1a/d9/287070844d84bd58e61e192eca78/seizing-the-er-d-advantage-frontiers-for-2030.pdf)).

El mercado es enorme en todas las capas. El tamaño no es la restricción. La restricción es qué capa puede ocupar un jugador nuevo.

## 2.3 Cómo se cotiza una tarjeta

Fórmula: **precio = materiales + mano de obra + preparación (NRE) + pruebas + margen** [V] ([VentureOutsource](https://ventureoutsource.com/contract-manufacturing/profit-margins-pcb-electronic-assembly-quotes-ems-manufacturing-costs-oem-pricing/)).

- Sobreprecio en componentes: 10 a 30% [V] ([Altium](https://resources.altium.com/p/buying-parts)).
- Costo por componente colocado: ~$0.185 en EE.UU. contra ~$0.048 en China [V] ([Altium](https://resources.altium.com/p/pcb-pcba-cost-comparison-us-versus-china)).
- Mano de obra por hora: México ~$6.5, China ~$7.9, EE.UU. ~$32 [V] ([American Industries](https://hub.americanindustriesgroup.com/insights/us-companies-know-nearshoring-manufacturing-mexico/)). México ya es más barato que China en mano de obra.

**Ejemplo ilustrativo [I]:** tarjeta de 4 capas, ~200 componentes, microcontrolador con radio, fabricada en China.

| Cantidad | Costo por unidad | Qué domina el costo |
|---|---|---|
| 10 | $80 a $150 | Preparación y componentes comprados al detal |
| 100 | $35 a $60 | Mezcla |
| 1,000 | $20 a $35 | Componentes |
| 10,000 | $14 a $25 | Casi solo componentes |

En EE.UU. es 1.3 a 2 veces más caro en volúmenes bajos y medios [I].

**La conclusión importante:** a 10 unidades el costo por tarjeta es irrelevante frente al costo de esperar. A 10,000 unidades cada centavo cuenta. Son dos negocios distintos con clientes distintos. El primero compra velocidad, el segundo compra costo.

**Precio del diseño:**
- Solo layout: $2k a $9.5k. Diseño completo de PCB: desde $10k [V] ([CadCrowd](https://www.cadcrowd.com/blog/how-much-does-it-cost-to-outsource-pcb-design-services-electronics-engineering-complete-prices-for-companies/)).
- Proyecto completo (esquemático, layout, firmware, bring-up) en firma occidental: $25k a $150k [I].
- Regla de la industria: planear al menos 3 vueltas de prototipo y 50% de sobrecosto [V] (Predictable Designs / Altium).

**Tarifas por hora de ingeniería de hardware/embebidos [V]** ([Developex](https://developex.com/blog/embedded-software-developer-rates-2026), [CadCrowd](https://www.cadcrowd.com/blog/how-much-does-it-cost-to-outsource-pcb-design-services-electronics-engineering-complete-prices-for-companies/)):

| Región | Tarifa |
|---|---|
| Firmas en EE.UU. | $100 a $200+ |
| Europa occidental | $80 a $120 |
| Europa del Este | $45 a $75 |
| América Latina | $40 a $65 |
| Asia-Pacífico | $30 a $55 |

## 2.4 Lo que ya se volvió commodity: el prototipo barato

JLCPCB (China) es el caso de estudio [V] ([Eastmoney](https://finance.eastmoney.com/a/202605133735813762.html)):
- Ingresos 2025: ~RMB 10.2B (~$1.4B), +28.6%.
- Más de 9.5M de pedidos en un semestre.
- Cinco tarjetas de 4 capas por $2 en promoción.
- Integra fabricación, ensamble y su propia tienda de componentes (LCSC), con cotización instantánea.

Consecuencia: fabricar un prototipo simple ya no vale nada. Nadie puede competir con eso en precio. Solo se compite en velocidad hacia un mercado específico, en complejidad, o en confianza (propiedad intelectual, defensa, regulación).

**El contraejemplo, Tempo Automation:** fábrica "definida por software" en San Francisco para prototipos rápidos. Salió a bolsa y quebró en diciembre de 2023 [V] ([Wikipedia](https://en.wikipedia.org/wiki/Tempo_Automation)). Lección: una fábrica premium de prototipos en una ciudad cara no cubre sus costos fijos solo con ensamble. Diode intenta resolverlo sumando el diseño (capítulo 3).

## 2.5 Capital y operación de una fábrica

**La máquina no es la barrera [V]** ([SMT Machine Line](https://smtmachineline.com/smt-line-cost-breakdown-factors-pricing-guide/)):

| Tipo de línea SMT | Costo |
|---|---|
| Línea china económica completa | $50k a $100k |
| Línea usada completa | ~$33k |
| Línea mediana | $150k a $500k |
| Línea nueva de marca, alto volumen | $500k a $2M |

**Las barreras reales:**

1. **Capital de trabajo.** Compras componentes hoy, cobras en 60 a 90 días. Jabil, por escala, opera con un ciclo de caja de 18 días. Plexus, de alta mezcla, con ~155 días [V] ([Jabil 10-K](https://www.sec.gov/Archives/edgar/data/898293/000162828025045293/jbl-20250831.htm), [GuruFocus](https://www.gurufocus.com/term/cash-conversion-cycle/PLXS)). En alta mezcla el inventario te come la caja.
2. **Utilización.** Las líneas de alta mezcla suelen operar por debajo de 30% de eficiencia porque pasan el tiempo cambiando de producto [V, dato de proveedor].
3. **Riesgo de inventario.** Castigar 0.2 a 0.5% adicional de inventario obsoleto le costó $3M de utilidad bruta a una firma [V] ([Evertiq](https://evertiq.com/news/2026-10-01-ems-under-the-hood-capital-efficiency-and-overall-winners)).
4. **Escasez de componentes.** En 2026 las memorias tienen plazos de 25 a 45 semanas y se asignan a clientes con historial [V] ([Avnet](https://www.avnet.com/americas/resources/article/memory-is-breaking-product-plans/)). Un comprador nuevo y pequeño queda al final de la fila.

## 2.6 Certificaciones: el peaje de cada mercado

| Certificación | Para qué | Costo | Tiempo |
|---|---|---|---|
| FCC con módulo de radio precertificado | Vender en EE.UU. | ~$1.9k | Semanas |
| FCC con radio propio | Vender en EE.UU. | ~$15k con Canadá | 1 a 2 meses |
| UL | Seguridad eléctrica | $3k a $15k, más de $50k si es complejo | 6 a 25 semanas |
| ISO 13485 | Proveer a dispositivos médicos | $15k a $80k | 3 a 12 meses |
| AS9100 | Aeroespacial | $10k a $50k | 3 a 12 meses |
| IATF 16949 | Automotriz | $20k a $50k | 8 a 18 meses |

[V] ([MarkReady](https://markready.pages.dev/guides/fcc-certification-cost), [OpenRegulatory](https://openregulatory.com/iso-13485-certification-cost)). Son costos manejables. No son la barrera. La barrera es el historial que el cliente exige además del certificado.

## 2.7 Ciclos de venta y por qué el negocio es pegajoso

- **Manufactura:** programas grandes de EMS tardan 18 a 26 meses en cerrarse [V] ([VentureOutsource](https://ventureoutsource.com/contract-manufacturing/ems-manufacturing-industry-faces-eroding-differentiation-rising-customer-acquisition-costs)).
- **Diseño:** semanas a 3 meses para startups y pymes [I].
- **Por qué nadie cambia de fabricante:** en dispositivos médicos, recalificar un cambio cuesta $150k a $400k y hasta 12 meses [V] ([VentureOutsource](https://ventureoutsource.com/contract-manufacturing/fda-requalification-tariff-lock-in/)). En general se pierde conocimiento de proceso y cae el rendimiento en la fábrica nueva.

**Contratos típicos [V]** ([MDDI](https://www.mddionline.com/contract-manufacturing/fixed-fee-vs-time-and-materials-which-outsourcing-pricing-structure-is-right-for-you-)): por horas (T&M), precio fijo, o híbrido. La propiedad intelectual es el punto más negociado. Lo normal: el cliente es dueño de lo que pagó y la firma conserva su IP previa y sus bloques reutilizables.

## 2.8 Síntesis

1. **El diseño es la puerta.** Se vende rápido, requiere poco capital, deja margen alto y decide quién fabrica.
2. **La manufactura es el foso.** Se vende lento, requiere caja, deja margen bajo, pero una vez adentro el cliente no se va.
3. **La mejor posición combina ambas:** entrar por diseño y quedarse con la producción de bajo volumen. Es lo que hacen Kaynes, VVDN, Titoma y Diode.
