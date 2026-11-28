# Claude-Leidy
Conectar Repositorio con Claude

## Contenido

- `remotion-video/`: proyecto de [Remotion](https://www.remotion.dev) (plantilla Hello World).
- `requirements.txt`: dependencias de Python para transcribir con faster-whisper.
- `.claude/skills/`: las 11 skills de [youtube-agent-skill](https://github.com/Jakeschincariol/youtube-agent-skill)
  (`/yt-script`, `/yt-package`, `/yt-edit`, `/yt-shorts`, `/yt-retention`, `/yt-viral`…). Licencia MIT.
- `youtube/voice.md`: tu perfil de estilo, que leen todas las skills. Rellénalo.

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
