# Temper ZMK Keyboard Module

This module provides ZMK support for the Temper keyboard.

## Usage

To use this module in your ZMK config, add it to your `config/west.yml`:

```yaml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: temper-zmk
      url-base: https://github.com/willthong
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: temper-zmk-config
      remote: temper-zmk
      revision: module
  self:
    path: config
```

Then in your build configuration, specify the shield:
- `temper_left` for the left side
- `temper_right` for the right side

