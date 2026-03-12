# Download Manager — egui Progress Bar

Episode 15 of the **Learn egui in Neovim** series.

Build a download manager app with an animated progress bar, percentage display, and state-driven buttons.

## What You'll Learn

- `egui::ProgressBar::new()` — display progress from 0.0 to 1.0
- `.show_percentage()` — show the current value as text
- `.animate()` — add a shimmer effect while active
- `ctx.request_repaint()` — drive continuous animation each frame
- State-driven UI — conditional buttons and status text

## Run

```bash
cargo run
```

## Key Code

```rust
let bar = egui::ProgressBar::new(self.progress)
    .show_percentage()
    .animate(self.downloading);
ui.add(bar);

if self.downloading {
    ctx.request_repaint();
}
```

## Series

This is part of the [Learn egui in Neovim](https://www.youtube.com/@CelesteAI) series, where we build Rust GUI apps step by step.
