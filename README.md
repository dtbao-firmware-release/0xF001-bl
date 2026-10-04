# 0xF001-bl

Release channel for the **updater** (`app_updater`, OTA slot `ota_0`) of the ESP32-S3 RS-485
isolated gateway, product id `0xF001`.

Each release carries one file, the ChaCha20-encrypted application image `bl_*_enc.bin`,
built and published by the release workflow of
[esp32s3-rs485-iso-gateway-bl](https://github.com/dtbao-firmware/esp32s3-rs485-iso-gateway-bl).
The tag matches that repository's version (`vX.Y.Z`).

## Sibling channel

The product firmware (`app_firmware`, slot `ota_1`) is released separately in
[0xF001-fw](https://github.com/dtbao-firmware-release/0xF001-fw). One repository per app keeps
a separate "latest" release for each, and lets both use plain `vX.Y.Z` tags.

Both apps share the `cfg_setting` and `cfg_factory` partitions, so a release note states the
oldest sibling version it works with when that matters.

## Note

This repository was named `0xF001` until 2026-10-04. GitHub redirects the old URL here, so
never create a new repository called `0xF001`: that would break the redirect for units that
still point at it.

The source, build instructions and the full set of artefacts (bootloader, partition table,
`.elf`, plain `.bin`) live in the source repository, not here.
