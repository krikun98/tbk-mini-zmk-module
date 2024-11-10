# TBK Mini ZMK Module

This repository contains the board files for the [TBK Mini](https://github.com/bastardkb/TBK-Mini) with the nice!nano adapter
to allow users to build firmware.
This can be done by adding the module to the west.yml found in your zmk-config's config directory. 
There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the TBK Mini module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: krikun98
      url-base: https://github.com/krikun98
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: tbk-mini-zmk-module
      remote: krikun98
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.

## Notes

The matrix pinout corresponds to the "adapter_v2" version in "https://github.com/cwebster2/zmk-config".
I have not added RBG support and do not plan to, but feel free to submit a PR.
