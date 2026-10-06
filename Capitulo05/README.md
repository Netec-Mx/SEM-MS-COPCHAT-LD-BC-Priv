# Práctica guiada 4. Caso final: convertir el análisis acumulado en una recomendación ejecutiva, justificarla, identificar riesgos y preparar preguntas de seguimiento

## Metadatos

| Campo | Valor |
|---|---|
| Duración | 40 minutos |
| Complejidad | Difícil |
| Nivel de Bloom | Crear |
| Aplicación principal | Microsoft 365 Copilot Chat |
| Insumo | Page acumulativa con resumen, brief y matriz comparativa |
| Entregable | Recomendación ejecutiva final y Page consolidada del caso |

## Descripción General

El comité ya dispone del resumen inicial, el brief refinado de NexoSolar y una comparación estructurada frente a GridFlex. Ahora solicita un entregable final: una **recomendación ejecutiva provisional**, sustentada en la evidencia acumulada y acompañada de riesgos, condiciones y preguntas de seguimiento.

> [!IMPORTANT]
> No recibirás datos nuevos. La práctica final consiste en aprovechar correctamente lo que ya construiste, diseñar un prompt que obligue a Copilot a justificar su conclusión y comprobar que la recomendación no supera la evidencia disponible.

## Objetivos de Aprendizaje

- [ ] Integrar resultados de prácticas anteriores en una solicitud final coherente.
- [ ] Construir un prompt de recomendación con criterios, límites y trazabilidad.
- [ ] Diferenciar recomendación provisional de decisión financiera definitiva.
- [ ] Identificar riesgos, condiciones que podrían cambiar la conclusión y preguntas de seguimiento.
- [ ] Comparar el prompt propio y la salida obtenida con referencias completas.
- [ ] Consolidar la Copilot Page como producto final del caso.

## Prerrequisitos

### Conocimientos requeridos

- Construcción y refinamiento de prompts.
- Diferenciación entre hechos, inferencias, supuestos y datos faltantes.
- Uso de criterios de comparación y restricciones de salida.

### Acceso y artefactos requeridos

- Copilot Chat habilitado.
- Page `Caso de inversión — NexoSolar vs. GridFlex` con:
  - sección 1: resumen inicial de NexoSolar;
  - sección 2: brief refinado;
  - sección 3: matriz comparativa y preguntas pendientes.

> [!NOTE]
> No se requieren archivos externos.

## Entorno de Laboratorio

### Hardware mínimo y recomendado

Equipo con conexión estable a Internet y acceso a Microsoft 365 Copilot Chat.

### Software y servicios

| Tecnología | Uso |
|---|---|
| Microsoft 365 Copilot Chat | Construcción, ejecución y refinamiento del prompt final |
| Copilot Pages | Fuente acumulativa y entregable final |

### Preparación del espacio de trabajo

1. Abre la Page acumulativa.
2. Recorre las tres secciones existentes antes de redactar el prompt final.
3. Abre un chat nuevo para evitar que contexto no controlado influya en el resultado.
4. Utiliza únicamente la información contenida en la Page y los datos originales de las prácticas.

## Distribución de tiempo

| Fase | Actividad | Tiempo |
|---|---|---:|
| 1 | Revisar la evidencia acumulada | 5 min |
| 2 | Diseñar criterios y construir el prompt de recomendación | 8 min |
| 3 | Ejecutar y revisar la recomendación provisional | 7 min |
| 4 | Comparar con el prompt sugerido | 5 min |
| 5 | Comparar con el resultado esperado | 6 min |
| 6 | Refinar y realizar control de calidad | 5 min |
| 7 | Consolidar la Page final | 4 min |
| **TOTAL** |  | **40 min** |

## Instrucciones Paso a Paso

### Paso 1: Revisar qué evidencia existe realmente

> [!NOTE]
> **Objetivo:** evitar que la recomendación se base en información que apareció solo como inferencia o como dato faltante.

Recorre la Page y separa mentalmente:

- hechos de NexoSolar;
- hechos de GridFlex;
- cálculos directos condicionados;
- riesgos;
- supuestos;
- datos no disponibles;
- preguntas pendientes.

