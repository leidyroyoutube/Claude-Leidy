# Claude-Leidy

Repositorio para hacer vídeos de YouTube. Responde en español.

## Skills de YouTube

`.claude/skills/yt-*` son las 11 skills de
[youtube-agent-skill](https://github.com/Jakeschincariol/youtube-agent-skill) (MIT, commit `a2feb21`),
copiadas sin cambios. Todas leen `~/.claude/youtube/voice.md`, que el setup script del entorno enlaza a
`youtube/voice.md` de este repositorio. Si el enlace no existe, créalo:

```bash
mkdir -p ~/.claude/youtube && ln -sf "$(pwd)/youtube/voice.md" ~/.claude/youtube/voice.md
```

Los cambios del perfil se guardan en `youtube/voice.md`: haz commit de ese archivo.

## Herramientas

- **faster-whisper** (`requirements.txt`): transcripción. Los modelos se descargan de Hugging Face la
  primera vez. Las skills `yt-edit`, `yt-chapters`, `yt-shorts` y `yt-retention` aceptan su salida (srt, vtt
  o json).
- **Remotion** (`remotion-video/`): en la nube, renderiza siempre con
  `--browser-executable=/opt/pw-browsers/chromium_headless_shell`, porque `remotion.media` está bloqueado.
- **ffmpeg**: para aplicar los cortes de `yt-edit` y recortar Shorts.

No subas vídeos ni audios grandes al repositorio: GitHub rechaza archivos de más de 100 MB. Los renders
van en `remotion-video/out/`, que está en `.gitignore`.
