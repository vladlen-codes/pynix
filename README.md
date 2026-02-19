# Pynecto
Modern Python GUI framework that enable you to build virtually any type of application from simple tools to production-grade systems.


## Project Structure
```
pynecto/
├── core/                        # C source — libpynecto
│   ├── pynecto.h                # Master header
│   ├── vdom.c / vdom.h
│   ├── layout.c / layout.h
│   ├── renderer.c / renderer.h
│   ├── events.c / events.h
│   ├── store.c / store.h
│   ├── arena.c / arena.h        # Memory management
│   └── backends/
│       ├── opengl/
│       ├── skia/
│       └── wasm/
│
├── bridge/                      # CPython C extension — _pynecto
│   ├── _pynecto.c
│   └── bindings.py
│
├── pynecto/                     # Python package
│   ├── __init__.py              # Clean public API surface
│   ├── component.py
│   ├── hooks.py                 # state, effect, memo, ref, context
│   ├── style.py
│   ├── router.py
│   ├── store.py
│   ├── context.py
│   ├── animation.py
│   └── widgets/
│       ├── __init__.py
│       ├── layout.py            # Stack, Grid, Flex, Scroll, Spacer
│       ├── input.py             # Button, TextInput, Checkbox, Slider, Select
│       ├── display.py           # Text, Image, Icon, Badge, Table, Chart
│       ├── overlay.py           # Modal, Tooltip, Drawer, Menu, Toast
│       └── media.py             # Video, Audio, Canvas
│
├── cli/                         # necto CLI
│   ├── main.py
│   ├── commands/
│   │   ├── new.py
│   │   ├── dev.py
│   │   ├── build.py
│   │   └── deploy.py
│   └── templates/               # necto new scaffolds
│       ├── default/
│       ├── dashboard/
│       └── minimal/
│
├── CMakeLists.txt
├── pyproject.toml
├── necto.toml                   # Framework-level defaults
└── README.md
