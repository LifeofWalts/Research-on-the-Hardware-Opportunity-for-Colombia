# 1. Fundamentos: qué es "hacer hardware para otros"

Objetivo de este capítulo: que puedas leer el resto del research sin conocimiento previo de electrónica. Todo parte de principios básicos.

## 1.1 Qué es un producto electrónico

Todo producto electrónico hace tres cosas: **siente** (sensores, botones, radios que reciben), **decide** (un chip que ejecuta software) y **actúa** (motores, pantallas, radios que transmiten). Un reloj inteligente, un robot y un PLC de fábrica son variaciones de lo mismo.

Para que eso exista se necesitan cuatro capas:

| Capa | Qué es | Analogía |
|---|---|---|
| Componentes | Chips, resistencias, conectores, sensores. Los fabrican empresas como TI, ST, NXP, Nordic, NVIDIA | Los ladrillos |
| PCB (la tarjeta) | Lámina de fibra de vidrio con pistas de cobre que conecta los componentes entre sí | Los planos y la plomería del edificio |
| Firmware | Software que corre dentro del chip y controla el hardware | El sistema nervioso |
| Mecánica | Carcasa, disipación de calor, cables, ensamblaje final | La fachada y la estructura |

Una "board a la medida" es una PCB diseñada para un producto específico, con los componentes ya soldados y normalmente con su firmware.

## 1.2 Vocabulario mínimo

- **Esquemático**: el diagrama lógico. Dice qué componente se conecta con cuál. Es la decisión de ingeniería más importante.
- **Layout**: el diseño físico de la tarjeta. Dónde va cada componente y por dónde pasan las pistas de cobre. Aquí viven los problemas de calor, ruido e interferencia.
- **Stack-up / capas**: una PCB tiene de 2 a 20+ capas de cobre. Más capas permiten más densidad y mejor señal, pero cuestan más.
- **BOM** (Bill of Materials): la lista de todos los componentes con su precio y proveedor. Es el costo variable principal del producto.
- **Gerbers**: los archivos que se le mandan a la fábrica para producir la tarjeta. Equivalen al "PDF final" del diseño.
- **PCB vs PCBA**: PCB es la tarjeta vacía. PCBA es la tarjeta con los componentes soldados (A de assembly).
- **SMT**: la tecnología de montaje superficial. Una máquina *pick and place* pone los componentes sobre pasta de soldadura y un horno (*reflow*) los fija. Es el proceso central de cualquier fábrica de electrónica.
- **DFM** (Design for Manufacturing): diseñar para que la fábrica pueda producir sin errores y a bajo costo.
- **Bring-up**: la primera vez que se enciende una tarjeta nueva y se depura hasta que funcione. Es trabajo de laboratorio, con osciloscopio en mano.
- **NRE** (Non-Recurring Engineering): el costo único de diseñar. Se paga una vez, a diferencia del costo por unidad.
- **EVT / DVT / PVT**: las tres etapas de validación antes de producción masiva (ingeniería, diseño, producción). Cada una es una tanda de prototipos más cercana al producto final.
- **Certificación**: pruebas obligatorias para vender (FCC en EE.UU., CE en Europa, UL para seguridad eléctrica, IEC 60601 para equipo médico).

## 1.3 El ciclo de vida de una board

```
Idea -> Requisitos -> Arquitectura -> Esquemático -> Layout -> Fabricación PCB
     -> Compra de componentes -> Ensamble (PCBA) -> Bring-up y pruebas
     -> Iterar (2 a 4 vueltas) -> Certificación -> Producción -> Soporte
```

Tres hechos de este ciclo explican casi todo el negocio:

1. **Cada iteración es física.** En software un error se corrige en minutos. En hardware un error significa fabricar otra tarjeta: días o semanas y dinero real. Por eso la velocidad de iteración es el recurso escaso y por eso la gente paga por expertos que se equivoquen menos.
2. **El costo se decide en el diseño.** Se estima que cerca del 80% del costo de un producto queda fijado en la etapa de diseño (regla general de la industria). Quien diseña tiene poder sobre quién fabrica y con qué componentes.
3. **El riesgo está en los detalles no digitales.** Ruido eléctrico, calor, interferencia, componentes que se agotan en el mercado, tolerancias de fábrica. Es conocimiento tácito que se gana con experiencia y es difícil de copiar.

## 1.4 Quién hace qué: los actores

| Actor | Qué hace | Ejemplos |
|---|---|---|
| OEM / marca | Dueño del producto y del cliente final | Apple, una startup de robótica, un fabricante de equipos médicos |
| Casa de diseño (design house) | Diseña electrónica por encargo. Vende horas de ingeniería o proyectos | Consultoras de desarrollo de producto |
| Fabricante de PCB | Produce la tarjeta vacía | Fábricas en China, Taiwán, algunas en EE.UU. |
| EMS / CM (contract manufacturer) | Ensambla y prueba productos diseñados por otros | Foxconn, Jabil, Flex, y miles de talleres pequeños |
| ODM | Diseña y fabrica un producto que otro vende con su marca | Quanta, Compal, muchos en Shenzhen |
| Distribuidor | Vende componentes | Digi-Key, Mouser, Arrow, Avnet, LCSC |
| Laboratorio de certificación | Prueba y certifica | UL, TÜV, Intertek |

"Hacer hardware para otros" significa ocupar uno o varios de los roles intermedios: casa de diseño, EMS, ODM, o una mezcla. La pregunta estratégica de este research es **cuál de esos roles tiene sentido ocupar desde Colombia**.

## 1.5 Los cinco modelos de negocio posibles

De menor a mayor capital requerido:

1. **Staff augmentation**: alquilar ingenieros de hardware/firmware por hora o mes a empresas extranjeras. Cero inventario. Margen por arbitraje salarial.
2. **Servicios de diseño por proyecto**: el cliente trae un problema, tú entregas el diseño (archivos + prototipos funcionando). Se cobra NRE. Se parece a una agencia de software.
3. **Diseño + manufactura de bajo volumen ("boards as a service")**: diseñas, compras componentes, ensamblas y entregas tarjetas funcionando. Es el modelo de Diode. Combina ingreso por ingeniería con ingreso por unidad.
4. **EMS / manufactura por contrato**: tienes líneas SMT y ensamblas diseños de otros. Negocio de volumen, capital y capital de trabajo.
5. **Producto propio / ODM / módulos**: diseñas una vez y vendes muchas veces (un módulo, un controlador, un gateway). Mejor margen, más riesgo de mercado.

La lógica económica de fondo:

- **Diseñar** es un negocio de talento: margen bruto alto, escala lineal con personas, poco capital.
- **Fabricar** es un negocio de activos y logística: margen bajo, escala con volumen, mucho capital de trabajo.
- **El punto intermedio** (bajo volumen, alta mezcla, entrega rápida) cobra una prima por velocidad y conveniencia, no por costo unitario.

Los capítulos siguientes ponen números a cada una de estas afirmaciones.
