# Práctica guiada 1. Crear el prompt base para resumir una oportunidad de inversión ficticia para una audiencia ejecutiva

## Metadatos

| Campo | Valor |
|---|---|
| Duración | 15 minutos |
| Complejidad | Fácil |
| Nivel de Bloom | Aplicar |
| Aplicación principal | Microsoft 365 Copilot Chat |
| Insumo | Caso ficticio NexoSolar incluido en esta guía |
| Entregable | Primera sección de una Copilot Page acumulativa |

## Descripción General

En esta práctica iniciarás un caso financiero que continuará durante todo el curso. Recibirás información ficticia sobre **NexoSolar** y asumirás que debes preparar un primer resumen para un comité ejecutivo interno.

La guía te llevará a decidir qué debe saber Copilot, qué debe producir, qué restricciones necesita y cómo debe presentar la respuesta. Después de ejecutar tu propia versión podrás abrir un **prompt sugerido de referencia** y un **resultado esperado de referencia** para comparar, corregir y mejorar tu trabajo.

El producto de la práctica se conservará en una **Copilot Page** titulada `Caso de inversión — NexoSolar vs. GridFlex`. Esta Page se ampliará en las prácticas siguientes.

> **Caso formativo:** todos los nombres, cifras y condiciones de esta guía son ficticios. El ejercicio no constituye asesoramiento financiero, fiscal, legal ni de inversión.

## Objetivos de Aprendizaje

- [ ] Construir un prompt base a partir de una necesidad ejecutiva concreta.
- [ ] Incorporar objetivo, contexto, audiencia, evidencia, restricciones y formato esperado.
- [ ] Ejecutar el prompt y revisar si Copilot respeta los datos disponibles.
- [ ] Comparar el prompt propio con un prompt sugerido y mejorarlo cuando sea necesario.
- [ ] Comparar la respuesta obtenida con un resultado de referencia mediante criterios verificables.
- [ ] Crear la Page que funcionará como entregable acumulativo del caso.

## Prerrequisitos

- Haber observado la demostración de acceso a Copilot Chat correspondiente al capítulo 2.
- Tener una cuenta corporativa o educativa elegible con Copilot Chat habilitado.
- Poder crear o editar una Copilot Page desde la experiencia disponible en tu organización.
- Comprender la estructura mínima vista en el capítulo 1: **objetivo, contexto, expectativas y fuente**.
- Utilizar exclusivamente los datos ficticios de esta guía.

## Entorno de Laboratorio

### Hardware mínimo recomendado

| Componente | Requisito |
|---|---|
| Equipo | Computadora capaz de ejecutar un navegador moderno o la aplicación autorizada por la organización |
| Conectividad | Acceso estable a Internet |
| Pantalla | Resolución suficiente para trabajar con Chat y Page de forma cómoda |
| Entrada | Teclado físico o virtual para redactar prompts de varias líneas |

### Software y servicios

| Tecnología | Uso en la práctica | Requisito funcional |
|---|---|---|
| Microsoft 365 Copilot Chat | Construcción, ejecución y refinamiento del prompt | Debe estar disponible para la cuenta del participante |
| Copilot Pages | Entregable acumulativo del caso | Debe permitirse crear o editar una Page desde la experiencia disponible |
| Navegador o aplicación Microsoft 365 Copilot | Acceso al servicio | Utilizar una opción autorizada por la organización |

### Alcance de licencias y herramientas

No se requieren Word, Excel, PowerPoint, bases de datos, terminales, máquinas virtuales ni archivos auxiliares. Todo el ejercicio se realiza en **Copilot Chat** y **Copilot Pages**.

### Configuración inicial

1. Abre Copilot Chat con tu cuenta autorizada.
2. Inicia una conversación nueva.
3. No pegues información real de clientes, inversiones o de tu organización.
4. Mantén disponible la opción para crear una Page cuando llegues al último paso.

## Distribución de tiempo