> [!IMPORTANT]
> **Por qué este paso importa:** una recomendación sólida no depende de que Copilot “razone mejor”, sino de que utilice evidencia claramente delimitada y reconozca los vacíos que podrían cambiar la decisión.

#### Ejemplo para orientarte

Antes de pensar en cuál alternativa parece mejor, revisa cómo está clasificada la información.

**Por ejemplo:**

- USD 2.4 millones de inversión inicial para NexoSolar es un hecho proporcionado.
- USD 120,000 anuales potenciales para GridFlex también proviene del caso, pero es un hecho condicionado, porque depende de contratos.
- GridFlex podría requerir menor desembolso inicial es una comparación derivada de hechos.
- GridFlex será más rentable no está respaldado, porque faltan variables para demostrarlo.
- NexoSolar podría retrasarse entre 3 y 6 meses por permisos es un riesgo conocido, no una confirmación de que el retraso ocurrirá.

Puedes hacer una revisión mental con esta pregunta:

> “¿Podría señalar exactamente de qué parte de la Page sale esta afirmación?”

> [!IMPORTANT]
> Si no puedes hacerlo, esa afirmación no debería utilizarse como base de la recomendación final.

---

### Paso 2: Definir qué tipo de recomendación puede emitir Copilot

El comité permite tres salidas legítimas:

1. Priorizar NexoSolar para una fase posterior de validación.
2. Priorizar GridFlex para una fase posterior de validación.
3. Aplazar la priorización hasta validar información crítica.

> [!IMPORTANT]
> Ninguna de estas opciones equivale a autorizar una inversión real.

Tu prompt debe obligar a Copilot a justificar la opción seleccionada y a indicar **qué evidencia respalda la conclusión y qué información podría modificarla**.

#### Cómo pensar las tres opciones

No necesitas escoger una alternativa antes de ejecutar el prompt. Define primero qué significaría cada resultado.

##### Ejemplo de priorización razonable:

“Priorizar una alternativa” no significa aprobarla. Significa que, con la evidencia disponible, parece tener mejores condiciones para pasar primero a una fase adicional de validación.

##### Ejemplo de aplazamiento razonable:

Si una conclusión depende de datos financieros, técnicos o contractuales que todavía no existen, aplazar puede ser una respuesta mejor fundamentada que forzar una selección.

**Una forma útil de plantearte la decisión es:**

- ¿Existe evidencia suficiente para distinguir claramente una alternativa?
- ¿La diferencia observada depende de datos confirmados o de condiciones pendientes?
- ¿Un solo dato faltante importante podría cambiar la conclusión?

> [!IMPORTANT]
> Si la respuesta a la última pregunta es sí, considera que la opción de aplazar puede ser legítima.

---

### Paso 3: Diseñar la estructura de la recomendación

**Construye instrucciones para que la respuesta final contenga:**

1. Decisión provisional.
2. Tesis ejecutiva.
3. Evidencia que respalda la decisión.
4. Riesgos principales.
5. Datos pendientes críticos.
6. Condiciones para avanzar.
7. Preguntas de seguimiento.
8. Limitaciones del análisis.

**Incluye además estas restricciones:**

- no inventar nueva información;
- no presentar ingresos condicionados como garantizados;
- no calcular métricas financieras no disponibles;
- no afirmar cumplimiento regulatorio o contractual;
- no ocultar contradicciones o vacíos;
- si la evidencia no permite priorizar con suficiente fundamento, seleccionar la opción de aplazar.

#### Ideas para empezar a construir el prompt final

No intentes redactar todo de una sola vez. Puedes armarlo por bloques.

##### 1. Define el contexto

Una forma de iniciar podría ser:

> “Debes preparar una recomendación ejecutiva provisional para un comité que está comparando NexoSolar y GridFlex.”

##### 2. Inserta la evidencia

Puedes introducirla con una instrucción como:

> “Utiliza únicamente el brief refinado y la matriz comparativa que aparecen a continuación como fuente autorizada.”

##### 3. Define la decisión que Copilot debe tomar

**Por ejemplo:**

> “Selecciona una de tres opciones: priorizar NexoSolar, priorizar GridFlex o aplazar la priorización.”

##### 4. Obliga a justificar

Algunas ideas:

> “Vincula cada argumento a una evidencia concreta.”

> “Indica qué información podría cambiar la conclusión.”

