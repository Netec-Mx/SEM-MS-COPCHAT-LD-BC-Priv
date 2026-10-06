# Práctica guiada 2. Evolucionar el prompt base hasta obtener un brief ejecutivo con tesis, supuestos, riesgos y datos faltantes
## Metadatos
| Elemento | Valor |
|---|---|
| Duración | 25 minutos |
| Complejidad | Media |
| Nivel de Bloom | Aplicar |
| Aplicación principal | Microsoft 365 Copilot Chat |
| Insumo | Prompt y resumen validados de la práctica 1, disponibles en la Copilot Page |
| Entregable | Brief ejecutivo refinado incorporado a la misma Page |


## Descripción General
El comité ya revisó el resumen inicial de NexoSolar. La información permite comprender la oportunidad, pero todavía no organiza claramente la tesis, los supuestos, los riesgos ni los datos faltantes que deben resolverse antes de tomar una decisión.

En esta práctica **evolucionarás tu propio prompt**, no comenzarás desde cero. Analizarás qué le falta al resultado anterior, decidirás qué nuevas instrucciones necesita Copilot y construirás una segunda versión orientada a un brief ejecutivo. Al final compararás tu prompt y tu respuesta con referencias completas.


## Objetivos de Aprendizaje
- [ ] Identificar brechas concretas en una respuesta generada anteriormente.
- [ ] Refinar un prompt incorporando mayor contexto, formato, restricciones y criterios de calidad.
- [ ] Obtener un brief con tesis, hechos, supuestos, riesgos y datos faltantes.
- [ ] Diferenciar información proporcionada de inferencias o cálculos no disponibles.
- [ ] Comparar el trabajo propio con un prompt sugerido y un resultado esperado de referencia.
- [ ] Integrar el brief refinado en la Page acumulativa del caso.


## Prerrequisitos
- Haber completado la práctica guiada 1.
- Tener disponible la Copilot Page `Caso de inversión — NexoSolar vs. GridFlex`.
- Conservar en la Page el prompt base final y el resumen validado de NexoSolar.
- Utilizar el mismo conjunto de datos de la práctica anterior; no sustituir cifras ni condiciones.


## Entorno de Laboratorio
### Configuración tecnológica
| Elemento | Requisito |
|---|---|
| Copilot Chat | Disponible para la cuenta del participante |
| Copilot Page | Page creada en la práctica anterior |
| Datos | Únicamente el caso ficticio NexoSolar definido en la práctica 1 |
| Archivos auxiliares | No requeridos |


### Licencias y configuración
La práctica se realiza exclusivamente en Copilot Chat y Copilot Pages. No requiere aplicaciones adicionales ni creación de archivos de evidencia.


### Recursos de hardware y conectividad
Un equipo con navegador o aplicación autorizada, conexión estable a Internet y acceso a Copilot Chat.


### Preparación del espacio de trabajo
1. Abre la Page `Caso de inversión — NexoSolar vs. GridFlex`.
2. Localiza la sección `1. Resumen ejecutivo inicial — NexoSolar`.
3. Abre Copilot Chat y, cuando sea posible, continúa en la conversación de la práctica anterior para conservar el contexto. Si inicias un chat nuevo, vuelve a proporcionar los datos del caso.


## Distribución de tiempo
| Fase | Actividad | Tiempo |
|---|---|---:|
| 1 | Revisar el resultado anterior y detectar brechas | 4 min |
| 2 | Diseñar y construir el prompt refinado | 6 min |
| 3 | Ejecutar y revisar el brief | 5 min |
| 4 | Comparar con el prompt sugerido | 4 min |
| 5 | Comparar con el resultado esperado y refinar | 4 min |
| 6 | Actualizar la Page | 2 min |
| **TOTAL** |  | **25 min** |


## Instrucciones Paso a Paso
### Paso 1: Volver al punto donde terminó la práctica anterior
> [!NOTE]
> **Objetivo:** utilizar el resultado anterior como punto de partida real del proceso.


Lee el resumen validado de NexoSolar en tu Page. El comité ahora plantea nuevas preguntas:

- ¿Cuál es la tesis de la oportunidad?
- ¿Qué elementos son hechos y cuáles requieren validación?
- ¿Qué riesgos pueden afectar la decisión?
- ¿Qué información faltante debe priorizarse?


