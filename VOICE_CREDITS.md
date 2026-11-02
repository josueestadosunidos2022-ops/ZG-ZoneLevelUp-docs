# Créditos de las voces de ZoneLevelUp r50

Los archivos OGG del cliente se generaron con [Piper](https://github.com/rhasspy/piper) y los modelos de [rhasspy/piper-voices](https://huggingface.co/rhasspy/piper-voices). Los modelos ONNX y el motor de síntesis no se incluyen en los JAR distribuidos.

- `es_ES-davefx-medium`: [ficha del modelo](https://huggingface.co/rhasspy/piper-voices/blob/main/es/es_ES/davefx/medium/MODEL_CARD), corpus CC0.
- `es_MX-claude-high`: [ficha del modelo](https://huggingface.co/rhasspy/piper-voices/blob/main/es/es_MX/claude/high/MODEL_CARD), corpus Apache 2.0.
- `es_ES-sharvard-medium`: [ficha del modelo](https://huggingface.co/rhasspy/piper-voices/blob/main/es/es_ES/sharvard/medium/MODEL_CARD), corpus [CC BY 3.0](https://creativecommons.org/licenses/by/3.0/), datos de la Universidad de Edimburgo. Créditos a sus autores originales según la ficha enlazada.

Las frases y relatos son texto original del proyecto ZoneLevelUp. 

## Narrador de GODIELAND — beta29-r50

Los 72 fragmentos de las cinemáticas son voz sintetizada en español latino con `es_MX-claude-high`, no grabaciones de un actor contratado ni una imitación de una persona específica. Se utiliza el modelo local ya citado, cuya ficha identifica el corpus bajo Apache 2.0. Se aplican una reducción moderada de tono (factor 0.94, formantes preservados), ecualización suave y normalización de voz. La naturalidad es una valoración auditiva; se entrega una muestra para revisión.

 Los modelos y motores no se distribuyen en el mod. El cliente reproduce audio incluido; no contacta servicios de voz ni sintetiza durante el juego. Solo los JAR de cliente incluyen el audio.
