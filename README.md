# Agente Mejoras Conversación — Ecosistema Qualitas/Insurmind

Agente de análisis de conversaciones WhatsApp. Nivel 3 del ecosistema multi-agente Insurmind.

## Qué hace

Lee conversaciones históricas de Heroku Postgres y produce informes Markdown con:
- Mapa de abandono por fase del funnel WhatsApp
- Análisis de copy de los mensajes del bot antes del silencio del lead
- Hasta 5 recomendaciones priorizadas para mejorar la tasa de respuesta

## Qué NO hace

- No envía mensajes a leads
- No detecta leads automáticamente
- No escribe en ningún sistema externo (n8n, Django, Meta)

## Uso

1. Abre este repo como proyecto Claude Code
2. Configura `DATABASE_URL` en las variables de entorno del proyecto (credencial `readonly_leads` de Heroku `hyl-wai-production`)
3. Dile al agente: "Analiza las conversaciones del [fecha inicio] al [fecha fin]"

El informe se guarda en `informes/YYYY-MM-DD-analisis.md`.

## Posición en el ecosistema

```
ARQUITECTO (Nivel 2)
       ↑
  Alberto lleva los hallazgos
       ↑
AGENTE MEJORAS CONVERSACION (este agente, Nivel 3)
  Lee Postgres → analiza → escribe informe
```
