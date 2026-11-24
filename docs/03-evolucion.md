# 3. Cómo está evolucionando: IA, aranceles y demanda

Convención: **[V]** verificado en fuente. **[I]** inferencia. Mucho de este capítulo es de 2026 y viene de resúmenes de búsqueda, no de lectura directa de las páginas.

## 3.1 Tus dos referencias: Diode y el artículo de Davide Asnaghi

No pude abrir ninguna de las dos páginas (la red de esta sesión las bloquea). Lo que sigue viene de fuentes secundarias.

**Diode Computers**
- **Qué vende:** "tarjetas como servicio". El cliente describe lo que necesita y recibe tarjetas funcionando, no archivos [V] ([a16z](https://a16z.com/announcement/investing-in-diode/)).
- **Cómo lo hace:** el diseño se escribe como código, en un lenguaje propio y abierto llamado Zener. Agentes de IA generan y revisan el diseño contra las hojas de datos de los componentes. Ingenieros humanos hacen la revisión final. Fabrican en su propia planta en Brooklyn [V] ([GitHub](https://github.com/diodeinc/pcb), [a16z Policy](https://a16zpolicy.substack.com/p/turning-americas-ai-progress-into)).
- **Precio:** desde ~$10,000 por diseño más fabricación en el nivel empresarial [V, vía resumen de su sitio]. Un ejemplo de cotización automática: 5 tarjetas por $5,498 en 9 días [V] ([GitHub PR](https://github.com/diodeinc/pcb/pull/1543)). Es un solo dato, no una lista de precios.
- **Ritmo:** "un diseño de tarjeta cada 4 días" [V] ([blog de Diode](https://blog.diode.computer/series-a-announcement)).
- **Clientes:** Physical Intelligence (robótica), Saronic (defensa naval) [V].
- **Tamaño:** $11.4M de Serie A liderada por a16z en julio de 2025, más de $14.5M en total, entre 8 y 11 empleados [V] ([PitchBook](https://pitchbook.com/profiles/company/620727-22)). Ingresos no públicos.
- **Historia:** empezaron con una herramienta de validación de diseño y pivotaron a controlar todo el flujo, del diseño a la fábrica [V].

**El artículo de X**
- Título: **"AI Hardware Design Gets Faster, Manufacturing Matters More"**, publicado cerca del 9 de noviembre de 2026 [V, solo extractos].
- Tesis, según los extractos:
  1. Los modelos todavía fallan en radiofrecuencia, entrega de potencia y ruteo de alta velocidad, pero cada versión necesita menos corrección.
  2. Cuando un modelo puede diseñar la tarjeta y escribir el firmware a pedido, **la manufactura se vuelve el cuello de botella**.
  3. Diseñar más rápido solo crea valor si la fábrica sigue el ritmo.
  4. Diseñar más fácil va a atraer a más equipos a hacer hardware a la medida.
- No tengo el texto completo. Si lo pegas, lo incorporo.

## 3.2 Qué demostró la IA en noviembre de 2026

Anthropic publicó el 9 de noviembre de 2026 una investigación hecha con Diode [V] ([Anthropic](https://www.anthropic.com/research/claude-electronics-design), [Adafruit](https://blog.adafruit.com/2026/11/09/claude-claims-it-can-now-design-electronic-prototypes-from-start-to-finish/)):

- **Qué hizo:** un modelo de Claude diseñó tres dispositivos completos (un altavoz manos libres, un asistente de voz y una mascota virtual portátil). Para cada uno produjo especificaciones, esquemático, layout de 4 capas, carcasa, firmware y lista de materiales.
- **Resultado:** las tres tarjetas se fabricaron sin rondas de corrección.
- **Medición:** en la prueba interna de layout de Diode ("PCB Gym") el modelo nuevo sacó 69% contra 25% del anterior. La prueba es interna y hay relación comercial entre las partes, así que no es verificable de forma independiente.
- **Qué siguieron haciendo humanos:** ensamblar y probar las tarjetas a mano. No hubo validación eléctrica, ajuste de antena, pruebas térmicas ni certificación. No eran diseños para producción masiva [V, cobertura secundaria de la misma publicación].

Otros jugadores van en la misma dirección:
- **Quilter** (layout con IA): $40M levantados. Reporta un computador Linux de 843 componentes que arrancó a la primera, con 38.5 horas humanas contra 428 cotizadas manualmente. Dato propio de la empresa [V] ([Quilter](https://www.quilter.ai/project-speedrun)).
- **Flux.ai** (diseño en el navegador con copiloto): $37M en febrero de 2026, dice tener más de 1M de usuarios [V].
- **Circuit Mind** (Reino Unido): $25M en octubre de 2026 [V] ([Axios](https://www.axios.com/pro/all-deals/2026/10/28/circuit-mind-25m-ai-electronics-design)).
- **Cadence** lanzó una capa de agentes sobre su herramienta profesional. Cita una tarea que pasó de 20 días a 20 minutos [V] ([Futurum](https://futurumgroup.com/insights/cadence-aurastack-extends-agentic-leadership-toward-advanced-packaging-design/)).
- **Cofactr** automatiza compras de componentes [V].

## 3.3 Qué se abarata y qué sigue escaso

| Se está volviendo commodity [I] | Sigue escaso [I] |
|---|---|
| Captura de esquemático | Arquitectura del sistema e integración entre módulos |
| Selección de componentes y BOM | Radiofrecuencia, antenas, potencia, señales de alta velocidad |
| Layout digital rutinario de 2 a 6 capas | Compatibilidad electromagnética y térmica |
| Revisión de reglas de diseño y DFM | Bring-up y depuración física en laboratorio |
| Esqueleto de firmware | Certificación |
| Cotización y compras | Proceso de manufactura, pruebas, rendimiento |
| | Cadena de suministro y confianza del cliente |

**Implicación directa para una tesis desde Colombia:**

1. **El arbitraje salarial en horas de diseño vale menos cada año.** Si un modelo hace el layout, vender "ingenieros baratos por hora" es apostar a lo que se está abaratando.
2. **La IA también nivela la cancha.** Un equipo pequeño con estas herramientas produce lo que antes requería un equipo grande. Las herramientas de Diode son abiertas. La barrera de entrada al diseño baja para todos, incluido un equipo en Medellín o Bogotá.
3. **El valor se mueve a lo físico:** fabricar rápido, probar con instrumentos, depurar, certificar, responder por el resultado. Es justo lo que el modelo no pudo hacer en la demostración. Ese trabajo de laboratorio es mano de obra calificada, y ahí el costo colombiano sí es ventaja, siempre que el ciclo físico (componentes que entran, tarjetas que salen) sea rápido.

## 3.4 Aranceles y relocalización a finales de 2026

**El cuadro cambió tres veces en 2026:**
- Febrero: la Corte Suprema de EE.UU. tumbó los aranceles basados en IEEPA [V] ([Global Trade Alert](https://globaltradealert.org/blog/from-ieepa-to-section-122)).
- Febrero a julio: recargo global temporal de 10%.
- Desde el 24 de julio: aranceles bajo Sección 301 a 60 economías [V] ([Federal Register](https://www.federalregister.gov/documents/2026/07/28/2026-15274/)).

**Arancel de EE.UU. sobre tarjetas, por origen:**

| Origen | Arancel | Nota |
|---|---|---|
| China | ~37.5% | 25% anterior más 12.5% nuevo [V] ([Atlas PCB](https://www.atlaspcb.com/news/news-pcb-tariff-section-301-exclusion-expiry-november-2026/)) |
| México | 0% | Si cumple origen T-MEC [V] ([Holland & Knight](https://www.hklaw.com/en/insights/publications/2026/07/mexico-mantiene-acceso-preferencial-bajo-el-tmec)) |
| Colombia | 12.5% | El TLC no lo exime. No está confirmado si la electrónica entra en las exenciones. Hay negociación para diciembre de 2026, sin garantía [V] ([Rio Times](https://www.riotimesonline.com/colombia-tariff-talks-december-us-deal-2026/)) |

**Otros hechos:**
- Se eliminó la exención de envíos menores a $800 (*de minimis*). Un pedido de $20 a un fabricante chino pasó a ~$60 [V] ([PCBWay](https://www.pcbway.com/blog/News/Impact_of_the_New_U_S_Tariff_Policy_on_Customs_Clearance_51dff4fd.html)).
- China fabrica 50 a 57% de las PCB del mundo. Norteamérica 4 a 5% [V] ([CNBC](https://www.cnbc.com/2026/06/03/beneath-nvidia-ai-chips-chinese-pcbs-raise-security-concerns-in-us.html)).

**Lectura [I]:**
- Los aranceles aplican a **bienes**. Un servicio de diseño exportado no paga arancel. Esto favorece empezar por diseño.
- En bienes, Colombia hoy queda 25 puntos mejor que China y 12.5 puntos peor que México. Para volumen, México gana.
- En bajo volumen y prototipos el arancel pesa poco. Pesa la velocidad.
- El cuadro es inestable. Un negocio que dependa de una tasa arancelaria específica es frágil.

## 3.5 Motores de demanda

- **Robótica:** más de $18.8B levantados en 2026 a mitad de año, ya por encima de todo 2025 (detalle en capítulo 4).
- **Defensa:** las startups de defensa levantaron más de $14.6B en 2026. Anduril a $61B de valoración. Saronic, cliente de Diode, levantó $1.75B [V] ([TechCrunch](https://techcrunch.com/2026/07/24/anduril-reportedly-in-talks-to-raise-funding-at-100b-valuation-more-than-3x-last-years-mark/)). Mercado cerrado para extranjeros, pero absorbe la capacidad de los proveedores de EE.UU. y deja desatendido lo demás [I].
- **Capacidad en EE.UU. apretada:** los pedidos de EMS en Norteamérica superan los despachos, con relación de 1.33 en junio de 2026 [V].
- **Faltan ingenieros:** EE.UU. tiene ~288k ingenieros eléctricos y electrónicos con ~17.5k vacantes al año. La industria de chips sola necesita más de 104k ingenieros adicionales a 2030. Alemania proyecta más de 100k puestos sin llenar en una década [V] ([CNBC](https://www.cnbc.com/2026/09/17/us-chipmakers-face-deep-labor-shortage-samsung-micron-sound-alarm.html)).
- **Segmento desatendido:** los programas de menos de ~50k unidades al año no le interesan a los EMS grandes [V, fuente de proveedor].

## 3.6 Empresas de referencia del nuevo modelo

| Empresa | Qué hace | Señal |
|---|---|---|
| Hadrian | Mecanizado automatizado para defensa | $1.37B levantados a $7.87B de valoración en agosto de 2026 [V] ([Washington Technology](https://www.washingtontechnology.com/companies/2026/08/hadrian-fetches-137b-add-more-automation-intensive-factories/415251/)) |
| Fictiv | Mercado digital de manufactura | Comprada por MISUMI por $350M en 2025 [V] |
| MacroFab | Plataforma de ensamble en EE.UU. y México | ~$102M levantados, reportes de despidos [V] |
| Tempo Automation | Prototipos rápidos en San Francisco | Quebró en 2023 [V] |
| ProvenMetal (YC S26), Axal (YC W25) | Ensamble rápido con IA | Nuevos entrantes en el mismo espacio que Diode [V] |

No encontré un equivalente latinoamericano de Diode.

## 3.7 Síntesis

1. La IA comprime el tiempo de diseño de semanas a días. El diseño rutinario pierde valor como servicio aislado.
2. Diseñar más fácil aumenta la cantidad de equipos que hacen hardware propio. El mercado total crece.
3. El cuello de botella pasa a ser el ciclo físico: fabricar, probar, corregir. Quien controle ese ciclo captura el valor.
4. La geopolítica empuja a sacar manufactura de China, pero el beneficiario natural por aranceles y escala es México, no Colombia.
5. La ventana abierta es el bajo volumen y alta mezcla con respuesta rápida, que los grandes no atienden.
