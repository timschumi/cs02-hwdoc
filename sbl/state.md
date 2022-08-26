# State flags

## `RST_STAT`

- **Value 0x08**: Call Test Mode (PUMR)
- **Value 0x02**: Calibration Mode (PUMR)
- **Value 0x87**: Watchdog reset

## `INFORM3`

- `0x00000000`: Default/Reset
- `0x1234567?`: `?` is the `REBOOT_MODE`
  - `?` is `0x1`: Download mode
  - `?` is `0x6`: FOTA BL
- `0xabcd????`: `????` is the `DEBUG_LEVEL`
- `0xabcf????`: SUD mode, `????` is the SUD number
- `0xffffffff`: "set recovery mode for next boot"

During upload mode:
- `0x??????22`: Forced upload
- `0x??????2f`: User fault
- `0x??????c8`: Kernel panic
- `0x??????cc`: CP crash
- `0x??????dd`: HSIC disconnected
