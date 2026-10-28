# whisper-rs-sys 0.15.0, with the median filter fix

This is [whisper-rs-sys](https://codeberg.org/tazz4843/whisper-rs) 0.15.0 exactly as published on crates.io (Unlicense; whisper.cpp is MIT, see whisper.cpp/LICENSE), with one change: whisper.cpp's `median_filter` narrows the filter instead of aborting when a window has fewer audio tokens than the filter is wide. That's the fix merged in whisper.cpp as [ggml-org/whisper.cpp#4096](https://github.com/ggml-org/whisper.cpp/pull/4096), applied to the whisper.cpp copy this crate ships.

It's meant only as a stopgap through `[patch.crates-io]` until a whisper-rs release includes the fix:

```toml
[patch.crates-io]
whisper-rs-sys = { git = "https://github.com/Somnius/whisper-rs-sys", rev = "..." }
```