> [!TIP]
> **Por qué este paso importa:** refinar un prompt no significa hacerlo más largo; significa identificar qué necesidad nueva no está siendo cubierta por la versión anterior.


En la respuesta previa identifica al menos dos brechas. Algunas posibilidades:


- no existe una tesis clara;
- no diferencia supuestos de hechos;
- los riesgos no están organizados;
- los datos faltantes no tienen prioridad;
- la salida no indica qué debería validarse antes de continuar.


Utiliza esta revisión únicamente para decidir qué modificarás en tu prompt.


#### Ejemplo para orientarte
No necesitas redactar todavía una solución. Busca señales concretas en tu resultado anterior.


**Por ejemplo:**
- Si tu resumen dice que NexoSolar requiere una inversión de USD 2.4 millones y que podría generar ahorros, pero no explica por qué la oportunidad podría ser relevante para el comité, probablemente falta una tesis.
- Si menciona el retraso de permisos como un dato aislado, pero no indica qué podría afectar, el riesgo todavía no está suficientemente estructurado.
- Si aparecen juntos la tasa de descuento, el financiamiento y la degradación de paneles sin distinguir cuál condiciona más la evaluación, falta priorizar la información pendiente.
- Si una frase afirma que “el proyecto será rentable”, esa conclusión va más allá de la evidencia disponible.


Puedes pensar tu revisión con una frase breve como:


> “Mi respuesta anterior explica qué es NexoSolar, pero todavía no separa con claridad hechos, riesgos, supuestos y datos críticos para continuar el análisis.”


> [!TIP]
> No copies esta frase como respuesta final. Úsala únicamente para identificar qué debe mejorar tu siguiente prompt.


---
### Paso 2: Decidir cómo debe evolucionar la salida
> [!NOTE]
> **Objetivo:** definir el nuevo producto antes de redactar instrucciones.


El resultado ya no será un resumen inicial. Debe convertirse en un **brief ejecutivo** con estas secciones:


1. Tesis de la oportunidad.
2. Hechos proporcionados.
3. Supuestos e inferencias.
4. Riesgos.
5. Datos faltantes priorizados.
6. Conclusión provisional sobre si existe información suficiente para avanzar a una evaluación más profunda.


> [!IMPORTANT]
> **Decisión importante:** una “conclusión provisional” no equivale a aprobar la inversión. El brief puede concluir que conviene continuar la validación o que faltan datos críticos.


#### Ejemplo para entender el cambio de salida
Un resumen inicial podría limitarse a expresar una idea como:

> “NexoSolar contempla sistemas solares en 12 centros logísticos con una inversión estimada de USD 2.4 millones.”


Eso explica el caso, pero todavía aporta poco para una revisión ejecutiva.


Un brief refinado debería ayudar a responder preguntas adicionales, por ejemplo:

- ¿Cuál podría ser la lógica de la oportunidad?
- ¿Qué información está confirmada?
- ¿Qué afirmaciones son inferencias?
- ¿Qué riesgos requieren atención?
- ¿Qué dato faltante debería resolverse primero?


Una forma de visualizar la evolución es:

> **Antes:** “Existe un posible incentivo de USD 300,000.”

> **Después:** “Hecho: existe un incentivo potencial de USD 300,000. Su aprobación no está confirmada, por lo que no debe incorporarse como beneficio asegurado.”


Tu salida no tiene que usar exactamente estas palabras. Lo importante es que el brief agregue estructura y criterio, no simplemente más texto.


---
### Paso 3: Refinar tu prompt base
> [!NOTE]
> **Objetivo:** modificar el prompt de la práctica 1 incorporando las necesidades nuevas.


Parte de tu propio prompt anterior y añade instrucciones para que Copilot:

- mantenga exactamente los datos de NexoSolar;
- formule una tesis breve;
- etiquete de forma visible hechos, supuestos e inferencias;
- agrupe riesgos en categorías útiles;
- priorice la información faltante;
- evite TIR, VAN, ROI u otros cálculos no soportados por la evidencia;
- emita únicamente una conclusión provisional sobre el siguiente paso de análisis.


> [!WARNING]
> **No envíes todavía.** Revisa que tu nueva versión siga incluyendo la evidencia del caso si estás en un chat nuevo.


