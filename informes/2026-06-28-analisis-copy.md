# Análisis de Copy y Comportamiento Conversacional — Junio 2026

> Generado: 2026-06-28
> Base: 21 conversaciones con historial disponible (junio 2026)
> Foco: cómo habla el bot y cómo eso afecta la conversión

---

## Resumen ejecutivo

- **El bot sabe ejecutar el flujo pero no sabe vender.** Cuando el lead ya decidió, el bot lo lleva perfectamente hasta la póliza. Cuando el lead explora o duda, el bot no crea urgencia, no conecta con su situación y cierra puertas en lugar de abrirlas.
- **El saludo inicial es genérico y frío.** "Estimado/a cliente" no personaliza ni engancha. El lead que cotizó ya tiene datos registrados — el bot podría usar el modelo del auto como gancho emocional y no lo hace.
- **El bot presenta demasiadas opciones de golpe.** Hasta 6 combinaciones cobertura/pago en un solo mensaje. Parálisis de decisión documentada: leads que preguntan opciones y no responden cuando se las dan todas.
- **Las señales de urgencia y contexto del lead se ignoran.** "Mi seguro se vence en un mes", "lo ocupo para plataforma", "me dijo Rafa Rebollar que..." — el bot responde igual que a cualquier mensaje genérico.
- **Cuando el lead dice "lo checo y me comunico", el bot lo deja ir.** No refuerza el valor, no crea ningún motivo para volver, no propone un próximo paso concreto.

---

## Hallazgos por patrón

---

### 1. El saludo inicial no engancha

**Mensaje actual (inferido de las 2 conversaciones exitosas con historial):**
> Estimado/a cliente, ¡bienvenido/a!
>
> Ya tengo su cotización para el **NISSAN TIIDA 2011**, con **Cobertura Amplia** y **Pago Anual (Contado)** por **$9,069.00 MXN**.
>
> ¿Desea continuar con esta opción o prefiere ver otras modalidades de pago y coberturas disponibles?

**Variante B:**
> Estimado cliente, ya tengo su cotización para el TOYOTA SIENNA 2027. El sistema le envió la opción de Cobertura Amplia con Pago Anual por $20,365.22 MXN. ¿Desea continuar con esta opción o prefiere revisar otras coberturas y formas de pago?

**Qué falla:**
- "Estimado/a cliente" es lo mismo que empezar con "A quien corresponda". No personaliza.
- "El sistema le envió la opción" suena a un correo automatizado, no a un asesor.
- La pregunta final es abierta y poco orientadora: el lead tiene que decidir entre dos caminos sin saber cuál es mejor para él.
- No hay ningún elemento que conecte emocionalmente con el lead ni que genere urgencia de responder.

**Mensaje sugerido:**
> ¡Hola! Ya tengo lista tu cotización para el **[MODELO AÑO]** 🚗
>
> La opción preseleccionada es **Cobertura Amplia** a **$[PRECIO] MXN al año** — cubre daños propios, robo total, responsabilidad civil y asistencia vial.
>
> ¿Seguimos con esta o prefieres ver otras opciones de pago?

**Por qué funciona mejor:** usa "tu" (tuteo, más directo), nombra el auto, explica en una línea qué cubre la Amplia (el lead sabe qué está comprando), y la pregunta final tiene solo dos opciones claras en lugar de una pregunta abierta.

---

### 2. Las señales de urgencia del lead se ignoran

**Caso documentado (sesión 526694314744, Honda Civic 2012):**

El lead escribió: *"Solo quería cotizar porque el seguro que tengo se vence en un mes"*

El bot respondió:
> Solo puedo ayudarte con la contratación de tu póliza de auto. ¿Seguimos con la contratación?

El lead dijo "Por ahora no gracias" y se fue.

**Qué falla:** El lead acaba de revelar que tiene un deadline real (vencimiento en un mes) y una necesidad activa. El bot lo descartó con una respuesta defensiva que dice explícitamente lo que el bot NO puede hacer. El lead que estaba en modo exploración necesitaba un puente hacia la decisión, no una puerta cerrada.

**Mensaje sugerido:**
> Perfecto, tienes margen para decidir con calma. Ya tengo tu cotización lista — el proceso desde aquí hasta tener la póliza activa toma menos de 10 minutos.
>
> ¿Quieres que te muestre los precios para que puedas comparar? No hay ningún compromiso.

