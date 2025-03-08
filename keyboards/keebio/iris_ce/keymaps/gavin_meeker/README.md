# General Guide for QMK

To use `c2json`

```shell
qmk c2json -km gavin_meeker -kb keebio/iris_ce/rev1 -o ./keyboards/keebio/iris_ce/keymaps/gavin_meeker/keymap.json
```

- `-km gavin_meeker`: this is looking in `keebio/iris_ce/rev/keymaps` folder for the folder `test`
- `-kb keebio/iris_ce/rev1`: this is the keyboard that is being targeted
- `-o`: this is the name of the output file

To `make` and flash to keyboard (**MAKE SURE THE KEYBOARD IS IN BOOT MODE**)

```shell
make keebio/iris_ce/rev1:gavin_meeker:flash
#                        ^^^^the name of they keymap in keymaps folder
```

- reference <https://github.com/qmk/qmk_firmware/tree/master/keyboards/keebio/iris_ce>

## Git Workflow

1. Fork
2. Clone your repo: `git clone git@github.com:user/qmk_firmware.git`
3. Add original repo as remote upstream: `git remote add upstream <git@github.com>:qmk/qmk_firmware.git`
4. Do your magic and push your work
5. When the original repo gets updated, do this:

```shell
git fetch upstream
git rebase upstream/master
git push -f
```