> “Separa los hechos de los datos pendientes.”

##### 5. Define la estructura

Puedes pedir, por ejemplo:

> “Presenta primero la decisión, luego la tesis, la evidencia, los riesgos, los datos pendientes y las preguntas de seguimiento.”

##### 6. Agrega límites

**Por ejemplo:**

> “No calcules métricas financieras no soportadas.”

> “No conviertas ingresos potenciales en ingresos garantizados.”

> “Si la evidencia es insuficiente, no fuerces una priorización.”

> [!NOTE]
> Estas frases son pistas de construcción, no el prompt final. Selecciona y adapta únicamente las que necesites.

---

### Paso 4: Construir y ejecutar tu prompt final

1. Copia desde la Page únicamente el contenido validado de las secciones 2 y 3, o resume fielmente la evidencia esencial.
2. Incorpóralo como fuente dentro de tu prompt.
3. Añade la tarea, formato y restricciones definidos en los pasos anteriores.
4. Envía el prompt.
5. Revisa la salida antes de aceptarla.

#### Preguntas de control:

- ¿La recomendación se apoya en datos realmente disponibles?
- ¿Explica por qué una alternativa podría priorizarse o por qué conviene aplazar?
- ¿Reconoce que NexoSolar tiene mayor inversión inicial y mayor ahorro anual estimado?
- ¿Reconoce que GridFlex tiene menor inversión inicial, menor ahorro base y un ingreso adicional condicionado?
- ¿Evita afirmar rentabilidad definitiva?
- ¿Identifica qué datos podrían cambiar la recomendación?

#### Ejemplos de revisión después de ejecutar

**Si Copilot responde:**

> “GridFlex es la mejor alternativa porque requiere menor inversión.”

La justificación es insuficiente. Una menor inversión inicial es un dato relevante, pero no demuestra por sí sola que sea la mejor opción.

**Podrías refinar con:**

> “No utilices un único criterio para priorizar. Contrasta inversión, beneficios estimados, riesgos, dependencias y vacíos críticos antes de emitir la decisión provisional.”

**Si Copilot afirma:**

> “NexoSolar generará USD 300,000 adicionales gracias al incentivo.”

Debes corregirlo, porque el incentivo está sujeto a aprobación.

**Una instrucción posible sería:**

> “Revisa todos los beneficios adicionales y distingue cuáles están confirmados y cuáles son condicionados. No incorpores como garantizado ningún valor sujeto a aprobación o contrato.”

**Si la recomendación no muestra qué podría cambiarla:**

> “Añade una sección donde indiques qué datos pendientes podrían modificar la decisión provisional y explica brevemente por qué.”

> [!IMPORTANT]
> El objetivo es corregir el problema concreto, no pedir genéricamente “hazlo mejor”.

---

### Paso 5: Comparar con el prompt sugerido

<details>

<summary><strong>PROMPT SUGERIDO DE REFERENCIA — abrir después de ejecutar tu versión</strong></summary>

```text

Actúa como asistente de análisis para preparar una recomendación ejecutiva provisional sobre dos alternativas ficticias: NexoSolar y GridFlex.

Audiencia: comité ejecutivo interno.

Horizonte de evaluación: 5 años.

Usa exclusivamente la evidencia validada incluida a continuación. No incorpores conocimiento externo ni datos nuevos.

EVIDENCIA VALIDADA

[Inserta aquí el brief refinado de NexoSolar y la matriz comparativa validada de la Copilot Page]

Tarea:

Emite una recomendación ejecutiva provisional seleccionando una de estas opciones:

1. Priorizar NexoSolar para una fase posterior de validación.
2. Priorizar GridFlex para una fase posterior de validación.
3. Aplazar la priorización hasta validar información crítica.

Formato obligatorio:

1. Decisión provisional: una sola opción de las tres anteriores.
2. Tesis ejecutiva: máximo 120 palabras.
3. Evidencia que respalda la decisión: tabla con “Evidencia”, “Alternativa”, “Implicación” y “Nivel de confianza” (Alto, Medio o Bajo según la calidad de la evidencia disponible).
4. Riesgos principales: máximo 4 por alternativa.
5. Datos pendientes críticos: máximo 6, priorizados.
6. Condiciones para avanzar: acciones concretas que deberían completarse antes de una decisión definitiva.
7. Preguntas de seguimiento para el comité: entre 4 y 6 preguntas.
8. Limitaciones del análisis.

Reglas:

- No inventes cifras, contratos, proveedores, permisos, tarifas, garantías ni condiciones.
- No calcules VAN, TIR, ROI o periodo de recuperación si no existen variables suficientes.
- No presentes incentivos o ingresos condicionados como garantizados.
- Diferencia hechos de inferencias y datos pendientes.
- Si los vacíos de información impiden justificar razonablemente una priorización, selecciona “Aplazar la priorización”.
- No presentes la salida como asesoramiento financiero, legal, fiscal o de inversión real.
- Indica explícitamente qué información podría cambiar la recomendación provisional.

```

