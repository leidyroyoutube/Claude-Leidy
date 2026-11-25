# Claude-Leidy
Conectar Repositorio con Claude

## Contenido

- `remotion-video/`: proyecto de [Remotion](https://www.remotion.dev) (plantilla Hello World).
- `requirements.txt`: dependencias de Python para transcribir con faster-whisper.

## Remotion

```bash
cd remotion-video
npm install
npm run dev
```

Para renderizar un vídeo:

```bash
npx remotion render HelloWorld out/HelloWorld.mp4
```

En las sesiones de Claude Code en la nube, Remotion no puede descargar su navegador; usa el que ya trae el contenedor:

```bash
npx remotion render HelloWorld out/HelloWorld.mp4 --browser-executable=/opt/pw-browsers/chromium_headless_shell
```

## faster-whisper

```bash
pip install -r requirements.txt
```

Los modelos se descargan de Hugging Face la primera vez que se usan.
