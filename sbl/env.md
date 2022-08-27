# Environment Variables

## Indices

| Index | Name                          |
|-------|-------------------------------|
| `0x0` | [`REBOOT_MODE`](#reboot_mode) |
| `0x1` | `SWITCH_SEL`                  |
| `0x2` | [`DEBUG_LEVEL`](#debug_level) |
| `0x3` | `KERNEL_LOG_LEVEL`            |
| `0x4` | `SUD_MODE`                    |
| `0x5` | `DN_ERROR`                    |
| `0x6` | `CHECKSUM`                    |
| `0x7` | `INT_RSVD6`                   |
| `0x8` | `INT_RSVD7`                   |
| `0x9` | `INT_RSVD8`                   |
| `0xa` | `INT_RSVD9`                   |
| `0xb` | `CMDLINE`                     |
| `0xc` | `STR_RSVD1`                   |
| `0xd` | `STR_RSVD2`                   |

## Memory Format

### Integer Environment Variables

Integer Environment Variables take 4 bytes of space.

### String Environment Variables

String Environment Variables have space for up to 400 bytes. The data appears to be expected to be null-terminated.

## Variables

### `REBOOT_MODE`

- `0x1`: Download mode (`sec_debug.reset_reason=0x1A2B3C00`)
- `0x2`: ? (`sec_debug.reset_reason=0x1A2B3C04`)
- `0x3`: ? (`sec_debug.reset_reason=0x1A2B3C10`)
- `0x4`: Recovery mode (`sec_debug.reset_reason=0x1A2B3C11`)
- `0x5`: ? (`sec_debug.reset_reason=0x1A2B3C12`, `bootmode=3` when not booting recovery)
- `0x6`: FOTA BL (`sec_debug.reset_reason=0x1A2B3C05`)

If none of the values match, `sec_debug.reset_reason=0x1A2B3C00` is set.

### `DEBUG_LEVEL`

- `0x4948`: Sets `sec_debug.level=0x10001` on the kernel cmdline. Sets `magc_ram_base` to `0x66262564`.
- `0x494d`: Sets `sec_debug.level=1` on the kernel cmdline. Sets `magc_ram_base` to `0x66262564`.
- `0x4f4c`: ?
- `0x5541`: Sets `sec_debug.level=1` on the kernel cmdline.