> [!TIP]
> **Por qué este paso importa:** la calidad del refinamiento depende de transformar necesidades ejecutivas concretas en criterios verificables de salida.


#### Ideas para empezar a construir tu prompt
No necesitas redactarlo de una sola vez. Puedes construirlo por bloques.
##### 1. Recupera el punto de partida
   Puedes comenzar con una idea como:

> “A partir del análisis anterior de NexoSolar, necesito convertir el resumen en un brief ejecutivo más útil para continuar la evaluación.”
##### 2. Define qué debe hacer Copilot
   Algunas formas de plantearlo:

> “Formula una tesis breve sobre la oportunidad...”

> “Separa la información proporcionada de las inferencias...”

> “Organiza los riesgos por categorías...”

> “Ordena los datos faltantes según su importancia para continuar el análisis...”
##### 3. Define cómo quieres ver la respuesta
   Puedes apoyarte en instrucciones como:

> “Presenta los hechos en viñetas.”

> “Utiliza una tabla para los datos faltantes.”

> “Mantén la conclusión en un máximo de un párrafo.”
##### 4. Agrega límites
   Por ejemplo:

> “No calcules métricas financieras que requieran información no disponible.”

> “No presentes el incentivo como aprobado.”

> “Si una conclusión depende de un dato faltante, indícalo expresamente.”


Estas frases son pistas de construcción, no un prompt completo. Selecciona, adapta y combina únicamente las que ayuden a conseguir el brief definido en el paso anterior.


---
### Paso 4: Ejecutar el prompt refinado
1. Envía tu nueva versión.
2. Lee el brief completo.
3. Comprueba especialmente:

   - que la inversión sigue siendo USD 2.4 millones;
   - que el alcance sigue siendo 12 centros;
   - que el horizonte sigue siendo 5 años;
   - que el incentivo permanece sujeto a aprobación;
   - que los permisos aparecen como riesgo potencial de 3 a 6 meses;
   - que no aparecen TIR, VAN o tasas inventadas.

4. Si detectas un error, corrige **tu prompt** o envía una instrucción de refinamiento precisa.


#### Ejemplos de refinamiento durante la conversación
   Si Copilot presenta el incentivo como seguro, podrías intervenir con una instrucción como:

> “Revisa la sección de beneficios. El incentivo de USD 300,000 es potencial y está sujeto a aprobación. Corrige cualquier afirmación que lo presente como confirmado.”


   Si mezcla hechos con interpretaciones:

> “Reestructura la respuesta para que los datos proporcionados aparezcan como hechos y las conclusiones derivadas aparezcan claramente como inferencias.”


   Si todos los datos faltantes aparecen con la misma importancia:

> “Prioriza los datos faltantes según cuánto podrían afectar la capacidad de continuar con una evaluación financiera y explica brevemente el criterio.”


> [!TIP]
> Observa que estas instrucciones corrigen un problema específico. Evita responder simplemente “mejóralo” o “hazlo más ejecutivo”, porque Copilot tendría que adivinar qué deseas cambiar.


---
### Paso 5: Comparar con el prompt sugerido
<details>

<summary><strong>PROMPT SUGERIDO DE REFERENCIA — abrir después de ejecutar tu versión</strong></summary>


```text

Refina el análisis de la oportunidad ficticia NexoSolar para convertirlo en un brief ejecutivo dirigido a un comité ejecutivo interno.

Datos autorizados del caso:

- Inversión inicial estimada: USD 2.4 millones.
- Alcance: sistemas solares en 12 centros logísticos.
- Horizonte de evaluación: 5 años.
- Ahorro anual estimado de energía: USD 720,000.
- Costo anual estimado de mantenimiento: USD 110,000.
- Incentivo potencial: USD 300,000, sujeto a aprobación.
- Riesgo conocido: los permisos podrían retrasar el proyecto entre 3 y 6 meses.
- Datos no disponibles: tasa de descuento, costo de financiamiento, degradación de paneles y condiciones contractuales.

Objetivo:

Transforma el resumen inicial en un brief que ayude al comité a identificar qué se sabe, qué debe validarse y qué información falta antes de una decisión.

Formato obligatorio:

1. Tesis de la oportunidad: máximo 3 frases.
2. Hechos proporcionados: máximo 6 viñetas; inicia cada una con “Hecho:”.
3. Supuestos e inferencias: separa claramente ambos conceptos. No conviertas ninguno en hecho.
4. Riesgos: organiza en operativos, financieros y regulatorios/permisos. Para cada riesgo indica la evidencia disponible y qué debe validarse.
5. Datos faltantes priorizados: tabla con “Dato faltante”, “Por qué importa” y “Prioridad” (Alta, Media o Baja).
6. Conclusión provisional: máximo 80 palabras indicando si existe información suficiente para continuar a una evaluación comparativa, sin aprobar ni rechazar la inversión.

Restricciones:

- Utiliza exclusivamente los datos proporcionados.
- No inventes métricas, tasas, contratos, aprobaciones, proveedores ni cálculos financieros.
- No calcules TIR, VAN, ROI ni periodo de recuperación.
- Mantén el incentivo fiscal como potencial y sujeto a aprobación.
- Si una afirmación requiere información no disponible, márcala como “requiere validación”.

```

