# Using WAV Channel Toolkit

## Quick start

Build, then run `./wav-toolkit left examples/demo.wav left.wav` or `./wav-toolkit reverse examples/demo.wav reversed.wav`. Existing output files are rejected.

## Supported workflow

1. PCM16 mono/stereo RIFF chunk parsing.
2. Frame-preserving reverse and left/right extraction.
3. New-file output with overwrite protection.

## Validation and troubleshooting

Run the commands in the README. Invalid inputs produce explicit errors rather than silently changing the requested operation. Browser audio requires a user gesture; microphone apps require HTTPS or localhost and permission. For file tools, supply supported input formats and writable output directories.

## Limitations

PCM16 mono/stereo only; files are loaded into memory. Does not decode compressed audio or preserve ancillary RIFF metadata.

Tests use synthetic fixtures. These tests do not certify hardware compatibility, real-world forecast quality, trained-model accuracy, or production suitability for every input.
