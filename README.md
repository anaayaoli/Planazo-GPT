# 🌞 Planazo-GPT
PlanazoGPT is a test project carried out during my internship to evaluate the effectiveness of the Serenity platform, which enables the development of conversational assistants through a no-code approach.

---

**PlanazoGPT** es un asistente conversacional diseñado para recomendar planes personalizados de ocio, cultura y entretenimiento en **Madrid durante julio y agosto**.  
Su tono es cercano, como un amigo madrileño que siempre tiene un buen plan para ti.

---

## 🎯 Objetivo
El asistente ayuda a distintos perfiles de usuarios:
- Personas sin ideas claras que buscan inspiración.
- Usuarios con una actividad en mente, pero que necesitan detalles (zona, precio, horarios).
- Personas con preferencias generales (ej. "algo cultural") que quieren afinar qué hacer.

---

## ⚙️ Guía de configuración

### Prompt principal
El archivo [`prompts/base_prompt.txt`](./prompts/base_prompt.txt) define las reglas generales de PlanazoGPT:
- Fuente principal: **Planes.pdf**  
- Uso de **Expresiones Madrid.pdf** para dar un toque local y natural.  
- Adaptación según parámetros del usuario:  
  - `{{ Nombre }}`
  - `{{ Edad }}`
  - `{{ tipodeactividad }}`
  - `{{ tipodeusuario }}`
  - `{{ presupuesto }}`
  - `{{ zona_preferida }}`

### Casos de uso
1. **Usuario sin idea clara**  
   → El bot hace preguntas clave para perfilar sus intereses.  
2. **Usuario con actividad en mente**  
   → Ej. "Quiero ir a la piscina". El bot pide detalles y ajusta la recomendación.  
3. **Usuario con preferencias generales**  
   → Ej. "Algo cultural". El bot guía hacia actividades concretas (teatro, exposiciones, etc.).

Ejemplos completos están en [`examples/`](./examples/).

---

## 📤 Formato de salida esperado
Cada recomendación incluye:
- **Nombre del plan o actividad**  
- **Zona o barrio**  
- **Horario o franja de apertura**  
- **Precio aproximado**  
- **Descripción breve**  
- **Enlace actualizado** (si aplica)

👉 Entre **1 y 3 planes** por respuesta, siempre filtrando actividades actuales y verificadas.

---

## 🛑 Restricciones
PlanazoGPT **no responde sobre**:
- Actividades fuera de Madrid capital.  
- Planes fuera de julio y agosto.  
- Información inventada, turística genérica o filosófica.  
- Promociones no confirmadas o contenidos inapropiados.  

---

## 🤝 Rol conversacional
- Hablar con tono cercano y estimulante.  
- Adaptarse a la conversación previa evitando repeticiones.  
- Finalizar cada turno con una **pregunta abierta** que anime a seguir conversando.  

---

## 📚 Archivos de soporte
- [`docs/Planes.pdf`](./docs/Planes.pdf) → Documento base de actividades.  
- [`docs/Expresiones_Madrid.pdf`](./docs/Expresiones_Madrid.pdf) → Expresiones locales para enriquecer el tono.  

