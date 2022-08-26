# Environment Variables

## Indices

| Index | Name                          |
|-------|-------------------------------|
| `0x0` | [`REBOOT_MODE`](#reboot_mode) |
| `0x1` | `SWITCH_SEL`                  |
| `0x2` | `DEBUG_LEVEL`                 |
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

- `0x1`: Download mode
- `0x4`: Recovery mode
- `0x6`: FOTA BL