| Fase | Actividad | Tiempo |
|---|---|---:|
| 1 | Comprender el caso y la necesidad ejecutiva | 2 min |
| 2 | Construir el prompt base | 4 min |
| 3 | Ejecutar y revisar la primera respuesta | 3 min |
| 4 | Comparar con el prompt sugerido y mejorar | 3 min |
| 5 | Comparar el resultado y crear la Page | 3 min |
| **TOTAL** |  | **15 min** |

## Instrucciones Paso a Paso

### Paso 1: Entender la situación antes de escribir

**Objetivo:** comprender qué necesita el comité y qué información está realmente disponible.

**Situación:** formas parte de un equipo que prepara información para un comité ejecutivo interno. El comité recibió una oportunidad denominada **NexoSolar**. En esta primera etapa no quiere aprobar ni rechazar la inversión; necesita un resumen breve para entender de qué se trata, cuáles son los datos relevantes y qué información todavía falta.

**Información disponible del caso:**

| Elemento | Información proporcionada |
|---|---|
| Oportunidad | NexoSolar |
| Inversión inicial estimada | USD 2.4 millones |
| Alcance | Sistemas solares en 12 centros logísticos |
| Horizonte de evaluación | 5 años |
| Ahorro anual estimado de energía | USD 720,000 |
| Costo anual estimado de mantenimiento | USD 110,000 |
| Incentivo potencial | USD 300,000, sujeto a aprobación |
| Riesgo conocido | Los permisos podrían retrasar el proyecto entre 3 y 6 meses |
| Información no disponible | Tasa de descuento, costo de financiamiento, degradación de paneles y condiciones contractuales |
| Audiencia | Comité ejecutivo interno |

**Por qué este paso importa:** Copilot no conoce este caso. Si la información no aparece en el prompt, no debe suponerse que el modelo la conoce o que puede completarla de forma segura.

**Antes de continuar, responde mentalmente:**

- ¿Qué necesita recibir el comité en esta etapa?
- ¿Qué cifras sí puede utilizar Copilot?
- ¿Qué información todavía no existe?
- ¿Qué conclusión no debe emitir todavía?

**Resultado esperado:** puedes explicar el caso en una frase y distinguir datos disponibles de datos faltantes.

---

### Paso 2: Construir el objetivo y la audiencia del prompt

**Objetivo:** redactar la primera parte de tu prompt.

1. En el cuadro de Copilot Chat escribe una primera instrucción que indique **qué debe producir Copilot**.
2. Incluye explícitamente que la salida se dirige a un **comité ejecutivo interno**.
3. No envíes todavía el prompt.

Puedes comenzar con una idea como:

```text
Prepara un resumen ejecutivo inicial...
```

**Por qué este paso importa:** “resumir información” es demasiado general. La audiencia y el uso del resultado ayudan a ajustar nivel de detalle, tono y estructura.

**Comprueba antes de seguir:** tu instrucción deja claro que quieres un resumen ejecutivo, no una recomendación definitiva.

---

### Paso 3: Incorporar el contexto y la evidencia

**Objetivo:** conseguir que Copilot trabaje sobre el mismo expediente que tú estás revisando.

1. Debajo de la instrucción inicial incorpora los datos de la tabla del **Paso 1**.
2. Mantén las cifras y condiciones exactamente como aparecen.
3. No conviertas el incentivo potencial en un beneficio confirmado.
4. Incluye también la lista de información no disponible.

**Por qué este paso importa:** un buen prompt no solo expresa una tarea; proporciona la evidencia necesaria para realizarla y delimita qué información puede utilizarse.

**Criterio de finalización:** tu borrador contiene NexoSolar, USD 2.4 millones, 12 centros, 5 años, USD 720,000, USD 110,000, el incentivo condicionado, el retraso potencial y los cuatro datos faltantes.

---

### Paso 4: Añadir restricciones que eviten conclusiones engañosas

**Objetivo:** limitar el comportamiento de Copilot cuando la evidencia es insuficiente.

Piensa qué podría salir mal. Por ejemplo:

