# 4. Verticales: salud, robótica, fábricas y otros

Convención: **[V]** dato verificado en una fuente (enlace al lado). **[I]** inferencia o estimación propia, sin fuente directa. Los datos vienen de resúmenes de búsqueda, muchos de reportes de mercado y blogs de proveedores. Sirven para órdenes de magnitud, no para citar sin revisar la fuente primaria.

## 4.1 La lógica para comparar verticales

Un proveedor nuevo y pequeño, ubicado fuera de EE.UU., gana donde se cumplen cuatro condiciones:

1. **Barrera regulatoria baja a nivel de la tarjeta.** La certificación la carga el dueño del producto, no quien diseña la board.
2. **Urgencia alta.** El cliente pierde más por esperar que por pagar.
3. **Volumen bajo y mucha variedad.** Las fábricas grandes no quieren ese trabajo.
4. **Tolerancia a proveedores remotos.** El cliente ya trabaja con contratistas.

Cada vertical se evalúa contra esas cuatro condiciones.

## 4.2 Robótica y "physical AI"

**Qué tarjetas necesitan [I]:** controladores de motor por articulación (FOC/BLDC con encoder), nodos EtherCAT o CAN-FD, BMS para baterías de 48 a 72 V, distribución de potencia y parada de emergencia, tarjetas de sensores (IMU, fuerza, tacto), agregadores de cámaras, *carrier boards* para NVIDIA Jetson, hardware de teleoperación.

