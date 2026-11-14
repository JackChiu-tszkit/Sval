<h1 align="center">Sval</h1>
<h3 align="center">本地视频剪辑。桦木色浅底，冷灰蓝强调色，不用账号。</h3>

Sval 是 [Concat](https://github.com/jub0t/Concat) 的修改版本，原作为 Jareer Abdullah 与 Concat 贡献者。剪辑引擎和项目文件沿用 Concat。这个名字在瑞典语、挪威语、丹麦语里是“清凉、从容”。界面按北欧习惯来：默认浅色桦木底，深色是蓝灰，强调色是克制的海灰蓝。

Concat © 2026 Jareer Abdullah 与 Concat 贡献者，[AGPL-3.0-or-later](../LICENSE)。

## 你会看到的

- 窗口标题、安装包、默认项目文件夹都叫 **Sval**（桌面上的 Sval）。
- 打开就是**浅色**。深色是蓝灰，仍可在设置里切换。
- 默认强调色是 **海**（浅色主题 `#3d5c6e`，深色主题 `#7f9eae`）。
- 关于页会写明上述来源。

程序文件仍叫 `concat` / `concat.exe`。可执行文件名留着，是为了构建、引擎和已有脚本还能对上。

## 编译

需要 Rust 1.93 或更新（见 `src/Cargo.toml` 的 `rust-version`）、FFmpeg 7+ 开发库、cmake 和 C++ 编译器。

- **macOS：** `brew install ffmpeg`
- **Windows：** BtbN 的 `win64-gpl-shared` FFmpeg，把 `FFMPEG_DIR` 指到解压目录
- **Linux：** 发行版自带的 FFmpeg 若已是 7 或更新即可，否则用 BtbN 的 `shared` 构建并设置 `FFMPEG_DIR`

```sh
cd src
cargo run -p concat
```

界面文案用仓库根目录的 `python scripts/locales.py --check` 检查。