</details>

> [!NOTE]
> Tu prompt no necesita ser idéntico. Debe lograr un resultado igualmente controlado, trazable y útil.

#### Cómo comparar tu prompt con la referencia

No reemplaces automáticamente tu versión por el prompt sugerido. Revísalos por componentes.

**Por ejemplo:**

- Si tu prompt ya limita las opciones a las tres decisiones permitidas, ese elemento está cubierto.
- Si pide justificar la recomendación pero no exige señalar qué evidencia respalda cada argumento, ahí existe una oportunidad de mejora.
- Si tu versión incluye riesgos y datos pendientes, pero no solicita condiciones para avanzar, puedes agregar solo ese bloque.
- Si tu estructura es más corta pero produce una salida clara, trazable y completa, puede ser igualmente válida.
- Si tu prompt fuerza una alternativa ganadora aun cuando la evidencia sea insuficiente, debes corregirlo.

Una conclusión útil de la comparación podría ser:

> “Mantendré mi estructura, pero agregaré una regla para aplazar la priorización cuando los vacíos críticos impidan justificar una elección.”

> [!NOTE]
> La comparación sirve para refinar tu diseño, no para copiar la solución de referencia.

---

### Paso 6: Comparar con un resultado esperado de referencia

<details>

<summary><strong>RESULTADO ESPERADO DE REFERENCIA — abrir después de revisar tu recomendación</strong></summary>

#### 1. Decisión provisional

**Aplazar la priorización hasta validar información crítica.**

#### 2. Tesis ejecutiva

NexoSolar y GridFlex muestran perfiles diferentes de inversión, ahorro y riesgo, pero la información disponible no permite una selección financiera concluyente. NexoSolar requiere mayor inversión inicial y ofrece mayor ahorro anual estimado; GridFlex requiere menor inversión y añade un ingreso potencial condicionado. Sin embargo, faltan variables técnicas, financieras y contractuales críticas en ambas alternativas. La decisión debería avanzar primero a una fase de validación enfocada en los vacíos que pueden modificar materialmente la comparación.

#### 3. Evidencia que respalda la decisión

| Evidencia | Alternativa | Implicación | Nivel de confianza |
|---|---|---|---|
| Inversión inicial USD 2.4 M | NexoSolar | Mayor desembolso inicial | Alto |
| Ahorro anual estimado USD 720,000 | NexoSolar | Mayor ahorro nominal estimado | Alto |
| Permisos podrían retrasar 3–6 meses | NexoSolar | Riesgo de calendario | Alto |
| Inversión inicial USD 1.8 M | GridFlex | Menor desembolso inicial | Alto |
| Ahorro anual estimado USD 560,000 | GridFlex | Menor ahorro base que NexoSolar | Alto |
| Ingreso potencial USD 120,000/año sujeto a contratos | GridFlex | Puede mejorar el caso, pero no está garantizado | Alto sobre la condición; bajo sobre su materialización |

#### 4. Riesgos principales

**NexoSolar**

- Permisos y posible retraso de 3–6 meses.
- Costo de financiamiento no disponible.
- Degradación técnica no evaluada.
- Incentivo fiscal sujeto a aprobación.

**GridFlex**

- Integración con sistemas existentes.
- Vida útil y garantías de baterías no disponibles.
- Ingreso de respuesta a la demanda sujeto a contratos.
- Tarifas, proveedores y penalizaciones contractuales no disponibles.

#### 5. Datos pendientes críticos

