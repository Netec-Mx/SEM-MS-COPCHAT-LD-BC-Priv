# Práctica guiada 3. Ampliar el caso comparando dos alternativas de inversión y construir una matriz ejecutiva de criterios, riesgos y preguntas pendientes

## Metadatos

| Campo | Valor |
|---|---|
| Duración | 25 minutos |
| Complejidad | Media |
| Nivel de Bloom | Crear |
| Aplicación principal | Microsoft 365 Copilot Chat |
| Insumo | Brief refinado de NexoSolar en la Page + caso ficticio GridFlex incluido en esta guía |
| Entregable | Matriz ejecutiva comparativa incorporada a la misma Page |

## Descripción General

El comité decide que NexoSolar no debe evaluarse de forma aislada. Existe una segunda alternativa, **GridFlex**, y se necesita una comparación estructurada antes de formular cualquier recomendación.

En esta práctica aprenderás a convertir dos conjuntos de información diferentes en un prompt de comparación **simétrico y verificable**. La guía te ayudará a definir criterios, controlar los vacíos de información y evitar que Copilot complete diferencias con datos inventados. Después compararás tu solución con un prompt sugerido y una matriz de referencia.

## Objetivos de Aprendizaje

- [ ] Ampliar un caso existente incorporando una segunda alternativa.

- [ ] Definir criterios de comparación que puedan aplicarse a ambas alternativas.

- [ ] Construir un prompt que diferencie hechos, inferencias y datos no disponibles.

- [ ] Obtener una matriz ejecutiva de criterios, riesgos y preguntas pendientes.

- [ ] Validar cálculos directos y evitar métricas financieras no soportadas.

- [ ] Incorporar la comparación en la Page acumulativa.

## Prerrequisitos

- Haber completado la práctica guiada 2.

- Tener disponible en la Page el brief validado de NexoSolar.

- Trabajar con el mismo conjunto de datos de NexoSolar definido desde la práctica 1.

- No utilizar navegación web ni información real para completar los datos faltantes.

## Entorno de Laboratorio

### Recursos de hardware

Equipo con conexión estable a Internet y acceso a Copilot Chat.

### Software y servicios

| Tecnología | Uso |
|---|---|
| Microsoft 365 Copilot Chat | Construcción y ejecución del prompt comparativo |
| Copilot Pages | Consulta del brief de NexoSolar y consolidación de la matriz |

### Alcance de licencias y herramientas

No se requieren hojas de cálculo ni archivos intermedios. La tabla comparativa se genera y conserva dentro de la Page.

### Preparación del espacio de trabajo

1. Abre la Page `Caso de inversión — NexoSolar vs. GridFlex`.

2. Localiza el brief validado de NexoSolar.

3. Abre una conversación nueva de Copilot Chat o continúa una conversación en la que puedas proporcionar el brief completo.

## Distribución de tiempo

| Fase | Actividad | Tiempo |
|---|---|---:|
| 1 | Analizar GridFlex y definir criterios comunes | 4 min |
| 2 | Construir el prompt comparativo | 6 min |
| 3 | Ejecutar y revisar la matriz | 5 min |
| 4 | Comparar con el prompt sugerido | 4 min |
| 5 | Comparar con el resultado esperado y refinar | 4 min |
| 6 | Actualizar la Page | 2 min |
| **TOTAL** |  | **25 min** |

## Instrucciones Paso a Paso

### Paso 1: Incorporar la segunda alternativa al storytelling

> [!NOTE]
> **Situación:** el comité considera una alternativa tecnológica distinta para los mismos fines de reducción y gestión de costos energéticos.

#### Alternativa B — GridFlex:

| Elemento | Información proporcionada |
|---|---|
| Inversión inicial estimada | USD 1.8 millones |
| Alcance | Almacenamiento energético y software de gestión de demanda en 8 centros logísticos |
| Horizonte de evaluación | 5 años |
| Ahorro anual estimado | USD 560,000 |
| Costo anual de operación | USD 150,000 |
| Ingreso potencial | USD 120,000 anuales por programas de respuesta a la demanda, sujeto a contratos |
| Dependencia principal | Integración con sistemas existentes |
| Información no disponible | Vida útil de baterías, garantías, tarifas aplicables, disponibilidad de proveedores y penalizaciones contractuales |

> [!NOTE]
> **Por qué este paso importa:** una comparación útil exige conocer no solo los datos de cada alternativa, sino también dónde la información es equivalente y dónde existen vacíos que impiden comparar directamente.

### Ejemplo para ubicar qué puedes comparar

Antes de pensar en el prompt, observa los datos como si prepararas una mesa de comparación. Algunas relaciones son directas y otras solo son parcialmente comparables.

Por ejemplo:
- Inversión inicial: sí puede compararse directamente: NexoSolar = USD 2.4 millones y GridFlex = USD 1.8 millones.
- Horizonte: también es comparable: ambas alternativas utilizan 5 años.
- Beneficio adicional: NexoSolar tiene un incentivo potencial único y GridFlex un ingreso anual potencial sujeto a contratos. Ambos son datos condicionados, pero no representan exactamente el mismo tipo de beneficio.
- Dependencias: NexoSolar depende de permisos y GridFlex de integración con sistemas existentes. Pueden compararse como dependencias de ejecución, pero no deben tratarse como riesgos idénticos.
- Datos técnicos faltantes: NexoSolar no tiene información de degradación de paneles y GridFlex no tiene vida útil ni garantías de baterías. Aquí la comparación correcta es reconocer que ambas alternativas tienen vacíos técnicos diferentes.

Puedes empezar pensando:

> “¿Qué datos tengo para las dos alternativas, cuáles solo existen para una y cuáles deberían marcarse como no disponibles?”

No necesitas escribir esta reflexión en la Page. Úsala para entender qué debe pedir tu prompt.

---

### Paso 2: Definir criterios simétricos de comparación

Antes de redactar el prompt, observa el brief de NexoSolar y los datos de GridFlex. Decide qué criterios pueden revisarse para ambas alternativas.

La guía propone estos diez criterios mínimos:

1. Inversión inicial.

2. Beneficios o ahorros estimados.

3. Costos operativos estimados.

4. Horizonte de evaluación.

5. Dependencias externas.

6. Complejidad de implementación.

7. Riesgos identificados.

8. Supuestos críticos.

9. Evidencia disponible.

10. Preguntas pendientes.

> [!NOTE]
> **Por qué este paso importa:** si pides “compara NexoSolar y GridFlex” sin criterios, Copilot puede priorizar atributos distintos para cada opción o introducir supuestos que hagan parecer más completa una alternativa.

### Ejemplo para convertir un criterio en una comparación útil

Un criterio demasiado general puede producir respuestas ambiguas. Conviene pensar qué pregunta concreta quieres que responda cada fila.

Ejemplos:
- Inversión inicial → “¿Cuánto capital inicial requiere cada alternativa?”
- Costos operativos → “¿Qué costo anual estimado se ha proporcionado para cada opción?”
- Dependencias externas → “¿Qué condición externa puede afectar la ejecución de cada alternativa?”
- Evidencia disponible → “¿El dato es un hecho proporcionado, una inferencia, un cálculo derivado o no está disponible?”
- Preguntas pendientes → “¿Qué información falta antes de poder comparar con mayor confianza?”

> [!WARNING]
> Ten especial cuidado con Complejidad de implementación. El caso no proporciona una puntuación o nivel de complejidad para ninguna alternativa. No sería correcto concluir, por ejemplo, que GridFlex es más simple solo porque cubre 8 centros en lugar de 12. Una salida válida podría ser:

> “Complejidad de implementación: no disponible. NexoSolar presenta dependencia de permisos y GridFlex dependencia de integración, pero la información no permite afirmar cuál es más compleja.”

