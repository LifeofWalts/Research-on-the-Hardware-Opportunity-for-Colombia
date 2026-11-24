# 7. Veredicto: ¿vale la pena explorarlo desde Colombia?

Este capítulo es mi análisis sobre la evidencia de los capítulos anteriores. Es opinión razonada, no dato.

## 7.1 Respuesta corta

**Sí vale la pena explorarlo, pero solo en una forma estrecha.** La tesis amplia ("fabricar hardware para otros desde Colombia") no se sostiene. Una tesis específica sí: un equipo pequeño, nativo en IA, que diseña y valida tarjetas para un nicho, con frente comercial en EE.UU. y un camino deliberado hacia ingreso que no dependa de horas.

El momento es bueno por una razón concreta: la IA acaba de bajar la barrera del diseño (noviembre de 2026) y todavía no existe un jugador latinoamericano en este espacio.

## 7.2 Lo que no funciona, y por qué

| Tesis | Por qué no |
|---|---|
| **EMS de volumen para exportar** | México tiene arancel de 0%, más de 730 plantas y mano de obra más barata que China. Colombia paga 12.5%, importa todos los componentes y financia inventario con tasa de referencia en 12%. Margen operativo de 4% sin escala es pérdida |
| **Vender horas de ingeniería baratas** | Es exactamente lo que la IA está abaratando. India cobra menos. El inglés es una limitación. Sasken muestra dónde termina: margen de 1.6% |
| **Defensa de EE.UU.** | ITAR lo cierra para extranjeros |
| **Electrónica de consumo** | Compite de frente con Shenzhen en costo |
| **Dispositivos médicos como primer mercado** | Ciclos de 6 a 18 meses e historial exigido. Sirve como segundo paso, no como entrada |
| **Fábrica de prototipos rápidos en Colombia para EE.UU., desde el día uno** | La entrada de componentes a Colombia rompe la promesa de velocidad. Tempo Automation quebró con mejor logística. Solo después de validar el ciclo físico |

## 7.3 Lo que sí puede funcionar

### Opción A: estudio de diseño y validación para startups de robótica e industrial de EE.UU.

- **Qué vende:** tarjetas funcionando y probadas (drivers de motor, BMS, sensores, hardware de prueba), no horas.
- **Por qué puede ganar:**
  - El cliente tiene urgencia, dinero y falta de ingenieros.
  - La IA hace el diseño rutinario. El equipo pone lo que la IA no hace: arquitectura, potencia, bring-up en laboratorio, responder por el resultado.
  - El trabajo de laboratorio es mano de obra calificada, donde Colombia sí es 5 a 8 veces más barata.
  - El diseño es un servicio: no paga arancel.
- **De qué depende:** de conseguir los primeros 3 clientes sin historial, y de que el ciclo físico no sea más lento que el de un competidor en EE.UU.
- **Contra quién compite:** Diode ya atiende este mismo cliente desde Brooklyn, con autoservicio para lo simple y sus ingenieros para lo complejo desde $10,000 por diseño. Un equipo en Colombia no gana en lo genérico ni en velocidad de entrega. Gana solo si es mejor en un tipo de problema específico o si cobra bastante menos por el mismo resultado.
- **Cómo cobrar:** por tarjeta funcionando, no por hora. Con IA y bloques reutilizables, el ingreso por ingeniero puede ser 2 a 3 veces el de vender horas (capítulo 6).
- **Tamaño realista:** $1M a $3M de ingresos en 3 años. Si se cobra por resultado, con 8 a 20 personas en vez de 15 a 40. Rentable, no explosivo.

### Opción B: hardware para demanda local y andina

- **Qué vende:** soluciones completas para industria (modernización de máquinas, gateways), transporte (recaudo, flotas), energía (monitoreo) y defensa nacional (drones, antidrones).
- **Por qué puede ganar:**
  - Aquí Colombia no compite con México ni con Diode. Compite con importaciones mal adaptadas y sin soporte.
  - Defensa tiene presupuesto (~US$1.68B en antidrones), urgencia (318 ataques en 2026) y sistemas importados que fallaron pruebas.
  - Cercanía, idioma y soporte en sitio son ventajas reales.
- **De qué depende:** de relaciones, de contratación pública y de ciclos de venta largos. El comprador industrial colombiano adopta lento.
- **Tamaño realista:** contratos grandes pero irregulares.

### Opción C: producto propio en un nicho (la ruta Teltonika)

- No es un punto de partida. Es a donde A o B deberían llevar.
- Cada proyecto deja bloques reutilizables. Cuando el mismo bloque se vende tres veces, hay un producto.
- Candidatos naturales: familia de controladores de motor para robótica, gateway industrial para la región, electrónica de drones no china.
- Es la única opción con economía de escala real: margen neto de ~15% y crecimiento que no depende de contratar.

### Cómo se combinan