**Por qué funciona mejor:** acknowledge la situación del lead, reduce la presión ("sin compromiso"), y da un dato concreto de tiempo que hace el proceso parecer fácil.

---

### 3. El contexto del lead referido se ignora completamente

**Caso documentado (sesión 525529192606, BYD Song Pro 2026):**

El lead escribió: *"Hola me dijo Rafa Rebollar que si me pueden ayudar con un descuento adicional"*

El bot respondió:
> Estimado/a cliente,
>
> Solo puedo ayudarte con la contratación de tu póliza de auto. ¿Seguimos con la contratación?

El lead dijo "Si" (y continuó, pero la frigidez del inicio pudo haber generado fricción).

**Qué falla:** El lead llegó por referido — señal de alta intención — y con una expectativa específica (descuento). El bot ignoró tanto el referido como la expectativa. No agradeció la referencia, no explicó por qué no hay descuentos adicionales, y no ofreció ningún valor alternativo. Un lead referido merece un trato diferencial en el saludo.

**Mensaje sugerido:**
> ¡Hola! Qué bueno que Rafa te recomendó. Los precios de Quálitas son los mismos para todos (sin descuentos adicionales en este canal), pero te garantizo que son los más competitivos del mercado y el proceso es muy rápido.
>
> Ya tengo tu cotización lista para el **[MODELO]**. ¿Vemos los números?

**Por qué funciona mejor:** acknowledge la referencia (hace sentir especial al lead), gestiona la expectativa del descuento de forma honesta y positiva, y redirige hacia el valor real.

---

### 4. Demasiadas opciones de golpe — parálisis de decisión

**Caso documentado (sesión 525529192606, BYD Song Pro 2026):**

El bot mostró 6 combinaciones en un solo mensaje sin que el lead las pidiera:

> **Cobertura Amplia:**
> • Anual: $20,667.66 MXN
> • Semestral: $21,557.06 MXN (primer pago $11,207.73)
> • Trimestral: $22,042.18 MXN (primer pago $6,154.30)
> • Mensual: $22,365.60 MXN (primer pago $2,650.63)
>
> **Cobertura Limitada:**
> • Anual: $10,092.01 MXN
> • Semestral: $10,506.58 MXN (primer pago $5,682.49)

El lead nunca respondió.

**Qué falla:** el lead tiene que tomar dos decisiones simultáneas (cobertura y forma de pago) sin ninguna recomendación. La diferencia entre la opción más cara ($22,365) y la más barata ($10,092) es del 122% — sin contexto para elegir, el lead se paraliza o va a comparar con otra aseguradora.

**Patrón en conversaciones exitosas:** las dos conversaciones que convirtieron mostraron primero la opción preseleccionada, el lead eligió cobertura, y DESPUÉS eligió forma de pago. Un paso a la vez.

**Mensaje sugerido (cuando el lead pide ver opciones):**
> Claro. Primero dime: ¿prefieres cobertura **Amplia** (cubre daños a tu auto) o **Limitada** (cubre solo responsabilidad y robo total)?
>
> La Amplia para tu [MODELO] cuesta desde **$[PRECIO_MENSUAL]/mes**. La Limitada desde **$[PRECIO_LIMITADA_MENSUAL]/mes**.

**Por qué funciona mejor:** separa la decisión en dos pasos, da solo el dato más relevante (precio mensual), y pide una decisión concreta.

---

### 5. Cuando el lead dice "lo pienso", el bot lo deja ir sin proponer nada

**Caso documentado (sesión 525520080526, Nissan March 2023):**

El lead dijo: *"Gracias lo checo y me comunico"*

El bot respondió:
> Entendido. Quedo a sus órdenes cuando desee continuar.
>
> Si tiene dudas, puede contactar a un agente especializado: https://api.whatsapp.com/send?...
>
> Recuerde que nuestro horario es de 8am - 5pm, Lunes a Viernes.

El lead nunca volvió.

**Qué falla:** el bot no hizo nada para que el lead tenga un motivo concreto para volver. "Quedo a sus órdenes" es la respuesta de alguien que acepta perder al cliente. Además, el link al agente humano en este momento le dice al lead "si tienes dudas, sal de este chat", lo que reduce la probabilidad de que regrese por este canal.

**Mensaje sugerido:**
> ¡Claro, tómate tu tiempo! Tu cotización queda guardada aquí.
>
> Solo un dato antes de que la compares: la Cobertura Limitada del **[MODELO]** a $[PRECIO]/mes incluye RC, robo total y asistencia vial. Si encuentras algo similar más barato, con gusto revisamos.
>
> ¿Cuándo crees que te decides?