Esta lógica te ayudará a pedir una comparación simétrica sin rellenar vacíos con suposiciones.

---

### Paso 3: Construir tu prompt comparativo

Tu prompt debe incluir:
- el brief validado de NexoSolar o, si prefieres reducir contexto, los hechos esenciales extraídos de ese brief;
- todos los datos de GridFlex;
- los criterios de comparación;
- una regla explícita para usar `no disponible` cuando falte información;
- una prohibición de recomendar una alternativa de manera definitiva;
- una solicitud de preguntas pendientes priorizadas.

Además, decide cómo quieres que Copilot identifique el tipo de información. Una forma útil es clasificar cada campo como:
- hecho proporcionado;
- inferencia limitada;
- cálculo derivado;
- no disponible.

> [!IMPORTANT]
> No envíes todavía el prompt hasta confirmar que las dos alternativas tienen el mismo horizonte de 5 años.

### Ideas para empezar a construir tu prompt comparativo

No necesitas redactar todo de una vez. Puedes construirlo por bloques y luego unirlos.

#### 1. Sitúa a Copilot en el objetivo

   Puedes iniciar con una idea como:

> “Necesito comparar dos alternativas de inversión ficticias para preparar información dirigida a un comité ejecutivo.”

#### 2. Proporciona las dos fuentes

   Incluye primero la información validada de NexoSolar y después los datos completos de GridFlex. Puedes introducirlas como:

> “Fuente A — NexoSolar...”

> “Fuente B — GridFlex...”

#### 3. Explica qué significa comparar

   Algunas frases que pueden ayudarte:

> “Aplica los mismos criterios a ambas alternativas.”

> “Cuando un criterio no tenga evidencia suficiente, indícalo como no disponible.”

> “No sustituyas un dato faltante por una inferencia.”

#### 4. Define la salida

   Puedes pedir una estructura como:

> “Organiza la comparación en una tabla donde cada fila corresponda a un criterio.”

> “Después de la tabla identifica riesgos, supuestos y preguntas pendientes.”

#### 5. Controla la conclusión

   En esta práctica todavía no buscas una alternativa ganadora. Una restricción útil sería:

> “No emitas una recomendación final; limita la respuesta a organizar evidencia, diferencias y vacíos.”

Estas frases son ejemplos parciales. Adáptalas y combínalas con tu propio prompt. El objetivo es que tu versión represente la necesidad del comité y los datos reales del caso.

---

### Paso 4: Ejecutar y revisar la matriz

1. Envía tu prompt.

2. Revisa que aparezcan las dos alternativas.

3. Comprueba manualmente todas las cifras.

4. Si Copilot realiza un cálculo directo, valida la operación antes de aceptarla.

Para GridFlex, un ejemplo de cálculo aritmético permitido es:
```text
Ahorro anual estimado + ingreso potencial condicionado - costo anual de operación

= 560,000 + 120,000 - 150,000

= USD 530,000
```

Si aparece, debe identificarse como **cálculo derivado condicionado**, porque los USD 120,000 dependen de contratos.

> [!WARNING]
> No aceptes cálculos de VAN, TIR, ROI o periodo de recuperación: faltan variables necesarias.

### Ejemplos para revisar la matriz sin perderte

Cuando recibas la respuesta, revisa primero unas pocas filas críticas antes de leer todo el análisis.

#### Ejemplo 1 — inversión inicial

   Una fila coherente podría indicar:

   NexoSolar: USD 2.4 millones | GridFlex: USD 1.8 millones | Tipo: hecho proporcionado.

> [!WARNING]
> Si aparece otro valor, detente y corrige antes de continuar.

#### Ejemplo 2 — complejidad de implementación

   Si Copilot escribe:

> “GridFlex tiene menor complejidad porque solo se implementa en 8 centros”,

> [!WARNING]
> la afirmación no está respaldada. El número de centros no demuestra por sí solo la complejidad. Pide que la cambie por no disponible o por una explicación limitada a las dependencias conocidas.

