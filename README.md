# WAV Channel Toolkit

Split PCM16 stereo recordings into mono channels or reverse frames without corrupting channel order.

**Language:** C++ · **License:** MIT · **Data:** Local by default

## What it does

- PCM16 mono/stereo RIFF chunk parsing
- Frame-preserving reverse and left/right extraction
- New-file output with overwrite protection

## Requirements

A C++17 compiler (g++ or clang++).

## Install, validate, and run

```sh
g++ -std=c++17 -O2 -Wall -Wextra main.cpp -o wav-toolkit
./wav-toolkit --self-test
python3 examples/make_fixture.py
./wav-toolkit reverse examples/demo.wav reversed.wav
```

Run `--help` where supported, or follow the examples in [docs/usage.md](docs/usage.md). Input files are never overwritten unless explicitly documented.

## Usage and examples

See [docs/usage.md](docs/usage.md) for a walkthrough and [docs/architecture.md](docs/architecture.md) for implementation details. Tests are deterministic and do not require an exchange, paid API, external model, microphone, or private data.

## Boundaries

PCM16 mono/stereo only; files are loaded into memory. Does not decode compressed audio or preserve ancillary RIFF metadata.

## Privacy

No analytics or accounts are built in. Local file tools process only the paths you supply. For model-server and weather apps, the interface and usage guide identify the destination and the data sent. Do not commit personal input files, model credentials, or generated recordings.

## Development

Run the validation commands above before submitting changes. GitHub Actions runs these checks on pushes and pull requests. See the workflow for the reproducible toolchain. A successful workflow verifies the tested paths; manual audio-device behavior is documented separately.