**Por qué funciona mejor:** deja al lead con un dato de valor en mente (para la comparación), mantiene la puerta abierta de forma activa, y hace una pregunta de seguimiento que puede generar una fecha de regreso.

---

### 6. La derivación al agente no explica el porqué — corta el engagement

**Caso documentado (sesión 525641445965):**

El lead preguntó sobre Cobertura Amplia y luego dijo: *"Si por favor lo ocupo para plataforma"* (Uber/DiDi).

El bot respondió:
> Para su caso, le recomendamos contactar directamente con un agente especializado que podrá atenderle mejor: https://api.whatsapp.com/send?...

El lead nunca siguió.

**Qué falla:** el lead no entiende por qué lo derivan. ¿Puede o no asegurar su auto para plataforma? ¿Es más caro? ¿Está excluido? La derivación sin explicación genera desconfianza — el lead probablemente interpretó "no podemos asegurarte" y buscó otra aseguradora.

**Mensaje sugerido:**
> Los autos usados en plataformas de transporte (Uber, DiDi) requieren una cobertura especial que no se puede contratar en línea — necesita la intervención de un asesor para configurarla correctamente.
>
> Te conecto con uno ahora: https://api.whatsapp.com/send?phone=525634352430&text=Quiero%20asegurar%20mi%20auto%20para%20plataforma%20-%20cotizacion%20[ID]
>
> Horario: 8am-5pm L-V. ¿Quieres que te explique más sobre qué cubre esa póliza especial?

**Por qué funciona mejor:** explica el porqué de la derivación (el lead entiende que no es un rechazo), preselecciona el mensaje de WhatsApp con el contexto correcto (el agente sabe de qué se trata), y ofrece continuar la conversación.

---

### 7. El bot no responde preguntas concretas de precio aunque tiene los datos

**Caso documentado (sesión 528688314921):**

El lead preguntó: *"Deseo pagar por mes, ¿cómo puedo conseguirlo y el costo?"*

El bot respondió con una explicación genérica sobre el pago mensual y dijo que necesita "completar su cotización con datos del vehículo". Pero el lead ya tenía una cotización activa — el bot no consultó `Get_Quotation_Data`.

El lead insistió: *"Solo cotizar cuanto por mes"*

El bot repitió que necesita los datos del vehículo para dar el costo.

El lead no respondió más.

**Qué falla:** el bot tenía acceso a la cotización del lead (es la razón por la que fue activado) pero no la consultó. En lugar de dar el número concreto que el lead pedía, dio una respuesta evasiva que hizo que el lead pensara que el bot no podía ayudarle.

**Mensaje sugerido (tras consultar Get_Quotation_Data):**
> Tu pago mensual para el **[MODELO]** con Cobertura Amplia sería:
>
> • Primer pago: **$[PRIMER_PAGO] MXN**
> • Los siguientes 11 meses: **$[PAGO_SUBSECUENTE] MXN**
>
> ¿Quieres continuar con esta opción?

**Por qué funciona mejor:** el lead recibe exactamente lo que pidió en el primer mensaje. El bot debe consultar la cotización activa antes de pedir datos que ya tiene.

---

### 8. El primer mensaje de data_capture pide 4 datos sin contexto

**Mensaje actual (presente en todas las conversaciones que llegaron a data_capture):**
> Para continuar con la emisión de su póliza, necesito recopilar algunos datos personales.
>
> **Por favor proporcione:**
> - Su nombre completo (nombre, apellido paterno, apellido materno)
> - Fecha de nacimiento (DD/MM/AAAA)
> - Género (M/F)
> - Número de INE (10 dígitos, opcional)

**Qué falla:** el lead acaba de decir "sí quiero contratar" y el bot le presenta una lista de 4 datos sin decirle cuántos pasos quedan, cuánto tarda el proceso, ni qué pasa cuando los proporcione. La transición entre "quiero contratar" y "dame tus datos" es abrupta.

**En conversaciones exitosas:** el mismo mensaje se usó y los leads respondieron, pero ambas conversaciones exitosas fueron de leads con muy alta intención de compra que no dudaron. Para leads con menor compromiso inicial, este mensaje puede generar abandono.

