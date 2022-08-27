# State registers

## `RST_STAT`

- **Value 0x08**: Call Test Mode (PUMR)
- **Value 0x02**: Calibration Mode (PUMR)
- **Value 0x87**: Watchdog reset

## `INFORM2`

- `0x00000000`: Default/Reset
- `0x12345678`: Normal reset

## `INFORM3`

- `0x00000000`: Default/Reset
- `0x1234567?`: `?` is the [`REBOOT_MODE`](env.md#reboot_mode)
- `0xabcd????`: `????` is the [`DEBUG_LEVEL`](env.md#debug_level)
- `0xabcf????`: SUD mode, `????` is the SUD number
- `0xffffffff`: "set recovery mode for next boot"

During upload mode:
- `0x??????22`: Forced upload
- `0x??????2f`: User fault
- `0x??????c8`: Kernel panic
- `0x??????cc`: CP crash
- `0x??????dd`: HSIC disconnected

## `INFORM5`

- `0xbdbd????`: `????` overrides the Board revision

## "State Flags"

The "State Flags" at address `0xae2a0044` get used to control the boot mode and state of the current boot.

| Bit | Value   | Purpose       |
|-----|---------|---------------|
| 0   | 0x1     | Odin Flag     |
| 1   | 0x2     | Error Flag    |
| 2   | 0x4     | Factory Flag  |
| 16  | 0x10000 | Upload Mode   |
| 17  | 0x20000 | Download Mode |
| 18  | 0x40000 | LPM Mode      |
| 19  | 0x80000 | Recovery Mode |
