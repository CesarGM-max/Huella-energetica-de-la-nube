# Explicación del blueprint — Huella energética de la nube

El escenario de Make tiene **3 módulos** en línea. Se importa con **Import Blueprint** y hay que elegir/crear el webhook.

| # | Módulo | Qué hace |
|---|---|---|
| 1 | **Webhooks → Custom webhook** | Recibe el formulario que envía la página: `video, musica, redes, videollamadas, juegos, nube, ia, correos` (y `acciones` si se marca el reto opcional). |
| 2 | **Make AI Agent → Run an agent** | Recibe una línea por campo (`Video: {{1.video}} h/dia`, …). Su *system prompt* le pide estimar kWh, kg CO2e al año, suposiciones, quién paga el costo (externalidad) y 3 acciones, en texto plano. Usa la conexión *Make's AI Provider*. |
| 3 | **Webhooks → Webhook Response** | Responde `200` con `{{2.response}}` y los headers `Content-Type: text/plain; charset=utf-8` y `Access-Control-Allow-Origin: *` (este último permite que el navegador acepte la respuesta). |

## Estado
- El escenario se llama **Huella_Nube_Cesar** y está activo con **Immediately as data arrives**. La URL del webhook ya está en `WEBHOOK_URL` dentro de `index.html`.
- El *system prompt* usa el factor de emisión **0.444 kg CO2e por kWh** (Sistema Eléctrico Nacional 2024, SEMARNAT).
- Reto opcional: la casilla "Después de aplicar las 3 acciones" envía el campo `acciones=si`; el agente lo recibe en la última línea de su entrada y agrega la sección REDUCCION ESTIMADA.