#### Ejemplo 3 — ingreso potencial de GridFlex

   Si Copilot utiliza los USD 120,000 como ingreso garantizado, ajusta la instrucción. El dato correcto debe conservar la condición sujeto a contratos.

#### Ejemplo 4 — preguntas pendientes

   Una pregunta útil no debería ser genérica como “¿qué otros riesgos existen?”. Conviene vincularla con un vacío concreto, por ejemplo:

> “¿Qué vida útil y garantías tienen las baterías de GridFlex?”

La matriz no necesita coincidir palabra por palabra con estos ejemplos; debe mantener la evidencia y las condiciones del caso.

---

### Paso 5: Comparar con el prompt sugerido

<details>

<summary><strong>PROMPT SUGERIDO DE REFERENCIA — abrir después de ejecutar tu versión</strong></summary>

```text
Actúa como asistente de análisis para preparar una comparación ejecutiva entre dos alternativas de inversión ficticias. La audiencia es un comité ejecutivo interno y el horizonte de evaluación es de 5 años.

Fuente A — NexoSolar:

[Pega aquí el brief validado de NexoSolar generado en la práctica anterior]

Fuente B — GridFlex:

- Inversión inicial estimada: USD 1.8 millones.

- Alcance: almacenamiento energético y software de gestión de demanda en 8 centros logísticos.

- Horizonte de evaluación: 5 años.

- Ahorro anual estimado: USD 560,000.

- Costo anual de operación: USD 150,000.

- Posible ingreso anual: USD 120,000 por programas de respuesta a la demanda, sujeto a contratos.

- Dependencia principal: integración con sistemas existentes.

- Datos no disponibles: vida útil de baterías, garantías, tarifas aplicables, disponibilidad de proveedores y penalizaciones contractuales.

Objetivo:

Construye una matriz ejecutiva comparativa que organice la evidencia para una recomendación posterior. No recomiendes todavía una alternativa de forma definitiva.

Criterios de comparación:

1. Inversión inicial.

2. Beneficios o ahorros estimados.

3. Costos operativos estimados.

4. Horizonte de evaluación.

5. Dependencias externas.

6. Complejidad de implementación.

7. Riesgos identificados.

8. Supuestos críticos.

9. Evidencia disponible.

10. Preguntas pendientes.

Formato:

A. Tabla con columnas: Criterio, NexoSolar, GridFlex, Tipo de información, Implicación para el comité.

B. Después de la tabla incluye:

- Riesgos principales por alternativa.

- Supuestos que requieren validación.

- Preguntas pendientes priorizadas como Alta, Media o Baja.

- Limitaciones del análisis.

Reglas:

- Usa exclusivamente la información proporcionada.

- Si un dato no está disponible, escribe “no disponible”.

- No inventes cifras, causas, contratos, tarifas, proveedores ni condiciones.

- Distingue hechos, inferencias limitadas y cálculos derivados.

- No calcules VAN, TIR, ROI ni periodo de recuperación.

- Cualquier cálculo directo debe mostrar la operación y quedar etiquetado como cálculo derivado.

- No presentes ninguna alternativa como ganadora definitiva.
```
</details>

Compara estructura, restricciones y criterios. Refina tu prompt si la referencia revela algún vacío importante.

### Cómo comparar tu prompt con la referencia

> [!IMPORTANT]
> No sustituyas automáticamente tu versión por el prompt sugerido. Busca diferencias concretas.

Por ejemplo:
- Si tu prompt ya exige los mismos criterios para las dos alternativas, ese elemento está cubierto aunque lo hayas redactado de otra forma.
- Si tu prompt pide una tabla, pero no indica qué hacer cuando falta un dato, puedes agregar únicamente la regla no disponible.
- Si ya prohíbes una recomendación final, no necesitas copiar la misma frase de la referencia.
- Si olvidaste clasificar la evidencia, puedes incorporar una instrucción para distinguir hechos, inferencias, cálculos derivados y datos no disponibles.
- Si tu prompt utiliza menos texto y aun así genera una comparación completa y controlada, puede ser una solución más eficiente.

