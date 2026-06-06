---
name: transcribe
description: Local speech-to-text transcription on Apple Silicon macOS. Supports wav directly and other audio formats via ffmpeg.
---

# Transcribe

Local speech-to-text using `parakeet-cpp-transcribe` on Apple Silicon macOS.

## Usage

```bash
{baseDir}/transcribe.sh <audio-file>
```

The first run downloads the macOS arm64 binary from the latest `badlogic/pibot` GitHub release into:

```text
~/.pi/tools/parakeet-cpp-transcribe/parakeet-cpp-transcribe
```

The binary downloads its GGUF model automatically if missing.

## Output

Plain text timestamped in 15 second chunks:

```text
[00:00-00:15] transcript text
[00:15-00:30] more transcript text
```

## Requirements

- Apple Silicon macOS only
- `curl` and `tar`
- `ffmpeg` for non-WAV input: `brew install ffmpeg`