```
Año 1:  Diseño y validación (A)  ->  caja, oficio, reputación
Año 2:  + producción de bajo volumen para los mismos clientes  ->  ingreso recurrente
Año 3+: + producto propio en el nicho que más se repita (C)   ->  escala
        B corre en paralelo si aparece un cliente ancla local
```

Es la misma secuencia de eInfochips, VVDN, Kaynes y Titoma.

## 7.4 Tres condiciones sin las cuales no arrancaría

1. **Un socio con oficio en hardware.** En todos los comparables los fundadores venían de la industria. Si no es tu caso, el primer paso es encontrar a esa persona. Candidatos naturales: gente formada en Titoma, Kiwibot o en firmas de EE.UU.
2. **Alguien que venda en EE.UU., en inglés, con red.** Ningún comparable vendió solo desde el país de origen.
3. **Un nicho elegido.** Una familia de tarjetas para un tipo de cliente.

## 7.5 Los supuestos críticos y cómo probarlos barato

Antes de constituir nada. Unas 6 a 8 semanas y menos de US$5k.

| # | Supuesto | Prueba | Señal de avance | Señal de parar |
|---|---|---|---|---|
| 1 | Las startups de EE.UU. comprarían tarjetas a un equipo en Colombia | 15 conversaciones con líderes de hardware de startups de robótica e industrial | 3 o más dicen "mándame una propuesta" | Todos exigen proveedor local |
| 2 | El ciclo físico desde Colombia es tolerable | Pedir componentes de Digi-Key a Colombia, ensamblar una tarjeta real, enviarla a EE.UU. Medir días y costo de cada paso | Menos de 10 días de punta a punta | Más de 3 semanas, o aduana impredecible |
| 3 | Existe el talento senior | Mapear y hablar con 10 ingenieros de hardware con experiencia de exportación | 3 dispuestos a entrar | No hay, o piden salario de EE.UU. |
| 4 | La IA multiplica a un equipo pequeño | Diseñar una tarjeta real con las herramientas abiertas de Diode y un modelo actual. De paso, pedir una cotización en su autoservicio para conocer precio y plazo reales del competidor | Diseño fabricable en días | Requiere tanto retrabajo como hacerlo a mano |
| 5 | Hay un comprador local con urgencia | 10 conversaciones: integradores industriales, CODALTEC, CIAC, operadores de recaudo, operadores de red | 1 dispuesto a pagar un piloto | Solo interés sin presupuesto |

Los supuestos 1 y 2 son los que deciden. Si fallan, la opción A no existe. Si el 2 falla pero el 1 pasa, la respuesta es separar funciones: diseñar en Colombia y ensamblar cerca del cliente.

## 7.6 Qué cambiaría este veredicto

**A mejor:**
- Que EE.UU. elimine el arancel de 12.5% a Colombia (se negocia para diciembre de 2026).
- Que se sancione la ley de electrónica y semiconductores con incentivos reales.
- Que un distribuidor de componentes ponga inventario en una zona franca colombiana.

**A peor:**
- Que la IA resuelva también potencia, radiofrecuencia y depuración en los próximos 12 a 24 meses. El espacio para un estudio de diseño se reduciría a manufactura pura, donde Colombia no tiene ventaja.
- Que se enfríe la financiación de robótica. Hoy es el motor de la demanda accesible.
- Que el peso siga fortaleciéndose.

## 7.7 El riesgo de fondo, dicho sin adornos

La tesis de Asnaghi, en sus palabras: "el puente entre el archivo de diseño y la tarjeta en tu mano es donde está el valor duradero". El diseño se vuelve commodity. Lo que vale es tener datos en vivo de qué componentes se consiguen, qué puede fabricar una planta "en el lugar correcto" y a qué costo, y eso solo se controla fabricando y entregando. Diode construye ese puente en Brooklyn.

Si tiene razón, hay tres consecuencias para Colombia:

1. **El puente depende del lugar.** Colombia no está cerca del cliente de EE.UU. y no tiene cadena de suministro. "Ser Diode en Colombia para EE.UU." es competir en desventaja estructural.
2. **Nadie ha construido ese puente en América Latina.** Si diseñar se vuelve fácil, más empresas de la región van a querer hardware propio y no van a tener quién se lo fabrique rápido. Diode no va a atender a un integrador en Medellín ni a un contratista de defensa en Bogotá. Esa es la versión local de la misma tesis. Su límite es el tamaño de la demanda local, que hoy es pequeña.
3. **Su propio artículo dice dónde falla la IA:** radiofrecuencia, potencia, alta velocidad, y todo lo que hay que medir en un banco. Ahí el conocimiento acumulado pesa más que la cercanía.

Por eso la posición defendible desde aquí es una de dos:

1. Ser el mejor en un nicho técnico de los que la IA todavía no resuelve.
2. Ser el puente para un cliente que Diode no va a atender: la industria, el transporte y la defensa de Colombia y la región.

Lo demás es competir en desventaja.