</details>


Compara tu prompt con la referencia. Si el tuyo consigue el mismo propósito con instrucciones más claras o eficientes, consérvalo. Si falta algún elemento esencial, mejóralo y vuelve a ejecutar.


#### Antes de modificar tu prompt, busca diferencias concretas
> [!IMPORTANT]
> No reemplaces automáticamente tu versión por la sugerida. Compáralas elemento por elemento.


**Por ejemplo:**
- Si tu prompt ya pide separar hechos de inferencias, no necesitas copiar esa instrucción otra vez.
- Si tu prompt identifica riesgos pero no solicita indicar qué debe validarse, puedes añadir únicamente ese criterio.
- Si tu versión produce una tabla de datos faltantes clara y priorizada, aunque use columnas diferentes, puede ser igualmente válida.
- Si tu prompt es más corto pero genera consistentemente las seis secciones requeridas, puede ser una mejor solución.

Una buena comparación puede terminar con una decisión como:

> “Mantendré mi estructura, pero agregaré una instrucción para vincular cada riesgo con la evidencia disponible y la validación requerida.”


---
### Paso 6: Comparar con un resultado esperado de referencia
<details>

<summary><strong>RESULTADO ESPERADO DE REFERENCIA — abrir después de validar tu brief</strong></summary>

#### Tesis de la oportunidad

NexoSolar propone reducir costos energéticos mediante sistemas solares en 12 centros logísticos. La oportunidad combina un ahorro anual estimado relevante con una inversión inicial de USD 2.4 millones, pero su evaluación sigue condicionada por permisos, variables financieras y condiciones contractuales no disponibles.

#### Hechos proporcionados

- **Hecho:** inversión inicial estimada de USD 2.4 millones.
- **Hecho:** alcance de 12 centros logísticos.
- **Hecho:** horizonte de evaluación de 5 años.
- **Hecho:** ahorro anual estimado de USD 720,000.
- **Hecho:** mantenimiento anual estimado de USD 110,000.
- **Hecho:** existe un incentivo potencial de USD 300,000 sujeto a aprobación.

#### Supuestos e inferencias

- **Inferencia:** el ahorro energético podría mejorar la estructura de costos, pero no equivale a rentabilidad financiera confirmada.
- **Inferencia:** un retraso de permisos podría desplazar el calendario de beneficios.
- **Supuesto a validar:** que el incentivo fiscal sea finalmente aprobado.

#### Riesgos

| Categoría | Riesgo | Evidencia | Validación requerida |
|---|---|---|---|
| Operativo | Desempeño y degradación de paneles no evaluados | La degradación no está disponible | Obtener supuestos técnicos y garantías |
| Financiero | Costo de capital desconocido | No se proporcionan tasa de descuento ni financiamiento | Definir estructura y costo de financiamiento |
| Regulatorio/permisos | Posible retraso de 3 a 6 meses | Dato proporcionado | Confirmar estado y calendario de permisos |

#### Datos faltantes priorizados

| Dato faltante | Por qué importa | Prioridad |
|---|---|---|
| Costo de financiamiento | Puede modificar de forma material la conveniencia financiera | Alta |
| Tasa de descuento | Es necesaria para una valoración financiera completa | Alta |
| Condiciones contractuales | Determinan obligaciones, riesgos y condiciones económicas | Alta |
| Degradación de paneles | Afecta el desempeño esperado durante el horizonte | Media |