**Por qué importa el volumen de tarjetas:**
- Un humanoide tiene entre 28 y 44 actuadores. Los actuadores son 40 a 60% del costo de materiales. El BOM estimado de un Optimus Gen 2 es cerca de $55k [V] ([McKinsey](https://www.mckinsey.com/industries/industrials/our-insights/turning-humanoid-supply-chain-constraints-into-billion-dollar-wins), [XenoSpectrum](https://xenospectrum.com/en/humanoid-robot-bom-actuator-cost/)).
- Eso implica unas 30 a 40 tarjetas de control de motor por robot [I].

**Demanda:**
- Startups de humanoides levantaron $6.1B en 139 rondas en 2025, contra $1.5B en 65 rondas en 2024. Robótica más physical AI: $27.6B en 1,009 rondas en 2025 [V] ([PitchBook](https://pitchbook.com/news/articles/apptronik-raises-520m-as-vc-funding-for-humanoid-robotics-explodes-300)).
- En el primer semestre de 2026, physical AI (definición amplia) levantó $47.4B en 521 rondas. Solo robótica llevaba $18.8B a mitad de 2026, más que todo 2025 [V] ([Crunchbase](https://news.crunchbase.com/venture/physical-ai-funding-startups-robotics-aerospace-h1-2026/)).
- Hay más de 100 empresas construyendo humanoides de tamaño completo, cerca de la mitad en China [V] ([Digitimes](https://www.digitimes.com/news/a20250827PD212.html)).
- Cuello de botella reportado: componentes de grado robótico con tiempos de entrega de 26 a 52 semanas, y tiempos de PCB descritos como "frustrantes" [V] ([Foundamental](https://www.foundamental.com/perspectives/field-guide-manufacturing-for-early-stage-robotics)).

**Qué se subcontrata:**
- Las empresas grandes de humanoides diseñan actuadores y drivers adentro y escalan con EMS grandes. Ejemplo: Jabil es el socio de manufactura de Apptronik desde febrero de 2025 [V] ([The Robot Report](https://www.therobotreport.com/apptronik-collaborates-with-jabil-to-produce-apollo-humanoid-robots/)).
- Las startups pequeñas y las no humanoides (AMR, construcción, agro) sí subcontratan tarjetas. Ejemplo: Softeq diseñó las tarjetas de Rugged Robotics [V] ([Softeq](https://softeq.com/featured_projects/hardware-for-commercial-construction-robot-rovers)).
- NVIDIA ya tiene una red de más de 150 socios que hacen *carrier boards* para Jetson (Advantech, ConnectTech, Seeed y otros) [V] ([NVIDIA](https://nvidianews.nvidia.com/news/nvidia-blackwell-powered-jetson-thor-now-available-accelerating-the-age-of-general-robotics)). Ese nicho tiene competencia establecida.

**Requisitos:** las normas de seguridad (ISO 10218, ISO 13482, UL 3300) son a nivel de sistema y las carga el fabricante del robot [V] ([ANSI](https://blog.ansi.org/iso-10218-1-2025-robots-and-robotic-devices-safety/)). Al proveedor de tarjetas le piden calidad de ensamble IPC clase 2 o 3 e ISO 9001 [I]. Nada bloquea a un proveedor extranjero, salvo que el robot sea para defensa.

**Ventas [I]:** ciclos de semanas a 3 meses. Primer contrato de $15k a $80k por una familia de tarjetas. Fidelidad media: las startups rediseñan seguido, pero quien es dueño de varias tarjetas se vuelve difícil de reemplazar.

**Veredicto:** el vertical más accesible con alto crecimiento. Cumple las cuatro condiciones. El riesgo es que es un ciclo de capital de riesgo: si la financiación se enfría, la demanda cae.

## 4.3 Salud y dispositivos médicos

**Qué tarjetas necesitan [I]:** wearables con sensores (BLE, IMU, PPG, ECG), front-ends de monitoreo de pacientes, fuentes y datos aislados (exigencia de la norma 60601), gateways de monitoreo remoto, control de bombas y motores.

**Tamaño del mercado subcontratado:**
- Outsourcing de dispositivos médicos: entre $132B y $158B en 2025 según la fuente. Diseño y desarrollo es el segmento más grande [V] ([Fortune BI](https://www.fortunebusinessinsights.com/medical-device-outsourcing-market-115379), [IMARC](https://www.imarcgroup.com/medical-device-outsourcing-market)).
- Manufactura por contrato: $79.3B en 2025, proyección $135.5B en 2031 [V] ([MarketsandMarkets](https://www.marketsandmarkets.com/Market-Reports/geography/medical-device-contract-manufacturing-market/North-America)).
- Las startups de monitoreo remoto y cuidado portátil levantaron $1.2B solo en el segundo trimestre de 2025 [V] ([PitchBook](https://pitchbook.brightspotcdn.com/2f/23/79e5bd5759e443ef7e0eef55be30/q2-2025-medtech-vc-and-pe-trends-preview.pdf)).

**Requisitos (aquí está la barrera):**
- La nueva regulación de calidad de la FDA (QMSR) rige desde febrero de 2026 e incorpora ISO 13485 [V] ([FDA](https://www.fda.gov/quality-systems-regulation)).
- ISO 13485 para una firma de hasta 50 personas: $15k a $35k y de 3 a 12 meses [V, fuentes de consultores] ([Greenlight Guru](https://www.greenlight.guru/blog/iso-13485-certification-timeline), [OpenRegulatory](https://openregulatory.com/iso-13485-certification-cost)).
- Pruebas IEC 60601: 6 a 12 semanas [V] ([Simplexity](https://www.simplexitypd.com/iec-60601-testing-overview-for-medical-device-development/)).
- Dispositivos conectados: plan de ciberseguridad y lista de software (SBOM) obligatorios [V] ([Federal Register](https://www.govinfo.gov/content/pkg/FR-2025-06-27/html/2025-11669.htm)).
- Ninguna de estas normas discrimina por nacionalidad [I]. El dueño del dispositivo carga el registro ante la FDA. Un subcontratista de diseño necesita procesos compatibles con ISO 13485.

**Ventas:**
- Calificar a un proveedor nuevo toma de 6 a 18 meses. Cambiar de proveedor es un evento regulatorio [V, blog de proveedor] ([VentureOutsource](https://ventureoutsource.com/contract-manufacturing/fda-requalification-tariff-lock-in/)).
- Consecuencia [I]: ciclo de venta de 6 a 12 meses o más, primer contrato de $30k a $150k, y relación muy estable una vez adentro. Es lento para entrar y lento para salir.

**Colombia:**
- En 2025 Colombia importó $1,374M en dispositivos médicos y exportó $81.2M. Mercado local de $1,773M en 2025, proyectado a $2,217M en 2030 [V] ([ProColombia vía Diario del Sur](https://www.diariodelsur.com.co/noticias/dispositivos-medicos-colombia-tiene-mercado-y-espacio-para-nueva-inversion-extranjera)).
- La dependencia de importaciones es casi total. Hay espacio para sustitución, pero el comprador (clínicas, EPS) compra marcas establecidas.

**Veredicto:** buen negocio de largo plazo, mala puerta de entrada. Accesible primero en dispositivos de bajo riesgo (clase I y II, bienestar, instrumentos de laboratorio, accesorios de monitoreo). Cerrado al inicio: clase III y proveeduría de producción a grandes fabricantes.

## 4.4 Fábricas, automatización e IoT industrial

**Qué tarjetas necesitan [I]:** gateways (de Modbus/RS-485 a la nube por celular o Wi-Fi), módulos de entradas y salidas (4-20 mA, 24 V), controladores tipo PLC, sensores de vibración y temperatura para modernizar máquinas viejas, tarjetas de HMI, control de variadores.

**Demanda:**
- Más del 60% de la maquinaria en Europa y Norteamérica tiene más de 15 años. Por eso se moderniza (*retrofit*) en vez de reemplazar [V, blog citando a McKinsey] ([InTechHouse](https://intechhouse.com/blog/brownfield-iot-retrofitting-legacy-industrial-machinery-for-predictive-maintenance)).
- IoT industrial global: $129.4B en 2025 [V] ([Fortune BI](https://www.fortunebusinessinsights.com/industrial-iot-market-119716)).
- Automatización industrial en América Latina: $16.8B a $19.7B en 2025, creciendo cerca de 7.4% anual [V] ([Mordor](https://www.mordorintelligence.com/industry-reports/latin-america-factory-automation-and-industrial-controls-market)).
- En Colombia la adopción de Industria 4.0 en pymes es baja. Las razones citadas son infraestructura débil y costo de inversión [V] ([encuesta a 121 pymes](https://doaj.org/article/54e22dce564b423ab23454fceddbfffe)).

**Quién subcontrata [I]:** Siemens, Rockwell, ABB y Schneider diseñan adentro. El trabajo subcontratado viene de startups de IoT industrial, fabricantes de maquinaria e integradores que necesitan algo a la medida.

**Requisitos [I]:** CE, UL/IEC 61010, IEC 61131-2 para PLC, y ATEX/IECEx para minería y petróleo. La certificación de seguridad funcional (IEC 61508) solo aplica si el contrato la exige [V] ([exida](https://www.exida.com/Blog/back-to-basics-12-what-is-iec-61508-certification)). Nada bloquea a un proveedor extranjero.

**Ventas [I]:** en Colombia, ciclos de 3 a 9 meses a través de integradores. Primeros contratos como pilotos de $10k a $50k. Fidelidad alta: los equipos duran más de 10 años, así que hay recompra y repuestos.

**Veredicto:** el mejor vertical para demanda nacional y andina. Menos glamoroso y más lento que robótica, pero más estable y con ventaja de cercanía (visitas a planta, soporte en español, entender la máquina real).

## 4.5 Otros verticales

| Vertical | Demanda | Barrera | Atractivo |
|---|---|---|---|
| Energía y medición inteligente | Colombia planea unos 11M de hogares con medición avanzada a 2030, con cerca de 1% desplegado [V] ([BNamericas](https://www.bnamericas.com/en/news/colombia-unveils-plans-for-11mn-smart-meters)). Solar en 4.58 GW a julio de 2026 [V] ([pv magazine](https://www.pv-magazine.com/2026/07/21/colombias-pv-capacity-tops-4-58-gw-with-1-19-gw-under-testing/)) | Certificación metrológica y fabricantes establecidos de medidores | Medio-alto para monitoreo y comunicaciones. Bajo para el medidor en sí |
| Telemática y flotas | Unos 10M de vehículos comerciales conectados en LatAm a fin de 2025. Geotab creció 34% en Colombia en dos años [V] ([Geotab](https://www.geotab.com/es-latam/blog/gestion-flotas-exito-latam-eng/)) | Rastreadores chinos baratos | Medio, solo en nichos (cadena de frío, maquinaria minera y agrícola) |
| Drones y defensa, EE.UU. | La ley prohíbe componentes chinos en drones del Pentágono y la FCC restringió drones extranjeros en diciembre de 2025 [V] ([Simpson Thacher](https://www.stblaw.com/the-federal-communications-commission-bans-foreign-made-drones-and-drone-components-with-exceptions-for-those-on-the-blue-uas-list-and-qualifying-domestic-end-products/)) | ITAR: compartir datos controlados con un colombiano cuenta como exportación [V] ([guía de deemed exports](https://www.stonybrook.edu/research-security/export-controls/reference_guides/deemed-exports.html)) | Bajo. Prácticamente cerrado |
| Drones y defensa, Colombia | CIAC lanzó en 2025 el primer dron militar nacional. Producción cercana a 8 unidades al mes. Programa antidrones de más de $1.6B [V] ([Rio Times](https://www.riotimesonline.com/colombia-puts-drone-manufacturing-at-the-center-of-its-military-industry/), [AFP vía Teletica](https://www.teletica.com/internacional/colombia-entra-en-la-guerra-de-drones-contra-las-guerrillas_409694)) | Contratación estatal | Alto como proveedor local |
| Agro | 163 startups agrifoodtech en Colombia según ANDI, con baja adopción [V] ([AgFunder](https://agfundernews.com/can-colombia-fulfill-the-promise-of-becoming-an-agrifoodtech-powerhouse)) | Comprador sensible al precio | Medio. Se vende mejor a través de gremios y exportadores |
| Consumo masivo | Grande | Compite de frente con Shenzhen | Bajo |

## 4.6 Ranking de accesibilidad para una firma nueva desde Colombia [I]

1. **Startups de robótica y physical AI en EE.UU.**: drivers de motor, BMS, sensores, hardware de prueba. Rápido, urgente, sin barrera regulatoria.
2. **IoT industrial y modernización de máquinas** en Colombia, región andina y fabricantes de maquinaria en EE.UU. Estable, con ventaja local.
3. **Salud de bajo riesgo e instrumentos de laboratorio.** Requiere ISO 13485 dentro del primer año.
4. **Defensa colombiana y monitoreo de energía.** Depende de relaciones y contratación pública.

**Cerrado en la práctica:** defensa de EE.UU., dispositivos médicos clase III, controladores de seguridad certificados, consumo de alto volumen.

**Vacíos de evidencia:** no se encontró ningún caso documentado de una startup de EE.UU. subcontratando diseño de tarjetas a una firma colombiana o latinoamericana. Los tamaños de contrato y ciclos de venta de este capítulo son inferencias, no datos. Validarlos requiere hablar con clientes.
