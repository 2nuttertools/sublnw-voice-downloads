# SubLnw Voice downloads

Files the SubLnw Voice app (www.sublnw.com) downloads on its first start. There is no app code here, and
nothing to install by hand: the app fetches these itself and checks each file's SHA-256.

## Releases

- `runtime-1`: `sublnw-voice-runtime-1-mac-arm64.tar.gz`, the Python runtime for Mac (Apple silicon).
  SHA-256 `faf7e97bf5638e0e5a11d241b7a59653268de6df28f8f22556dcc08bc97b8adc`.

## What is inside the runtime, and its licences

Unmodified third-party open-source software, redistributed under their own licences:

| Part | Licence |
|---|---|
| CPython 3.11.16 (python-build-standalone 20260929) | PSF License (and the licences of its bundled libraries) |
| PyTorch 2.14.1, torchaudio 2.11.0 | BSD-3-Clause |
| NumPy 2.4.6 | BSD-3-Clause |
| transformers 5.20.1, huggingface_hub 2.2.0, safetensors 0.8.0 | Apache-2.0 |
| voxcpm 2.0.3 | Apache-2.0 |
| librosa 0.11.0 | ISC |
| soundfile 0.14.0 (with libsndfile) | BSD-3-Clause (libsndfile: LGPL-2.1) |
| einops, pydantic, tqdm, regex and their dependencies | MIT / Apache-2.0 / BSD / PSF |

Each package's own licence file is inside the runtime (`lib/python3.11/site-packages/*.dist-info/`).
The voice and speech models are not here: the app downloads them from their publishers on Hugging Face
(`openbmb/VoxCPM2`, Apache-2.0; `typhoon-ai/typhoon-whisper-turbo`, MIT).
