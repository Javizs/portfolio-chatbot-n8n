# Chatbot IA para portfolio web (n8n + OpenAI)

Chatbot conversacional integrado en un portfolio personal para ayudar a recruiters
a conocer el perfil, proyectos y enfoque profesional del desarrollador.

El bot está diseñado para responder de forma clara, breve y honesta,
priorizando proyectos reales y evitando exageraciones técnicas.

---

## Tecnologías utilizadas

- n8n (self-hosted en VPS Linux)
- OpenAI (modelo GPT-4.1-mini)
- Webhooks públicos
- LangChain (AI Agent + Memory)
- HTML / CSS / JavaScript (frontend)

---

## Arquitectura general

1. El frontend web envía mensajes mediante un Chat Trigger (webhook).
2. n8n gestiona la sesión con `sessionId` personalizado.
3. Se aplica memoria conversacional con ventana limitada.
4. El agente IA responde según un prompt diseñado para recruiters.
5. La respuesta se devuelve al frontend en formato JSON.

---

## Memoria y contexto

El bot utiliza `Window Buffer Memory` con una ventana de contexto limitada
para mantener coherencia sin aumentar costes innecesarios.

---

## Prompt del asistente

El prompt está diseñado para:

- Responder en 3–6 líneas por defecto
- No inventar experiencia
- Usar proyectos reales como ejemplo
- Mantener tono profesional y cercano
- Adaptarse al idioma del usuario

---

## Estado del proyecto

✔ Funcional  
✔ Integrado en web real  
✔ Usado como herramienta profesional en portfolio  

Este repositorio documenta el flujo y la arquitectura.
El backend n8n y las credenciales no se publican por seguridad.
