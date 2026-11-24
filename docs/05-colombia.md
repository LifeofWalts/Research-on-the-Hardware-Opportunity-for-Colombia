# 5. Colombia: qué hay, qué falta, qué cuesta

Convención: **[V]** verificado en fuente. **[I]** inferencia o estimación. Varios temas quedaron sin investigar por límite de búsquedas. Están listados al final.

## 5.1 El ecosistema actual: pequeño y frágil

**Manufactura por contrato**
- **Colcircuitos (Medellín)**, parte del grupo Invertrónica junto con Tecrea (diseño) y LosComponentes (distribución). Descrita como el EMS más grande de Colombia. Ensamble automatizado, fabricación de PCB, miembro de IPC [V] ([Circuits Assembly](https://circuitsassembly.com/ca/editorial/menu-features/36644-nearshoring-ems-from-latin-america.html), [Colcircuitos](https://colcircuitos.com/about/)).
  - Exportaciones registradas en aduana: ~$42k contra ~$2.8M de importaciones [V] ([Veritrade](https://www.veritradecorp.com/en/colombia/imports-y-exports-colcircuitos-sas/nit-900381799)).
  - **Alerta:** un perfil de septiembre de 2024 la lista "en Proceso de Negociación de Emergencia", un trámite de reorganización por insolvencia [V] ([EMIS](https://www.emis.cn/php/company-profile/CO/Colcircuitos_SAS_en_Proceso_de_Negociacion_de_Emergencia_en_3710267.html)). Estado actual sin confirmar.
- **Microcircuitos (Cali):** existe en directorios, sin datos de capacidad [V].
- Ensambladores pequeños como Aldelta (Girardot, 4 empleados) [V].

**Diseño para exportación: el caso que sí existe**
- **Titoma** tiene en Manizales su centro de ingeniería: ~55 personas. Fundada por un holandés en Taiwán, diseña en Colombia y fabrica en Taiwán y China. Cada año toma los 10 mejores graduados de una universidad colombiana y los entrena 6 meses en Taiwán [V] ([Titoma](https://titoma.com/blog/titoma-ceo-transition/), [Altium](https://altium.com/company/customer-success/connecting-dots-titoma-and-altium)).
- Es la prueba más importante de este research: **ingenieros colombianos ya diseñan hardware para clientes internacionales**. El modelo que funcionó separa el diseño (Colombia) de la manufactura (Asia).

**Empresas de producto**
- **Kiwibot:** robots diseñados en Medellín con oficinas en EE.UU. y Taipéi [V, datos de 2020 y 2021].
- **CIAC:** dron militar DRAGOM, lanzado en 2025 [V].
- **Haceb:** ensambla ~1.5M de electrodomésticos al año. Sin evidencia de que diseñe sus tarjetas [V].

**Escala nacional**
- Colombia exportó $374k en tarjetas de circuito impreso en 2022 e importó $6.98M, casi todo de China [V] ([OEC](https://oec.world/profile/bilateral-product/printed-circuit-boards/reporter/col)).
- No encontré ninguna firma colombiana exportando diseño o manufactura electrónica a escala.

**Lectura [I]:** el terreno está vacío. Eso es una oportunidad (no hay competencia local) y una advertencia (no hay proveedores, ni distribuidores con inventario, ni laboratorios, ni clientes educados). Quien entre construye su propia cadena.

## 5.2 Talento

- **Oferta:** 2,591 ingenieros electrónicos graduados en 2018. Cerca de 42,000 entre 2001 y 2017. Unos 80 programas activos [V, SNIES vía [tesis USTA](https://repository.usta.edu.co/bitstreams/ffe943bf-88c4-4af5-b69c-24b397e71744/download)]. Sin serie reciente.
- **Salarios locales [V]** ([TalentUp](https://talentup.io/salary/hardware-engineer/colombia)):

| Perfil | Colombia (anual) | Referencia EE.UU. |
|---|---|---|
| Ingeniero electrónico junior | ~US$11k | |
| Ingeniero de firmware | ~US$18.6k | US$175k a 207k en un fabricante de chips |
| Ingeniero de hardware | ~US$24.6k | |
| Colombiano contratado remoto por firma de EE.UU. (software) | US$60k a 78k | |

- La diferencia es de 5 a 8 veces contra EE.UU. India está en ~US$15k, o sea que Colombia no es el más barato del mundo [V].
- **Inglés:** puesto 76 en el índice EF 2025, banda "baja" [V] ([EF](https://www.ef.com/assetscdn/WIBIwq6RdJvcD9bc8RMd/cefcom-epi-site/fact-sheets/2025/ef-epi-fact-sheet-colombia-english.pdf)). Es una restricción real para vender servicios.
- **Riesgo de talento [I]:** el mejor ingeniero puede ganar 3 veces más trabajando remoto para EE.UU. Una firma local compite por talento contra ese salario, no contra el salario colombiano promedio.

## 5.3 Impuestos y comercio

| Tema | Regla | Fuente |
|---|---|---|
| IVA | 19% sobre importaciones | [V] [Invest in Colombia](https://investincolombia.com.co/sites/default/files/2025-07/cap-4-comercio-exterior-y-aduanas.pdf) |
| Arancel a componentes | 0% para productos del acuerdo ITA (Decreto 1563/2017). Sin confirmar partida por partida | [V] |
| Envíos por courier | Hasta US$200 sin arancel. Pedidos comerciales van por importación ordinaria | [V] [DIAN](https://www.dian.gov.co/Viajeros-y-Servicios-aduaneros/Paginas/Modalidad-de-trafico-postal-y-envios-urgentes.aspx) |
| Plan Vallejo | Importas insumos y equipos sin arancel ni IVA si exportas el resultado. Solo 4.6% de los exportadores lo usa | [V] [Bancolombia](https://blog.bancolombia.com/negocios/plan-vallejo-expres-que-es-y-para-que-sirve/) |
| Zona franca | Renta de 20% sobre ingresos de exportación con plan de internacionalización. Difiere arancel e IVA | [V] [Actualícese](https://actualicese.com/tarifa-preferencial-del-impuesto-de-renta-para-usuarios-de-zonas-francas-se-reglamento/) |
| Renta general | 35% | [V] |
| Incentivo a I+D | Descuento de 30% del presupuesto aprobado por MinCiencias, o crédito de 50% para pymes. Convocatoria irregular: no hubo en 2024 | [V] [MinCiencias](https://especiales.minciencias.gov.co/wp-content/uploads/2025/11/Beneficios-Tributarios.pdf) |
| Arancel de EE.UU. a bienes colombianos | 12.5% desde julio de 2026. En negociación | [V] [Rio Times](https://www.riotimesonline.com/trump-may-lift-colombia-tariff-2026/) |

**Política industrial:**
- CONPES 4129 de reindustrialización (2023 a 2034) [V] ([MinCIT](https://www.mincit.gov.co/prensa/noticias/industria/gobierno-aprobo-el-conpes-de-reindustrializacion)).
- Proyecto de ley de industria electrónica y semiconductores con informe de conciliación de junio de 2026. Sanción sin confirmar [V] ([Cámara](https://www.camara.gov.co/wp-content/uploads/2026/06/proyectos-ley/publicaciones/proyecto-35776/INFORME-DE-CONCILIACION-PL-047-DE-2024-S-338-DE-2025-C-INDUSTRIA-ELECTRONICA-Y-SEMICONDUCTORES.docx-2-1.pdf)). Vale la pena seguirlo.
- La electrónica hoy está excluida de los programas de Colombia Productiva [V].

## 5.4 Logística: el punto crítico

**Salida (Colombia a EE.UU.): razonable.**
- FedEx tiene carguero directo Miami, Bogotá, Medellín, 6 vuelos por semana, con entrega a cualquier código postal de EE.UU. en menos de 72 horas [V] ([FedEx](https://newsroom.fedex.com/newsroom/fedex-express-launches-new-miami-bogota-medellin-miami-route-connecting-colombian-businesses-to-possibilities-worldwide)).
- El Dorado movió 810k toneladas en 2025, principal aeropuerto de carga de la región [V] ([Analdex](https://analdex.org/2026/03/18/informe-trafico-aereo-en-colombia-enero-a-diciembre-2025/)).
- Zona horaria: igual a la costa este de EE.UU. en invierno, una hora menos en verano.

**Entrada (componentes hacia Colombia): el problema.**
- No hay distribuidores con inventario local relevante. Todo componente viene de Digi-Key, Mouser o LCSC por courier.
- Cada pedido comercial paga 19% de IVA, más agenciamiento, más tiempo de aduana [I]. No encontré datos de tiempos de nacionalización de la DIAN.
- En un negocio donde el producto es velocidad de iteración, cada vuelta de prototipo espera a que lleguen las piezas. Un competidor en EE.UU. recibe de Digi-Key al día siguiente.

**Conclusión [I]:** el ciclo físico completo desde Colombia (pedir piezas, recibir, ensamblar, enviar) es de 1.5 a 3 semanas en el mejor caso, contra días en EE.UU. Hay tres formas de mitigarlo:
1. Operar en zona franca o con Plan Vallejo para eliminar IVA y agilizar aduana.
2. Mantener inventario propio de los componentes más usados.
3. Separar funciones: diseñar en Colombia y ensamblar prototipos cerca del cliente (EE.UU. o México). Es el modelo de Titoma con Asia.

Este es el supuesto más importante por validar antes de invertir en una línea de ensamble local para exportación.

## 5.5 Regulación para vender hardware en Colombia

- **INVIMA (dispositivos médicos):** clases I y IIa tienen registro automático. IIb y III requieren evaluación técnica. De 4 a 6 meses [V, consultoras] ([INVIMA](https://www.invima.gov.co/productos-vigilados/dispositivos-medicos/dispositivos-medicos-equipos-biomedicos)).
- **CRC (radio):** la homologación aplica a terminales móviles. Otros equipos de telecomunicaciones no requieren homologación adicional, lo que probablemente exime a muchos dispositivos IoT con Wi-Fi o Bluetooth [V] ([TeleSemana](https://www.telesemana.com/blog/2025/06/26/la-crc-actualizo-la-normativa-tecnica-para-la-homologacion-de-equipos/)).
- **Laboratorios:** no encontré un laboratorio de compatibilidad electromagnética acreditado por ONAC. Uniandes tiene cámara anecoica. Las pruebas formales para FCC o UL se hacen en el exterior [I].

## 5.6 Demanda local

- **Dispositivos médicos:** mercado de US$1.6B a 1.8B. El 82% es importado. Solo 8% de los registros INVIMA corresponde a fabricación nacional [V] ([ITA](https://www.trade.gov/knowledge-product/colombia-medical-equipment), [MedDeviceGuide](https://meddeviceguide.com/blog/colombia-invima-importer-apoderado-concentration-channel-lock-in-analysis-2026)).
- **Energía:** la regulación obliga a los operadores de red a desplegar medición inteligente [V] ([CREG](https://gestornormativo.creg.gov.co/gestor/entorno/docs/resolucion_creg_101-1_2022.htm)). Avance real bajo.
- **Defensa y drones:** programa antidrones de ~US$1.68B. 318 ataques con drones explosivos en 2026 hasta octubre. CODALTEC con contratos de ~COP 65,000M. Algunos sistemas comprados fallaron pruebas técnicas [V] ([Rio Times](https://www.riotimesonline.com/colombia-puts-drone-manufacturing-at-the-center-of-its-military-industry/)). Hay presupuesto, urgencia y un incentivo político a comprar nacional.
- **Transporte:** empresas de recaudo y tránsito en Bogotá están contratando líderes de PCB y firmware [V, ofertas de empleo].
- **Industria:** ver capítulo 4. Adopción baja en pymes.

## 5.7 Riesgos estructurales

- **Tasa de cambio:** el peso se fortaleció ~19% en 2026, a ~COP 3,300 por dólar [V]. La ventaja de costo para exportar servicios se redujo en la misma proporción. Un negocio de exportación con costos en pesos tiene este riesgo siempre.
- **Costo del capital:** tasa del Banco de la República en 12% [V]. Financiar inventario en pesos es caro. Otro argumento contra empezar por manufactura.
- **Riesgo país:** S&P en BB-, Fitch en BB [V] ([La República](https://www.larepublica.co/economia/rebaja-de-s-p-global-ratings-a-bb-llevo-el-riesgo-pais-al-nivel-mas-alto-en-un-ano-4368023)).
- **Política:** nuevo gobierno desde agosto de 2026, con relaciones con EE.UU. en reajuste [V] ([Local10](https://www.local10.com/espanol/2026/06/24/autoridad-electoral-declara-al-conservador-abelardo-de-la-espriella-presidente-electo-de-colombia/)). Puede mejorar el cuadro arancelario, sin garantía.
- **México:** exporta ~$107B en electrónica, tiene más de 730 plantas y arancel de 0% [V] ([Start-Ops](https://start-ops.com.mx/electronics-manufacturing-in-mexico-an-industry-analysis/)). En manufactura de volumen Colombia no compite con eso.

## 5.8 Balance

| A favor | En contra |
|---|---|
| Talento de ingeniería 5 a 8 veces más barato que EE.UU. | Inglés bajo |
| Zona horaria de EE.UU. | Sin cadena de suministro local de componentes |
| Entrega a EE.UU. en menos de 72 horas | Entrada de componentes lenta y con IVA |
| Terreno sin competencia local | Sin laboratorios de certificación |
| Caso probado de diseño exportado (Titoma) | El EMS más grande del país pasó por insolvencia |
| Demanda local con dependencia de importaciones | Arancel de 12.5% hoy, México en 0% |
| Zona franca y Plan Vallejo disponibles | Peso fuerte y crédito caro |

## 5.9 Lo que no se pudo verificar

Tiempos de nacionalización de la DIAN. Partidas arancelarias exactas de componentes y maquinaria. Exención de IVA para exportación de servicios. Reglas de origen del TLC. Tarifas reales de courier. Tiempos de entrega de Digi-Key, Mouser y LCSC a Colombia. Cifras recientes de graduados. Datos de ANDI sobre Industria 4.0. Estado actual de Colcircuitos y del proyecto de ley de electrónica.
