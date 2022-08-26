# Memory

## Memory Ranges in SBL

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

### Important addresses

| Address    | Purpose                    |
|------------|----------------------------|
| 0xae200000 | SBL binary mapping address |
| 0xae900000 | Logging buffer             |