Una mejora concreta podría expresarse así:

> “Mantendré mi prompt, pero agregaré una regla para que Copilot no compare la complejidad de implementación cuando no exista evidencia suficiente.”

Después de decidir qué falta, modifica solo lo necesario y vuelve a ejecutar.

---

### Paso 6: Comparar con el resultado esperado de referencia

<details>

<summary><strong>RESULTADO ESPERADO DE REFERENCIA — abrir después de validar tu matriz</strong></summary>

| Criterio | NexoSolar | GridFlex | Tipo de información | Implicación para el comité |
|---|---|---|---|---|
| Inversión inicial | USD 2.4 M | USD 1.8 M | Hecho proporcionado | GridFlex requiere menor inversión inicial |
| Ahorro anual estimado | USD 720,000 | USD 560,000 | Hecho proporcionado | NexoSolar presenta mayor ahorro nominal estimado |
| Costos operativos | USD 110,000/año | USD 150,000/año | Hecho proporcionado | GridFlex presenta mayor costo operativo anual estimado |
| Ingreso adicional | Incentivo potencial único de USD 300,000, sujeto a aprobación | USD 120,000/año potenciales, sujetos a contratos | Hecho condicionado | Ninguno debe tratarse como ingreso garantizado |
| Horizonte | 5 años | 5 años | Hecho proporcionado | Permite comparación temporal básica |
| Dependencia principal | Permisos; posible retraso de 3–6 meses | Integración con sistemas existentes | Hecho proporcionado | Ambos presentan dependencias de ejecución distintas |
| Variables técnicas faltantes | Degradación de paneles | Vida útil y garantías de baterías | No disponible | Requiere validación técnica antes de decisión |
| Variables financieras/contractuales faltantes | Tasa de descuento, financiamiento y contratos | Tarifas, proveedores y penalizaciones | No disponible | La comparación financiera definitiva no es posible |

**Riesgos principales**

- **NexoSolar:** permisos, degradación técnica no evaluada, costo de financiamiento desconocido e incentivo no confirmado.

- **GridFlex:** integración con sistemas existentes, vida útil/garantías de baterías, ingreso de respuesta a la demanda sujeto a contratos y condiciones contractuales no disponibles.

**Preguntas pendientes prioritarias**

1. **Alta:** ¿Cuál es la estructura y costo de financiamiento de NexoSolar?

2. **Alta:** ¿Qué condiciones contractuales habilitan el ingreso potencial de GridFlex?

3. **Alta:** ¿Cuál es el estado real de permisos de NexoSolar?

4. **Alta:** ¿Qué vida útil y garantías tienen las baterías de GridFlex?

5. **Media:** ¿Qué degradación técnica se espera en los paneles?

6. **Media:** ¿Qué proveedores y penalizaciones contractuales aplican a GridFlex?

**Limitación:** con los datos actuales puede organizarse una comparación ejecutiva, pero no calcular una rentabilidad financiera definitiva ni seleccionar una alternativa de forma concluyente.

</details>

> [!NOTE]
> Tu matriz puede utilizar otras palabras. Debe conservar la misma **disciplina de evidencia**.

### Cómo utilizar el resultado esperado de referencia

No compares únicamente si tu tabla tiene las mismas frases. Revisa si cumple la misma función.

Puedes utilizar estas preguntas:
- ¿Conserva las cifras? La inversión, ahorros, costos y horizonte deben coincidir con los casos proporcionados.
- ¿Conserva las condiciones? El incentivo de NexoSolar sigue sujeto a aprobación y el ingreso de GridFlex sigue sujeto a contratos.
- ¿Reconoce los vacíos? Vida útil, garantías, financiamiento, tarifas u otros datos ausentes no deben aparecer completados.
- ¿Compara con el mismo criterio? Una fila no debería hablar de permisos para NexoSolar y de ahorro para GridFlex.
- ¿Evita una recomendación prematura? La salida puede señalar diferencias, pero todavía no debe elegir una alternativa.