- convertir el incentivo en un hecho confirmado;
- inventar una TIR, VAN o tasa de descuento;
- afirmar que el proyecto es rentable;
- agregar proveedores, fechas o contratos inexistentes.

Ahora añade a tu prompt reglas que impidan esos comportamientos. Como mínimo, tu prompt debe indicar que Copilot:

- use únicamente los datos proporcionados;
- no invente cifras ni condiciones;
- distinga hechos de información pendiente;
- no emita todavía una recomendación de inversión.

**Por qué este paso importa:** las restricciones hacen explícito qué debe hacer el modelo cuando no dispone de información suficiente.

---

### Paso 5: Definir el formato de salida

**Objetivo:** transformar la solicitud en un resultado útil para una audiencia ejecutiva.

El comité necesita localizar rápidamente la información. Define un formato con estas cuatro partes:

1. Resumen de la oportunidad.
2. Hechos relevantes.
3. Riesgos o condiciones conocidas.
4. Información pendiente.

Añade un límite de **150 palabras** para mantener el resultado conciso.

**Por qué este paso importa:** especificar la estructura permite evaluar objetivamente si la respuesta cumple la necesidad.

---

### Paso 6: Ejecutar tu prompt

1. Relee el prompt completo.
2. Comprueba que no contiene información inventada.
3. Envíalo a Copilot Chat.
4. Lee la respuesta completa antes de aceptar el resultado.

**Revisa específicamente:**

- ¿USD 2.4 millones aparece correctamente?
- ¿Se mencionan los 12 centros y el horizonte de 5 años?
- ¿El incentivo de USD 300,000 se mantiene como condicionado?
- ¿El retraso potencial de permisos se presenta como riesgo y no como hecho consumado?
- ¿Se reconocen los datos faltantes?
- ¿Copilot evita recomendar aprobar o rechazar la inversión?

---

### Paso 7: Comparar tu prompt con una referencia

Solo después de ejecutar tu propia versión, abre el siguiente bloque.

<details>
<summary><strong>PROMPT SUGERIDO DE REFERENCIA — abrir después de construir el tuyo</strong></summary>

```text
Actúa como asistente de análisis para preparar información dirigida a un comité ejecutivo interno.

Necesito elaborar un resumen ejecutivo inicial de una oportunidad de inversión ficticia denominada NexoSolar.

Información disponible:
- Inversión inicial estimada: USD 2.4 millones.
- Alcance: instalación de sistemas solares en 12 centros logísticos.
- Horizonte de evaluación: 5 años.
- Ahorro anual estimado de energía: USD 720,000.
- Costo anual estimado de mantenimiento: USD 110,000.
- Posible incentivo fiscal: USD 300,000, sujeto a aprobación.
- Riesgo conocido: los permisos podrían retrasar el proyecto entre 3 y 6 meses.
- No disponemos todavía de tasa de descuento, costo de financiamiento, degradación estimada de los paneles ni condiciones contractuales.

Prepara un resumen ejecutivo breve que permita al comité comprender la oportunidad sin emitir todavía una recomendación de inversión.

Organiza la respuesta en:
1. Resumen de la oportunidad.
2. Hechos relevantes.
3. Riesgos y condiciones conocidas.
4. Información pendiente.

Reglas:
- Utiliza únicamente la información proporcionada.
- No inventes cifras, fechas, proveedores, contratos ni condiciones.
- No presentes el incentivo fiscal como confirmado.
- Diferencia los datos disponibles de la información pendiente.
- No concluyas todavía si la inversión debe aprobarse o rechazarse.
- Extensión máxima: 150 palabras.
```

</details>

**Compara, no copies automáticamente.** Tu versión puede ser igual de válida o mejor. Revisa si contiene los mismos componentes esenciales y, si identificas una mejora, modifica tu prompt y ejecútalo una vez más.

---

### Paso 8: Comparar tu respuesta con un resultado esperado de referencia

