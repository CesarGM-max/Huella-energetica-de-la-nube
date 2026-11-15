# Práctica 4.3 — Huella energética de la nube

- **Alumno:** Cesar Jesus Gamez Mendoza
- **Materia:** Desarrollo Sustentable (ACD-0908)
- **Profesor:** Mtro. Miguel Ángel Barrón Hernández
- **Institución:** Tecnológico Nacional de México — Campus Mazatlán

## Descripción
Página web donde cada persona captura su uso digital (video, música, redes, videollamadas, juegos, nube, IA y correos). La página envía los datos a un webhook de Make, un agente de IA estima la energía y las emisiones que provoca ese uso, explica quién paga ese costo (externalidad) y propone 3 acciones para reducirlo. El resultado se muestra en la misma página.

**Flujo:** Página web → Webhook de Make → Make AI Agent → Webhook Response → Página web.

## Objetivo
Reconocer el consumo energético de los servicios digitales como un costo externalizado, estimar la huella digital propia con apoyo de IA y evaluar críticamente sus suposiciones.

## Material utilizado
- Computadora con navegador y celular (tiempo de pantalla)
- Cuenta de Make (conexión *Make's AI Provider*)
- Repositorio de GitHub con GitHub Pages

## Código
- [`Codigo/blueprint.json`](Codigo/blueprint.json): escenario de Make exportado (importable con *Import Blueprint*).
- [`Codigo/Explicacion del blueprint.md`](Codigo/Explicacion%20del%20blueprint.md): explicación módulo por módulo.
- [`Codigo/index.html`](Codigo/index.html): página web de la práctica.

## Imágenes
<!-- Captura del escenario completo en Make, ordenado y con los 3 módulos visibles -->
<!-- Captura de la página con tus resultados -->

## Video
[`Video/enlace.txt`](Video/enlace.txt)

## Resultados
[`Resultados/Resultados.pdf`](Resultados/Resultados.pdf)

## Conclusiones
Ver la conclusión y las respuestas a las 5 preguntas en [`Resultados/Resultados.pdf`](Resultados/Resultados.pdf).

Factor de emisión usado: 0.444 kg CO2e/kWh (Sistema Eléctrico Nacional 2024, SEMARNAT). Energía de streaming: IEA 0.077 kWh/h vs. Shift Project 0.8 kWh/h.
