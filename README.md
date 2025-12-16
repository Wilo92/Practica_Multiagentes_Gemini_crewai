# Proyecto de Comparación de Sistemas Multiagente (MAS)

Este proyecto implementa un Sistema Multiagente (MAS) utilizando la librería CrewAI y el modelo de lenguaje Gemini (gemini-2.5-flash) para evaluar cómo la especialización del Agente (su rol, objetivo y contexto) afecta la calidad de la respuesta generada por la misma LLM.

El objetivo principal es comparar la calidad y pertinencia de las respuestas entre dos agentes con roles técnicos opuestos ante una misma consulta.

## Arquitectura del Sistema Multiagente

El Crew (equipo) está compuesto por dos agentes con roles técnicos específicos:

| Agente | Rol | Foco Principal |
| :--- | :--- | :--- |
| Agente Ciberseguridad | Experto en Seguridad Informática y Análisis de Riesgos. | Vulnerabilidades, Mitigación y Seguridad Defensiva. |
| Agente Software | Asesor experto en Desarrollo de Software. | Calidad de Código, Mantenibilidad, Eficiencia y Buenas Prácticas. |

Ambos agentes reciben la misma consulta de forma simultánea, lo que permite una comparación directa de la especialización de sus salidas.

## Metodología de Evaluación

La calidad de las respuestas se evaluó en una escala de 1 a 5, utilizando los siguientes criterios obligatorios:

* Claridad
* Pertinencia:
* Coherencia:Consistencia lógica del argumento.
* Utilidad: Valor práctico y aplicable de la información.

##  Configuración y Requisitos

El proyecto requiere la clave de API de Google Gemini.

1.  Entorno de Ejecución: El proyecto fue desarrollado en Google Colab para la gestión 
2.  **Dependencias:
    ```bash
    pip install crewai crewai_tools google-genai pandas numpy
    ```
3.  Clave API: La variable de entorno `GEMINI_API_KEY` debe cargarse desde la sección Secrets de Colab.

Creado por Wilmer Fidel Restrepo Orrego (WILO)