<details>
<summary><strong>RESULTADO ESPERADO DE REFERENCIA — abrir después de revisar tu respuesta</strong></summary>

> **Resumen de la oportunidad**  
> NexoSolar plantea instalar sistemas solares en 12 centros logísticos con una inversión inicial estimada de USD 2.4 millones y un horizonte de evaluación de 5 años.
>
> **Hechos relevantes**  
> - Ahorro anual estimado de energía: USD 720,000.  
> - Mantenimiento anual estimado: USD 110,000.  
> - Incentivo potencial: USD 300,000, sujeto a aprobación.
>
> **Riesgos y condiciones conocidas**  
> - Los permisos podrían retrasar el proyecto entre 3 y 6 meses.  
> - El incentivo no está confirmado.
>
> **Información pendiente**  
> - Tasa de descuento.  
> - Costo de financiamiento.  
> - Degradación de paneles.  
> - Condiciones contractuales.
>
> Con la información actual puede describirse la oportunidad, pero todavía no existe evidencia suficiente para emitir una recomendación de inversión.

</details>

La redacción de Copilot puede variar. Evalúa tu salida por **contenido y restricciones**, no por coincidencia textual.

---

### Paso 9: Crear la Copilot Page acumulativa

1. Usa la opción disponible en tu experiencia para llevar la respuesta validada a una Page o crear una Page nueva.
2. Titúlala:

```text
Caso de inversión — NexoSolar vs. GridFlex
```

3. Crea esta primera sección:

```text
## 1. Resumen ejecutivo inicial — NexoSolar
### Prompt base final
[Tu prompt final]

### Resultado validado
[La mejor respuesta obtenida]
```

4. Conserva esta Page. Será el insumo de las prácticas siguientes.

**Criterio de finalización:** la Page contiene el prompt final construido por ti y un resumen de NexoSolar que respeta los datos y restricciones del caso.

## Validación y Pruebas

| # | Criterio | Estado |
|---|---|---|
| 1 | El prompt identifica la audiencia ejecutiva | ☐ |
| 2 | El prompt incorpora todos los datos del caso sin alterarlos | ☐ |
| 3 | El prompt limita la invención de datos y evita una recomendación prematura | ☐ |
| 4 | La respuesta mantiene el incentivo como condicionado | ☐ |
| 5 | La respuesta identifica los cuatro datos faltantes | ☐ |
| 6 | La respuesta no supera 150 palabras | ☐ |
| 7 | Existe la Page `Caso de inversión — NexoSolar vs. GridFlex` | ☐ |
| 8 | La Page contiene el prompt final y el resultado validado de la práctica 1 | ☐ |

## Solución de Problemas

### Problema 1: Copilot agrega información que no aparece en el caso

**Qué hacer:** vuelve a tu prompt y refuerza la restricción: “Utiliza únicamente la información proporcionada y marca como no disponible cualquier dato ausente”. Ejecuta de nuevo.

### Problema 2: La respuesta parece una recomendación de inversión

**Qué hacer:** añade una instrucción explícita: “No recomiendes aprobar, rechazar ni priorizar la inversión en esta etapa”.

### Problema 3: No aparece la opción para crear una Page

**Qué hacer:** utiliza la opción equivalente disponible en tu experiencia de Copilot para crear o editar una Page. Si Pages no está habilitado para tu cuenta, conserva temporalmente la respuesta dentro del mismo chat y comunícalo al instructor; no crees archivos auxiliares por tu cuenta.

## Limpieza

- No elimines la Page creada; se reutiliza en los capítulos 3, 4 y 5.
- Puedes cerrar conversaciones de prueba que no contengan la versión final.
- No guardes bitácoras, archivos de notas ni copias locales adicionales.
- No uses los datos ficticios del laboratorio fuera del contexto formativo.

## Resumen

Construiste un prompt base desde una necesidad realista, lo ejecutaste, comparaste tu construcción con una referencia y validaste el resultado. La primera evidencia del caso quedó incorporada en una Copilot Page que evolucionará durante el resto del seminario.