**Mensaje sugerido:**
> Perfecto. El proceso desde aquí hasta tener tu póliza activa toma unos 5 minutos.
>
> Primero necesito tu nombre completo (nombre y ambos apellidos). ¿Cómo te llamas?

**Por qué funciona mejor:** da un contexto de tiempo (5 minutos hace el proceso parecer manejable), pide solo un dato a la vez, y usa una pregunta conversacional en lugar de una lista.

---

## Recomendaciones priorizadas (copy y comportamiento)

1. **Reescribir el saludo inicial para personalizar y reducir la fricción de la primera pregunta** — Fase: greeting, mensaje de bienvenida. Mensaje actual: _"Estimado/a cliente, ¡bienvenido/a! Ya tengo su cotización para el [MODELO] con Cobertura Amplia y Pago Anual por $X MXN. ¿Desea continuar con esta opción o prefiere ver otras modalidades de pago y coberturas disponibles?"_ Mensaje sugerido: _"¡Hola! Ya tengo lista tu cotización para el [MODELO AÑO]. La opción preseleccionada es Cobertura Amplia a $[PRECIO] MXN al año — cubre daños propios, robo total, RC y asistencia vial. ¿Seguimos con esta o prefieres ver otras opciones de pago?"_ Motivo: 90 leads (57.7%) recibieron este mensaje y no respondieron. Cualquier mejora en respuesta aquí es el mayor palanca de conversión del embudo.

2. **Cambiar el manejo de "lo pienso / lo checo" para dejar al lead con algo concreto y proponer un siguiente paso** — Fase: greeting, respuesta a lead indeciso. Mensaje actual: _"Entendido. Quedo a sus órdenes cuando desee continuar. Si tiene dudas, puede contactar a un agente especializado: [link]."_ Mensaje sugerido: _"¡Claro, tómate tu tiempo! Tu cotización queda guardada aquí. Solo un dato: la [COBERTURA] del [MODELO] a $[PRECIO]/mes incluye [BENEFICIO CLAVE]. Si encuentras algo similar más barato, con gusto revisamos. ¿Cuándo crees que te decides?"_ Motivo: esta respuesta cierra conversaciones que podrían recuperarse. En el período analizado, al menos 6 leads dijeron variantes de "lo pienso" y ninguno volvió.

3. **Separar la elección de cobertura y la de forma de pago en dos preguntas distintas** — Fase: greeting, cuando el lead pide ver opciones o es la primera cotización sin preselección. Mensaje actual: tabla con 6 combinaciones cobertura/pago en un solo mensaje. Mensaje sugerido: primero preguntar _"¿Prefieres cobertura Amplia (daños propios desde $[PRECIO]/mes) o Limitada (solo RC y robo desde $[PRECIO]/mes)?"_ y una vez elegida la cobertura, mostrar las opciones de pago. Motivo: los leads que recibieron 6 opciones de golpe no respondieron; los que convirtieron tomaron las decisiones de una en una.

4. **Cambiar el mensaje de derivación al agente para explicar el porqué y mantener la conversación abierta** — Fase: greeting, nodo de fallback cuando el bot no puede procesar la solicitud. Mensaje actual: _"Para su caso, le recomendamos contactar directamente con un agente especializado que podrá atenderle mejor: [link]"_ Mensaje sugerido: _"[Explicación breve del por qué se necesita agente]. Te conecto con uno ahora: [link con contexto preescrito]. ¿Quieres que te explique más sobre eso antes?"_ Motivo: sin explicación, el lead interpreta la derivación como un rechazo. Con explicación, la derivación es un servicio. Aplica a casos de plataforma, preguntas fuera de scope y situaciones especiales.

5. **Reescribir la entrada a data_capture: un dato a la vez, con contexto de tiempo y proceso** — Fase: data_capture, primer mensaje. Mensaje actual: lista de 4 datos (nombre, fecha, género, INE) en un bloque. Mensaje sugerido: _"Perfecto. El proceso desde aquí hasta tener tu póliza activa toma unos 5 minutos. Primero, ¿cómo te llamas? (nombre y ambos apellidos)"_ Una vez respondido, pedir fecha de nacimiento, luego género, luego INE. Motivo: la sesión 573107696237 (Honda Civic) llegó a data_capture, recibió la lista de 4 datos, y nunca respondió. Pedir de uno en uno reduce la fricción del inicio.

_(Máximo 5 recomendaciones, ordenadas de mayor a menor impacto estimado)_
