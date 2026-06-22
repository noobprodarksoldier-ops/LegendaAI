# 🎬 LegendaAI

Legenda em tempo real flutuando sobre qualquer app (YouTube, Twitch, etc).

## Como funciona

```
Áudio → SpeechRecognizer → ML Kit Translate → Overlay Window
```

## Fases de desenvolvimento

| Fase | STT | Status |
|------|-----|--------|
| Phase 1 | SpeechRecognizer (microfone) | ✅ Atual |
| Phase 2 | AudioPlaybackCapture → Whisper/Vosk | 🔜 Próxima |

Na Phase 1 o app usa o microfone do celular — funciona se o som estiver no alto-falante.  
Na Phase 2 vai capturar o áudio diretamente do YouTube/Twitch sem precisar de alto-falante.

## Build via GitHub Actions

1. Faça fork/push deste repo no GitHub  
2. Vá em **Actions → Build APK → Run workflow**  
3. Baixe o APK em **Artifacts → LegendaAI-debug**

## Permissões necessárias no celular

- **Aparecer sobre outros apps** — para a janela de legenda flutuante  
- **Microfone** — para o reconhecimento de voz (Phase 1)  
- **Projeção de mídia** — solicitada ao iniciar (necessária para Phase 2)  

## Stack

- Kotlin + Android SDK 29+  
- ML Kit Translate (on-device, offline após 1º download)  
- WindowManager (overlay)  
- SpeechRecognizer (Phase 1 STT)  

## Idiomas suportados

Inglês, Português, Espanhol, Japonês, Coreano, Francês

---

*by NoxProducao*