1. Costo y estructura de financiamiento de NexoSolar — **Alta**.
2. Estado y calendario de permisos de NexoSolar — **Alta**.
3. Condiciones contractuales de ambas alternativas — **Alta**.
4. Vida útil y garantías de baterías de GridFlex — **Alta**.
5. Tasa de descuento aplicable al análisis financiero — **Alta**.
6. Degradación esperada de paneles de NexoSolar — **Media**.

#### 6. Condiciones para avanzar

- Validar permisos, condiciones contractuales y variables financieras de NexoSolar.
- Confirmar garantías, vida útil, tarifas e ingreso contractual de GridFlex.
- Definir una metodología financiera común para ambas alternativas.
- Actualizar la comparación una vez estén disponibles los datos críticos.

#### 7. Preguntas de seguimiento

1. ¿Cuál es el costo y la estructura de financiamiento aplicable a cada alternativa?
2. ¿Qué permisos faltan en NexoSolar y cuál es el calendario probable?
3. ¿Qué contratos soportarían los USD 120,000 anuales potenciales de GridFlex?
4. ¿Qué garantías y vida útil ofrecen las baterías?
5. ¿Qué condiciones contractuales podrían modificar costos o beneficios?
6. ¿Qué tasa de descuento utilizará el comité para una evaluación financiera común?

#### 8. Limitaciones

La recomendación es provisional y se basa únicamente en los datos ficticios proporcionados. No incorpora valoración financiera completa, contratos, validación legal, análisis técnico detallado ni información externa.

</details>

> [!NOTE]
> Este es un ejemplo completo, no una respuesta única. Si tu salida prioriza una alternativa, debe justificarlo con la evidencia disponible y reconocer explícitamente qué incertidumbres podrían cambiar esa priorización.

#### Cómo utilizar el resultado esperado de referencia

No compares palabra por palabra. Evalúa si tu salida cumple la misma función.

**Busca especialmente:**

- Decisión provisional: debe ser una de las tres opciones permitidas.
- Tesis: debe explicar el razonamiento principal sin aparentar una decisión definitiva.
- Evidencia: cada argumento debería poder rastrearse a la Page.
- Nivel de confianza: no debería confundirse “dato disponible” con “resultado garantizado”.
- Riesgos: deben existir para ambas alternativas.
- Datos pendientes: deben centrarse en información que realmente pueda alterar la comparación.
- Condiciones para avanzar: deberían convertir los vacíos en acciones concretas de validación.
- Preguntas de seguimiento: deben surgir de necesidades reales del caso, no de curiosidad general.

Por ejemplo, si tu recomendación también concluye que conviene aplazar, pero organiza la evidencia de otra manera y llega a esa conclusión utilizando correctamente los datos, puede ser perfectamente válida.

Si tu salida prioriza NexoSolar o GridFlex, revisa con mayor cuidado si la diferencia está realmente respaldada y si reconoces qué información pendiente podría cambiarla.

---

### Paso 7: Ejecutar un control de calidad final

**Revisa tu respuesta contra estas preguntas:**

1. ¿Cada cifra puede rastrearse al caso original o a un cálculo directo mostrado?
2. ¿Alguna inferencia se presenta como hecho?
3. ¿Algún ingreso condicionado aparece como garantizado?
4. ¿Se ocultó algún dato faltante importante?
5. ¿La recomendación es provisional y no una autorización de inversión?
6. ¿Las preguntas de seguimiento están vinculadas a vacíos reales del caso?

Si detectas un problema, realiza una última iteración con una instrucción precisa.

#### Ejemplos de correcciones específicas antes del cierre

**Si detectas exceso de certeza:**

> “Reformula la conclusión para que quede explícitamente como recomendación provisional y señala los datos que todavía deben validarse.”

**Si falta trazabilidad:**

> “Para cada argumento de la recomendación, indica qué dato o condición del caso lo respalda.”

**Si una alternativa parece favorecida por un ingreso condicionado:**

> “Reevalúa la comparación sin tratar incentivos ni ingresos potenciales como garantizados. Conserva visibles sus condiciones.”

**Si las preguntas de seguimiento son genéricas:**

> “Sustituye las preguntas generales por preguntas vinculadas directamente a permisos, financiamiento, contratos, garantías, vida útil o tarifas que siguen sin resolverse.”