#### Conclusión provisional

La información es suficiente para continuar con una evaluación comparativa preliminar, pero no para aprobar la inversión. Antes de una recomendación definitiva deben validarse costo de financiamiento, tasa de descuento, condiciones contractuales, desempeño técnico e incentivo fiscal.

</details>


> [!NOTE]
> La forma de redactar puede variar. Tu brief debe ser equivalente en **cobertura, prudencia y trazabilidad**.


#### Cómo utilizar el resultado de referencia
> [!TIP]
> No compares palabra por palabra. Busca señales de calidad.


**Por ejemplo:**
- En Hechos, deberían aparecer únicamente datos entregados en el caso.
- En Supuestos e inferencias, una frase como “el ahorro podría mejorar la estructura de costos” es aceptable si queda marcada como inferencia y no como hecho.
- En Riesgos, no basta con escribir “permisos”; debería quedar claro qué se conoce y qué se necesita validar.
- En Datos faltantes, la prioridad debe tener una razón. No es suficiente colocar “Alta” sin explicar por qué.
- En la Conclusión provisional, una salida prudente puede indicar que existe base para continuar el análisis, pero todavía no para aprobar la inversión.

Si tu respuesta cubre estos elementos con una redacción diferente, no necesitas reemplazarla por el ejemplo.


---
### Paso 7: Actualizar la Copilot Page
En la misma Page agrega:


```text

## 2. Brief ejecutivo refinado — NexoSolar


### Prompt refinado final

[Tu versión final]


### Brief validado

[La mejor respuesta obtenida]

```

> [!WARNING]
> No elimines la sección de la práctica 1; el propósito es evidenciar cómo evolucionó el análisis.


#### Ejemplo de cómo debería verse la evolución en la Page
No necesitas copiar este contenido. Utilízalo únicamente como referencia de organización:


```markdown
## 1. Resumen ejecutivo inicial — NexoSolar
[Resultado validado de la práctica 1]


## 2. Brief ejecutivo refinado — NexoSolar
### Prompt refinado final
[Prompt que construiste y validaste]


### Brief validado
[Tesis]

[Hechos]

[Supuestos e inferencias]

[Riesgos]

[Datos faltantes priorizados]

[Conclusión provisional]
```


Al observar ambas secciones debería ser evidente que el caso no cambió; lo que mejoró fue la manera de solicitar, organizar y evaluar la información.


## Validación y Pruebas
| # | Criterio | Estado |
|---|---|---|
| 1 | El brief conserva las cifras originales del caso | ☐ |
| 2 | Existe una tesis ejecutiva breve | ☐ |
| 3 | Hechos, supuestos e inferencias están diferenciados | ☐ |
| 4 | Los riesgos están organizados y vinculados a evidencia | ☐ |
| 5 | Los datos faltantes aparecen priorizados | ☐ |
| 6 | No se calculan métricas financieras no soportadas | ☐ |
| 7 | La conclusión es provisional y no aprueba la inversión | ☐ |
| 8 | La Page contiene la nueva sección sin eliminar la anterior | ☐ |


### Criterios de aceptación
La práctica se considera terminada cuando el brief puede ser utilizado como insumo de comparación en el capítulo 4 sin introducir datos que no existían en el caso original.


## Solución de Problemas
### Problema 1: Copilot cambia las cifras del caso
Vuelve a proporcionar el conjunto completo de datos y agrega: “Conserva exactamente las cifras suministradas; no sustituyas ni normalices valores”.


### Problema 2: Copilot formula una recomendación definitiva
Refina el prompt para pedir únicamente una “conclusión provisional sobre la suficiencia de información” y prohíbe aprobar o rechazar la inversión.


### Problema 3: El brief es demasiado extenso
Reduce el número máximo de viñetas, limita la tesis a tres frases y establece extensiones máximas por sección.


## Limpieza
- Conserva la Page acumulativa.
- No generes archivos separados, bitácoras ni notas de trabajo como entregables.
- Puedes cerrar respuestas intermedias que no formen parte del resultado final.


## Resumen
Transformaste el prompt base en un instrumento de análisis más preciso. El caso sigue siendo el mismo; lo que evolucionó fue la calidad de la solicitud y la estructura del resultado. La Page contiene ahora el resumen inicial y el brief refinado.
