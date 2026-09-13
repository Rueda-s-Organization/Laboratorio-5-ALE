# Laboratorio 5 - Agentes en el Arcade Learning Environment (ALE): Space Invaders

Fernando Rueda - 23748

CC3092 Deep Learning y Sistemas Inteligentes.

Investigación del Arcade Learning Environment y de los espacios de observación y acción de los entornos de Atari, más un módulo reutilizable para crear entornos, ejecutar agentes y grabar video de las partidas. No se entrena un agente inteligente, el objetivo es dejar funcionando la infraestructura para que un agente simple (aleatorio o de regla fija) interactúe con `ALE/SpaceInvaders-v5` y genere un video del juego.

## Contenido

- `Laboratorio5_ALE_SpaceInvaders.ipynb`, notebook con la investigación de ALE, la investigación de los espacios de observación y acción, el módulo de funciones (`crear_entorno`, `agente_aleatorio`, `agente_regla_simple`, `ejecutar_episodio`, `generar_video_agente`), la generación de los videos y la discusión.
- `videos/`, videos `.mp4` de los episodios grabados en Space Invaders, en una subcarpeta por agente (`videos/aleatorio` y `videos/regla_simple`).
- `requirements.txt`, dependencias de Python.

El informe escrito de máximo tres páginas se entrega aparte en PDF.

## Cómo ejecutar

```bash
python3.10 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook Laboratorio5_ALE_SpaceInvaders.ipynb
```

Las ROM de Atari vienen incluidas con `ale-py`, no hace falta descargarlas aparte. El grabado de video usa `RecordVideo` con el ffmpeg que trae `imageio-ffmpeg`, por lo que no se necesita un ffmpeg del sistema. El notebook fija semillas para que los resultados sean reproducibles.