#### Ejemplo de instrucción integral de revisión:

```text

Revisa la recomendación anterior únicamente contra la evidencia suministrada. Corrige cualquier afirmación no respaldada, vuelve a etiquetar como condicionado todo ingreso o incentivo no confirmado y conserva visibles los datos pendientes que podrían cambiar la decisión. No agregues información nueva.

```

---

### Paso 8: Consolidar la Copilot Page final

**Agrega la sección final:**

```text

## 4. Recomendación ejecutiva final

### Prompt final

[Tu prompt de recomendación validado]

### Decisión provisional y justificación

[La mejor respuesta obtenida]

### Riesgos y condiciones para avanzar

[Contenido validado]

### Preguntas de seguimiento

[Contenido validado]

```

**La Page final debe conservar las cuatro secciones:**

1. Resumen ejecutivo inicial — NexoSolar.
2. Brief ejecutivo refinado — NexoSolar.
3. Comparación ejecutiva — NexoSolar vs. GridFlex.
4. Recomendación ejecutiva final.

#### Ejemplo de cómo debería leerse la historia completa en la Page

No copies este contenido como solución. Úsalo para comprobar la continuidad:

##### 1. Resumen ejecutivo inicial — NexoSolar

¿Qué es la oportunidad y qué información básica existe?

##### 2. Brief ejecutivo refinado — NexoSolar

¿Qué sabemos, qué inferimos, qué riesgos existen y qué falta validar?

##### 3. Comparación ejecutiva — NexoSolar vs. GridFlex

¿Cómo se comparan ambas alternativas bajo criterios comunes?

##### 4. Recomendación ejecutiva final

¿Qué puede recomendarse provisionalmente con la evidencia actual?

¿Qué podría cambiar esa recomendación?

¿Qué debe validarse antes de una decisión definitiva?

Al finalizar, otra persona debería poder recorrer la Page de arriba abajo y entender cómo evolucionó el razonamiento, no solo cuál fue la conclusión final.

## Validación y Pruebas

| # | Criterio | Estado |
|---|---|---|
| 1 | La recomendación utiliza únicamente evidencia del caso | ☐ |
| 2 | La decisión se identifica como provisional | ☐ |
| 3 | Los riesgos de ambas alternativas están presentes | ☐ |
| 4 | Los datos pendientes críticos están priorizados | ☐ |
| 5 | No se presentan ingresos condicionados como garantizados | ☐ |
| 6 | No existen métricas financieras inventadas | ☐ |
| 7 | Existen condiciones concretas para avanzar | ☐ |
| 8 | Existen entre 4 y 6 preguntas de seguimiento | ☐ |
| 9 | La Page contiene las cuatro secciones del proceso | ☐ |
| 10 | Los prompts finales de cada práctica permanecen visibles como evidencia | ☐ |

### Criterio de aceptación final

> [!NOTE]
> La práctica se considera terminada cuando otra persona puede abrir la Page y comprender, en orden, cómo evolucionó el caso desde un resumen inicial hasta una recomendación provisional, qué evidencia sustenta cada etapa y qué información sigue pendiente.

## Solución de Problemas

### Problema 1: Copilot selecciona una alternativa sin justificarla

Añade una tabla de evidencia obligatoria y exige que cada argumento se vincule a un dato del caso.

### Problema 2: La respuesta presenta certeza excesiva

Incluye la regla: “Si la evidencia es insuficiente para una priorización razonable, selecciona aplazar la priorización”.

### Problema 3: Aparecen métricas o condiciones nuevas

Solicita una revisión estricta contra la evidencia y elimina cualquier dato que no pueda rastrearse a la Page.

## Limpieza

- Conserva la Page final como único entregable acumulativo del caso.
- No crees bitácoras ni archivos adicionales.
- Puedes cerrar chats intermedios después de confirmar que los prompts finales y los resultados validados están en la Page.
- No reutilices los datos ficticios como si correspondieran a una situación real.

## Resumen

Completaste un flujo consecutivo de prompting: construiste un prompt base, lo refinaste, ampliaste el caso a una comparación y finalmente generaste una recomendación ejecutiva provisional. La Page final evidencia tanto los prompts construidos como los resultados validados y permite comparar la evolución del proceso de principio a fin.
