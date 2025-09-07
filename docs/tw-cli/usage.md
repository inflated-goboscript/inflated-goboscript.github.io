# Usage

`twcli run` <Project path\>

It only works on project files.

---

If you want to automatically supply inputs to `ask and wait` blocks, use the -i command:

`twcli run .\Project.sb3 -i "hi" "there`

This provides the arguments:
- `hi`
- `there`

If you want to disable headless mode (to see the browser), use `-H`:

`twcli run .\Project.sb3 -i "hi" "there" -H`

If you want to raise an error if the exit code is not `'0'`, use `-R`:

`twcli run .\Project.sb3 -i "hi" "there" -R`