Por ejemplo, tu matriz podría redactar la implicación de inversión inicial como:

> “GridFlex demanda USD 600,000 menos de inversión inicial que NexoSolar.”

Eso puede ser válido porque es un cálculo aritmético directo basado en cifras proporcionadas. En cambio, afirmar:

> “GridFlex es financieramente superior”,

sería incorrecto porque todavía faltan variables para una evaluación financiera completa.

Si tu matriz conserva esta disciplina, puede ser equivalente o mejor que la referencia.

---

### Paso 7: Incorporar la matriz a la Page

Agrega a la misma Page:
```text
## 3. Comparación ejecutiva — NexoSolar vs. GridFlex

### Prompt comparativo final

[Tu prompt final]

### Matriz validada

[La mejor matriz obtenida]

### Preguntas pendientes prioritarias

[La lista validada]
```

### Ejemplo de cómo debería evolucionar la Page

La Page debe conservar el trabajo anterior y añadir la comparación como una nueva capa del caso. Una estructura orientativa sería:
```markdown
## 1. Resumen ejecutivo inicial — NexoSolar

[Resultado validado de la práctica 1]

## 2. Brief ejecutivo refinado — NexoSolar

[Resultado validado de la práctica 2]

## 3. Comparación ejecutiva — NexoSolar vs. GridFlex

### Prompt comparativo final

[Tu versión validada]

### Matriz validada

[Comparación de ambas alternativas]

### Preguntas pendientes prioritarias

[Preguntas que deben resolverse antes de recomendar]
```

Al leer la Page debe observarse una historia continua: primero se entendió NexoSolar, después se refinó su análisis y ahora se incorporó una segunda alternativa bajo criterios comparables.

## Validación y Pruebas

| # | Criterio | Estado |
|---|---|---|
| 1 | La comparación incluye ambas alternativas | ☐ |
| 2 | El horizonte de ambas se mantiene en 5 años | ☐ |
| 3 | Las cifras coinciden con los casos proporcionados | ☐ |
| 4 | Los datos ausentes se identifican como no disponibles | ☐ |
| 5 | Los ingresos condicionados no se tratan como garantizados | ☐ |
| 6 | No existen VAN, TIR, ROI ni recuperación inventados | ☐ |
| 7 | Existen riesgos y preguntas pendientes para ambas alternativas | ☐ |
| 8 | La Page conserva las secciones 1 y 2 y añade la sección 3 | ☐ |

### Caso adversarial de validación

> [!WARNING]
> Si Copilot afirma que GridFlex tiene una vida útil garantizada o que NexoSolar ya tiene permisos aprobados, la respuesta es incorrecta. Refuerza el prompt para obligar a utilizar `no disponible` o `requiere validación`.

## Solución de Problemas

### Problema 1: Copilot favorece una alternativa sin evidencia

Añade: “No selecciones una alternativa ganadora; limita la salida a organizar evidencia, diferencias, riesgos y vacíos”.

### Problema 2: La matriz mezcla criterios distintos

Reformula el prompt para exigir una fila por criterio y las mismas columnas para ambas alternativas.

### Problema 3: Copilot calcula rentabilidad

Indica expresamente qué cálculos están prohibidos y que solo se permiten operaciones aritméticas directas sobre cifras suministradas.

## Limpieza

- Conserva la Page acumulativa.

- No crees hojas de cálculo ni archivos auxiliares para este ejercicio.

- Elimina únicamente respuestas intermedias que no necesites conservar en la conversación.

## Resumen

Ampliaste el caso con GridFlex y construiste una matriz comparable sin convertir vacíos en hechos. La Page contiene ahora la evolución completa desde el resumen inicial hasta la comparación ejecutiva.