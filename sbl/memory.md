# Memory Ranges in SBL

| #  | Start          | End          | Flags? |
|----|----------------|--------------|--------|
| 0  | 0x00000000     | 0x02000000   | 0x12   |
| 1  | 0x02000000     | 0x34000000   | 0x00   |
| 2  | 0x34000000     | 0x40000000   | 0x12   |
| 3  | 0x80000000     | 0x81e00000   | 0x12   |
| 4  | 0x81e00000     | 0xb0000000   | 0x12   |
| 5  | 0xae200000     | 0xae580000   | 0x1e   |
| 6  | 0xae2000c8     | 0xae700000   | 0x12   |
| 7  | 0xae700000     | 0xae900000   | 0x1e   |
| 8  | 0xae900000     | 0xaeb00000   | 0x12   |
| 9  | 0x85000000     | 0x95000000   | 0x12   |

## Important addresses

| Address    | Purpose                         |
|------------|---------------------------------|
| 0x34051fe4 | `INFORM0`                       |
| 0x34051fe8 | `INFORM1`                       |
| 0x34051fec | [`INFORM2`](state.md#inform2)   |
| 0x34051ff0 | [`INFORM3`](state.md#inform3)   |
| 0x34051ff4 | `INFORM4`                       |
| 0x34051ff8 | [`INFORM5`](state.md#inform5)   |
| 0x34051ffc | `INFORM6`                       |
| 0x35004024 | [`RST_STAT`](state.md#rst_stat) |
| 0x81e08000 | Linux kernel entry address      |
| 0xae200000 | SBL binary mapping address      |
| 0xae900000 | Logging buffer                  |
