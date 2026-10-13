# Lane

Cross-API graphics backend — one abstraction, two lanes: **OpenGL** and **Vulkan**.

The goal is a single rendering back-end interface that can be driven by either a
legacy GL path or a modern Vulkan path, so the same client/renderer code can ship
on both without a second implementation of the scene layer.

> Status: scaffolding only — name, submodules and repo layout. No renderer code yet.

## Why "Lane"

Two parallel lanes, one road. The backends run side by side behind the same
interface, and a caller picks a lane at startup instead of at every call site.

## Layout

```
.
├── .dsh/          # harness-dotfiles (submodule) — agent rules & skills
├── 3rd/
│   └── Utils/     # Utils (submodule) — shared utilities
└── README.md
```

## Cloning

```sh
git clone --recursive git@github.com:TURIING/Lane.git
```

`Utils` carries its own nested submodules (`3rd/gtest`, `3rd/spdlog`). To pull
those as well:

```sh
git submodule update --init --recursive
```

## License

Not chosen yet.
