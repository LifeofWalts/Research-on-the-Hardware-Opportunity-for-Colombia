# 3. Cómo está evolucionando: IA, aranceles y demanda

Convención: **[V]** verificado en fuente. **[I]** inferencia. Las secciones 3.1 y 3.2 vienen de lectura directa de las fuentes primarias. El resto es de 2026 y viene de resúmenes de búsqueda.

## 3.1 Tus dos referencias: Diode y el artículo de Davide Asnaghi

Leídas de fuente primaria: el [sitio de Diode](https://www.diode.computer/) y sus cuatro publicaciones. El artículo de X no se pudo abrir en esa plataforma, pero Diode publicó el mismo título en su blog el 9 de noviembre de 2026, firmado por Asnaghi, Lenny Khazan y Zabie Elmgren: ["AI Hardware Design Gets Faster, Manufacturing Matters More"](https://blog.diode.computer/ai-hardware-design-manufacturing). Asumo que es el mismo texto.

### Qué vende Diode

"Tarjetas a la medida, diseñadas y fabricadas con IA". Tres pasos en un solo lugar [V]:

1. **Diseño:** los requisitos se convierten en esquemático y layout escritos como código, que el agente de IA y los ingenieros pueden revisar.
2. **Fabricación:** cada diseño se revisa contra las reglas de la fábrica antes de producir.
3. **Ensamble:** compran todos los componentes y ensamblan en su planta de Brooklyn, de prototipos a producción.

Dos formas de comprar [V]:

| | Autoservicio | Empresarial |
|---|---|---|
| Quién diseña | El cliente, con el agente de IA de Diode | Los ingenieros de Diode |
| Qué trae el cliente | Una descripción, un diagrama de bloques o un proyecto KiCad | Sus requisitos |
| Precio | Fabricación y ensamble, cotizados al instante | Desde $10,000 por diseño, más fabricación |
| Incluye | Revisión de manufacturabilidad antes de fabricar | Slack dedicado, soporte prioritario y bring-up |

**Lo que muestran de su propio trabajo [V]:**
- Dos tarjetas propias de 10 capas: un radio definido por software (70 MHz a 6 GHz) y una *carrier board* para NVIDIA Jetson Orin, pensada para robótica.
- Diseños de referencia abiertos: controlador de motor BLDC trifásico, sonda de depuración, *carrier* para Raspberry Pi CM5.

**Cifras que ellos reportan [V]** ([anuncio de Serie A](https://blog.diode.computer/series-a-announcement)):
- "Un diseño de tarjeta cada 4 días". Un solo ingeniero eléctrico entregó más de 100 diseños únicos en un año.
- Sus clientes bajaron las revisiones por tarjeta de cinco a una.
- Clientes: Physical Intelligence, Saronic, y varios proveedores Tier 1.
- Entregan en los formatos de Altium y Cadence si el cliente los usa.
- Cada tarjeta que pasa por Diode alimenta sus datos: rendimiento real, plazos de componentes, perfiles de soldadura.

**Tamaño:** $11.4M de Serie A liderada por a16z en julio de 2025, entre 8 y 11 empleados según bases de datos [V] ([PitchBook](https://pitchbook.com/profiles/company/620727-22)). Ingresos no públicos. Están contratando ingenieros de nivel *staff*.

### Cómo trabaja por dentro

De ["Teaching Claude To Design Circuit Boards That Ship"](https://blog.diode.computer/anthropic-partnership) [V]:

- **Zener:** lenguaje abierto para describir tarjetas como código. Se puede versionar, revisar y probar como software, y un modelo lo lee y escribe con facilidad porque se parece a Python.
- **Biblioteca pública:** un flujo automático produjo cerca de 250 diseños de referencia en dos semanas (sensores, microcontroladores, etapas de potencia, cadenas analógicas).
- **El "Registry", su activo privado:** módulos ya probados en proyectos reales, cada uno con su fragmento de layout validado y datos de manufactura. Incluye plataformas de cómputo (Qualcomm, Jetson) y frentes de radiofrecuencia.
- **Efecto:** arrancar un proyecto pasa de empezar en blanco a componer bloques probados. Reportan pasar "de meses a semanas".
- **Simulación como verdad:** cada módulo corre simulaciones automáticas. Si el circuito no cumple, el modelo ve por qué e itera.
- **Los ingenieros firman cada diseño.**

De ["A Better Way to Review Hardware"](https://blog.diode.computer/hardware-review) [V]:

- Su revisor con IA encontró 22 errores en el reto de hardware de comma.ai y ganó el premio.
- Reconocen el límite: no reemplaza validación en laboratorio, pruebas electromagnéticas, térmicas, certificación ni la firma final. "El hardware real todavía hay que medirlo y validarlo".

### La tesis del artículo

En orden [V]:

1. **Diseñar una tarjeta es, en el fondo, producir un archivo que cumple reglas.** Con el entorno y los datos correctos, los modelos lo hacen bien. Diode lleva dos años ayudando a entrenarlos.
2. **Todavía fallan** en radiofrecuencia, entrega de potencia y ruteo de alta velocidad. Cada versión falla menos.
3. **Pronto alguien sin formación en electrónica** va a describir lo que quiere y obtener un diseño que funciona, "al menos en el papel".
4. **El hardware a la medida da mejor producto:** más pequeño, más barato en volumen, con menos piezas que fallan. No se hacía porque era lento y caro, y los buenos ingenieros eléctricos son escasos.
5. **Si diseñar se vuelve fácil, más equipos harán hardware a la medida.** Lo difícil pasa a ser fabricarlo.
6. **El mundo real es desordenado.** Un componente se agota entre la revisión y la fabricación. Un archivo es ambiguo y el pedido queda detenido mientras la fábrica adivina. Eso cuesta semanas o deja tarjetas que no funcionan.
7. **"El puente entre el archivo de diseño y la tarjeta en tu mano es donde está el valor duradero."** Se necesitan datos en vivo: qué componentes se consiguen, qué puede fabricar una planta en el lugar correcto, cuánto cuesta a tu plazo y volumen. Eso solo se controla cuando fabricas y entregas.
8. **La manufactura queda como el único cuello de botella.** Robótica y centros de datos aceleran el ritmo.
9. **Cambia lo que se le pide a las fábricas.** Si una revisión cuesta lo que toma escribir un prompt, los equipos harán muchas más versiones en lotes más pequeños. Ese trabajo de alta mezcla siempre fue lento y caro, y por eso se fue al exterior.
10. **Para que EE.UU. compita**, la tecnología debe permitir tandas pequeñas de tarjetas nuevas, baratas y bien a la primera, con capacidad de escalar.

## 3.2 Qué demostró la IA en noviembre de 2026

Anthropic publicó el 9 de noviembre de 2026 ["Claude can design electronic prototypes from start to finish"](https://www.anthropic.com/research/claude-electronics-design), hecha con Diode. Leída de fuente primaria [V]. La publicación declara que hay relación comercial entre las dos empresas.

- **Qué hizo:** un modelo de Claude diseñó tres dispositivos a partir de una instrucción corta: un altavoz manos libres USB, un asistente de voz para el hogar y una mascota virtual portátil a batería. Para cada uno escribió especificaciones, esquemático, layout de 4 capas, carcasa imprimible en 3D, firmware y lista de materiales.
- **Resultado:** Diode fabricó las tres tarjetas directo de los archivos, sin correcciones a los circuitos. El altavoz sigue funcionando tras semanas de uso.
- **Cómo trabajó:**
  - Ruteó primero las señales críticas (alta velocidad, alta corriente, sensibles al ruido).
  - Leyó hojas de datos para decidir. Predijo correctamente un comportamiento del cargador sin batería.
  - Cuando el ruteador disponible no bastó, escribió el suyo en cerca de media hora.
  - Borró y rehízo conexiones decenas de veces al ver que el layout se enredaba. Los modelos anteriores casi nunca corregían su propio trabajo y dejaban tarjetas "95% completas pero inutilizables".
  - Corrió las revisiones de manufacturabilidad y de disponibilidad de componentes, y separó errores reales de falsos.
- **Mediciones:**
  - En la prueba interna de layout de Diode ("PCB Gym"): 69% contra 25% de la versión anterior. Es interna y no verificable de forma independiente.
  - En BenchCAD 2.1, prueba pública de reconstrucción de piezas y tarjetas: 83.5%, casi el doble de la versión previa.
- **Qué hicieron los humanos:** ensamblar, cargar el firmware y probar. El modelo no estaba conectado a instrumentos ni a máquinas de fabricación. Las instrucciones fueron mínimas ("limpia el esquemático", "continúa").
- **Límites declarados:** son prototipos. No pasaron validación eléctrica, ajuste de antena, pruebas térmicas ni certificación. No están diseñados para producción masiva.
- **Lo que sigue según ellos:** tarjetas más densas y rápidas, verificación por simulación, y aprender de mediciones sobre dispositivos terminados. Mencionan que OpenAI publicó un trabajo similar.

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
2. **La IA también nivela la cancha.** Un equipo pequeño con estas herramientas produce lo que antes requería un equipo grande. Diode reporta más de 100 diseños al año por ingeniero. Su lenguaje y su biblioteca pública son abiertos. La barrera de entrada al diseño baja para todos, incluido un equipo en Medellín o Bogotá.
3. **Lo abierto no es el foso.** El activo de Diode es privado: su biblioteca de módulos ya validados en proyectos reales y los datos que le devuelve su propia fábrica. Quien entre tiene que construir su equivalente, proyecto por proyecto.
4. **El extremo simple ya tiene autoservicio.** Una startup de EE.UU. que necesita una tarjeta sencilla puede diseñarla con el agente de Diode y recibirla cotizada al instante. Los controladores de motor y las *carrier boards* para Jetson, que parecían nichos accesibles, ya existen como diseños de referencia abiertos. Competir ahí por precio no tiene sentido.
5. **El valor se mueve a lo físico:** fabricar rápido, probar con instrumentos, depurar, certificar, responder por el resultado. Es justo lo que el modelo no pudo hacer en la demostración. Ese trabajo de laboratorio es mano de obra calificada, y ahí el costo colombiano sí es ventaja, siempre que el ciclo físico (componentes que entran, tarjetas que salen) sea rápido.

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
