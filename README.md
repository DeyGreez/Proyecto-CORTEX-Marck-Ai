# Proyecto-CORTEX-Marck-AI
# Mision: Asistente AI diseñado para la ayuda de medico optométricos 
# Integrantes: Juan David Leal Carmona, Erick Fabian Cardenas Bello
# 1.Perfil del Agente
<img width="1238" height="777" alt="Captura de pantalla 2026-02-19 105853" src="https://github.com/user-attachments/assets/3a1c5006-5e7f-425c-99cd-aa173eb01626" />

# 2.Grafico de Radar del Agente

<img width="1575" height="806" alt="Captura de pantalla 2026-02-26 102949" src="https://github.com/user-attachments/assets/88da2547-6d66-40b3-811e-93056ca8a101" />

# Argumentaciòn del porque de estos Valores:

Atención = 10
Porque en medicina no se puede distraer. O sea, un pequeño error en una graduación o en un dato del paciente puede afectar el tratamiento. Entonces el sistema tiene que fijarse en todo, hasta en los detalles pequeños. No puede estar “medio atento”, tiene que estar full concentrado.

Memoria = 10
También necesita recordar el historial del paciente, las consultas pasadas, si tiene diabetes, si toma medicamentos, cosas así. Si no recuerda eso, podría dar una recomendación mal. Entonces la memoria tiene que estar al máximo porque la consulta no es solo lo que pasa en ese momento, sino todo lo que viene de antes.

Lenguaje = 10
Esto es importante porque el asistente tiene que explicar cosas técnicas de forma clara. No todos los pacientes entienden términos médicos. Además, tiene que ayudar a redactar informes bien hechos. Si se comunica mal, puede haber confusiones, y en salud eso es grave.

Emoción = 2
Aquí es donde cambia la cosa. No queremos que la IA tome decisiones por emoción. No debería “sentir lástima” o exagerar algo porque suena grave. Tiene que ser objetiva. Pero tampoco cero emoción total, porque si responde súper fría puede parecer rara. Entonces un nivel bajo está bien: un poco humano, pero sin que afecte las decisiones.

En resumen, el agente está pensado para ser súper fuerte en lo técnico (atención, memoria y lenguaje), pero mantener la emoción controlada para que no interfiera. O sea, que piense como profesional, no como alguien que se deja llevar por lo que siente.


# Inputs Brainstrom 

<img width="1919" height="881" alt="Captura de pantalla 2026-03-12 104457" src="https://github.com/user-attachments/assets/28169808-3693-4b0a-b148-7bc76b88be57" />

# El Flujo Del Procesamiento 

Procesamiento
Arriba-Abajo (TopDown) y Patrones

