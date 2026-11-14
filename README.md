<h1 align="center">Sval</h1>
<h3 align="center">A local video editor. Birch and slate, a quiet sea accent, no account.</h3>

Sval is a modified version of [Concat](https://github.com/jub0t/Concat) by Jareer Abdullah and Concat contributors. Same engine and project files. The name is the word for cool and composed in Swedish, Norwegian, and Danish. The window is built for that taste: a light birch ground, cool slate when the theme is dark, and a grey-blue accent instead of a loud one.

Concat © 2026 Jareer Abdullah and Concat contributors, [AGPL-3.0-or-later](LICENSE).

## What you see

- Window title, installers, and the default project folder are **Sval** (Desktop/Sval).
- The window opens on the **light** theme. Dark is a blue-grey night, still in Settings.
- Default accent is **Sea** (`#3d5c6e` on the light theme, `#7f9eae` on the dark theme).
- The About page states this lineage in the language of the interface.

The program file is still `concat` / `concat.exe`. Renaming the binary would break the build, the engine crates, and existing scripts.

## Build

Rust 1.93 or newer (`rust-version` in `src/Cargo.toml`), FFmpeg 7+ development libraries, cmake, and a C++ compiler.

- **macOS:** `brew install ffmpeg`
- **Windows:** a BtbN `win64-gpl-shared` FFmpeg build, with `FFMPEG_DIR` pointing at it
- **Linux:** the distro FFmpeg when it is 7 or newer, otherwise a BtbN `shared` build and `FFMPEG_DIR`

```sh
cd src
cargo run -p concat
```

Interface strings are checked with `python scripts/locales.py --check` from the repo root.
