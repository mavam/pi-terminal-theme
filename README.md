# 🖥️ pi-terminal-theme

Your terminal colors are fine. Stop overriding them.

This [pi](https://github.com/badlogic/pi-mono/tree/main/packages/coding-agent)
theme maps UI colors to ANSI `0..15`. That's it.

## 📦 Install

```bash
pi install npm:pi-terminal-theme
```

## 🎨 Use

Pick `terminal` in `/settings` → `theme`, or:

```json
{
  "theme": "terminal"
}
```

## 🔄 No theme switcher needed

Because this theme uses your terminal’s ANSI palette directly, it automatically
follows whatever your terminal is already using (light/dark, custom palettes,
scheduled changes, etc.).

That means you usually don’t need a separate theme switcher integration such as:

- https://github.com/mise42/pi-theme-sync
- https://github.com/ferologics/pi-system-theme

## 📄 License

[MIT](LICENSE)