![image](https://github.com/user-attachments/assets/fb3b0ad1-802d-4949-bf88-ac8d16b323d7)

Miro:


<img width="1020" height="865" alt="Captura de pantalla 2026-03-19 100023" src="https://github.com/user-attachments/assets/26ee89a2-dfd1-4399-ae0b-449d097350a2" />

# El Filtro de Atenciòn

Atenciòn selectiva y Carga Cognitiva

![ollEG](https://github.com/user-attachments/assets/acffaa02-67b9-4d5c-b9f8-e71a948a318c)

Miro:

<img width="1014" height="853" alt="Captura de pantalla 2026-03-19 100733" src="https://github.com/user-attachments/assets/65632649-5872-4aef-9f65-2867c1560a23" />

# El Disco Duro

Memoria a Largo Plazo (LTM): Semántica y Episódica.


![BaHL0](https://github.com/user-attachments/assets/e34a2578-4085-4d90-8591-89b653a0a6b8)

| Carpeta / Categoría                  | Tipo de Memoria     | Descripción                                                                 | Ejemplos para Mark-AI (Optometría)                              |
|--------------------------------------|---------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------|
| Anatomía y Fisiología Ocular         | Semántica           | Conceptos básicos y hechos permanentes del ojo y sistema visual            | Estructura de retina, cristalino, nervio óptico, vías visuales |
| Fórmulas y Cálculos Optométricos     | Semántica           | Ecuaciones y constantes clínicas que nunca cambian                         | Fórmula de lensmaker, Snellen, equivalentes esféricos, dioptrías |
| Patologías y Diagnósticos            | Semántica           | Enfermedades, signos y criterios diagnósticos                              | Miopía, hipermetropía, astigmatismo, glaucoma, catarata        |
| Protocolos y Guías Clínicas          | Semántica           | Procedimientos estandarizados y mejores prácticas                          | Examen refractivo completo, normas de prescripción, ISO 9001   |
| Catálogo de Lentes y Productos       | Semántica           | Información técnica de materiales y tratamientos                           | Tipos de lentes (monofocales, progresivos, fotocromáticos)     |
| Leyes y Regulaciones                 | Semántica           | Normativa legal y ética en salud ocular                                    | Leyes colombianas de optometría, consentimiento informado      |
| Historial Clínico (anonimizado)      | Episódica           | Casos y evoluciones de pacientes (solo patrones y lecciones aprendidas)    | Seguimientos de graduación, respuestas a tratamientos          |
| Investigación y Avances              | Semántica           | Estudios científicos y evidencia actualizada                               | Últimos papers sobre IA en optometría, nuevas tecnologías      |

Miro:

<img width="1511" height="876" alt="Opera Instantánea_2026-03-26_103039_miro com" src="https://github.com/user-attachments/assets/37800a0e-7f5f-4554-8808-adf057dc030b" />


# La Ram Cognitiva

Memoria de Trabajo y Carga Cognitiva (El número mágico 7±2).

![36ykO](https://github.com/user-attachments/assets/cb5822c9-5412-429d-8879-803a8c1ef751)

| Componente                  | Descripción                                                                 | Límite Recomendado          | Razón (Carga Cognitiva)                                      |
|-----------------------------|-----------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------|
| Ventana de Contexto         | Memoria de Trabajo / RAM Cognitiva del bot                                  | 7 ± 2 mensajes / turnos     | Número mágico de Miller (evita sobrecarga cognitiva)        |
| Mensaje actual              | Consulta o mensaje más reciente del usuario                                 | Siempre incluido            | Prioridad máxima (Atención = 10)                            |
| Mensajes anteriores         | Historial inmediato de la conversación                                      | Hasta 6 mensajes previos    | Mantiene contexto clínico reciente sin saturar la RAM       |
| Mensajes descartados        | Mensajes que salen de la ventana                                            | A partir del mensaje -8     | Se archivan en Memoria a Largo Plazo (LTM)                  |
| Límite superior             | Máximo de tokens / mensajes retenidos                                       | 7 ± 2                       | Evita olvido del inicio de la consulta y sobrecarga         |
| Recuperación desde LTM      | Cuando se necesita información antigua                                      | Solo si es relevante        | Se activa mediante Memoria=10 (Top-Down)                    |

**Notas de la Ventana de Contexto:**
- El bot mantiene **solo los últimos 7 ± 2 mensajes** en Memoria de Trabajo.
- Superado el límite, los mensajes más antiguos se descartan automáticamente de la RAM.
- La información antigua sigue disponible mediante la Memoria a Largo Plazo (LTM).
- Esto equilibra precisión clínica, atención selectiva y eficiencia computacional.

Miro:

<img width="1524" height="867" alt="Opera Instantánea_2026-03-26_103414_miro com" src="https://github.com/user-attachments/assets/afd912d5-8a30-4528-b8ad-df3638396b73" />

# El Bilbliotecario

Procesos de recuperacion y olvido

| Paso | Fase del Flujo                          | Descripción                                                                 | Acción del Bot                                      | Componente Usado                  | Nota / Regla                          |
|------|-----------------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------|---------------------------------------|
| 1    | Entrada de Pregunta                     | Recibe la consulta del usuario (Fase 2)                                     | Aplica Gatekeeper (filtro de ruido)                | Atención Selectiva = 10           | Filtra todo lo no clínico             |
| 2    | Verificación en Contexto Inmediato      | Revisa si la información ya está disponible                                 | Busca dentro de la Ventana de Contexto             | RAM Cognitiva (7 ± 2 mensajes)    | Si está → Responder directamente      |
| 3    | Búsqueda en Memoria Permanente          | Si no está en RAM, consulta la base de conocimiento                        | Recupera datos relevantes usando patrón Top-Down   | LTM (Memoria a Largo Plazo)       | Memoria = 10 + Atención = 10          |
| 4    | Recuperación y Priorización             | Extrae solo la información útil y actual                                    | Prioriza entidades clínicas y contexto histórico   | Lenguaje = 10                     | Evita sobrecarga cognitiva            |
| 5    | Integración y Respuesta                 | Combina contexto reciente + conocimiento recuperado                         | Genera respuesta objetiva y precisa                | Procesamiento final               | Emoción = 2 (siempre objetivo)        |

**Regla de Olvido (Documentada en GitHub - README.md)**

- **Condición**: Si pasan **10 minutos de inactividad** en la conversación.
- **Acción**: Limpiar completamente la Ventana de Contexto (RAM Cognitiva).
- **Consecuencia**: Los mensajes antiguos salen de la RAM, pero permanecen seguros y accesibles en LTM.
- **Objetivo**: Evitar sobrecarga cognitiva, reducir consumo de tokens y garantizar privacidad de datos del paciente.

cuadro:

![image](https://github.com/user-attachments/assets/715b8177-2016-4d00-b812-4b516f329ba0)

miro:

<img width="1920" height="1032" alt="Captura de pantalla 2026-04-09 103944" src="https://github.com/user-attachments/assets/cb82fb0e-fd50-4be7-845d-049a321041dd" />

#Semana 16 El Motoro De La Motivación

## 6. Sistema de Motivación y Emoción

### Función Objetivo (Reward Function) de Mark-AI

**Misión Principal del Agente:**  
Maximizar la **calidad clínica** y la **satisfacción del usuario** mientras se mantiene un alto estándar de precisión y seguridad en salud visual.

**Prioridad Numérica (Jerarquía de Motivación):**

1. **Prioridad Máxima (Nivel 1)**: Precisión clínica y seguridad del paciente  
   (Nunca comprometer la salud visual por velocidad)

2. **Prioridad Alta (Nivel 2)**: Calidad de la explicación y empatía controlada  
   (Explicar claramente y validar emociones del usuario)

3. **Prioridad Media (Nivel 3)**: Eficiencia  
   (Responder de forma oportuna, pero nunca a costa de la calidad)

**Regla de Equilibrio (Resolución de Dilemas):**

> "Mark-AI prioriza siempre la **Calidad y Seguridad** sobre la Velocidad.  
> Si detecta frustración, confusión o malestar emocional en el usuario, ignorará límites de tiempo y dedicará los recursos necesarios para validar el sentimiento, explicar con mayor detalle y ofrecer soluciones alternativas."

**Métricas de Éxito:**
- Precisión clínica ≥ 95%
- Satisfacción percibida del usuario
- Tasa de escalamiento a humano (solo cuando sea necesario)
- Cumplimiento del Protocolo Anti-Sesgos y de Seguridad Emocional

#Semana 17 La Matriz De Empatía

<img width="1168" height="784" alt="imagen" src="https://github.com/user-attachments/assets/00d7f363-b814-460e-8f03-a25f2b1ab8dd" />

#Semana 18 Cierre Del Sistema

## Entregable Final - Blueprint Completo de Mark-AI

**Repositorio GitHub - Estructura Final:**

### 1. Portada y Misión (Fase 1)
- Título, descripción y radar del agente (Atención=10, Memoria=10, Lenguaje=10, Emoción=2)

### 2. Percepción y Sensores (Fase 2)
- Inputs Crudos vs Interpretados
- Flujo Top-Down

### 3. Memoria (Fase 3)
- Tabla de Estructura de Memoria (Semántica y Episódica)
- Ventana de Contexto (7±2)

### 4. Personalidad y Comunicación (Fase 4)
- Guía de estilo y tono

### 5. Cerebro Lógico (Fase 5)
- Árbol de Decisión
- Protocolo Anti-Sesgos (Sesgo de Confirmación)

### 6. Corazón - Motivación y Seguridad (Fase 6)
- Función Objetivo y Prioridades
- Protocolo de Seguridad Emocional (Manejo de Crisis)
- Regla de Olvido (10 minutos)

**Estado Final:** Repositorio completo, organizado y listo para presentación.


