# 🖥️ pi-terminal-theme

Your terminal colors are fine. Stop overriding them.

This [pi](https://github.com/earendil-works/pi-mono/tree/main/packages/coding-agent)
package includes two terminal-first themes:

- `terminal` maps UI colors to ANSI `0..15`. That's the safe default.
- `terminal-tinted` also uses custom palette slots for message and tool
  backgrounds.

## 🚀 Installation

```sh
pi install npm:pi-terminal-theme
```

## ✨ Usage

Pick `terminal` in `/settings` → `theme`, or configure it in
`~/.pi/agent/settings.json`:

```json
{
  "theme": "terminal"
}
```

To opt in to tinted message and tool backgrounds, select `terminal-tinted`:

```json
{
  "theme": "terminal-tinted"
}
```

Project-specific settings can use the same `theme` key in `.pi/settings.json`.

## 🔄 No theme switcher needed

Because these themes use your terminal’s palette directly, they automatically
follow whatever your terminal is already using (light/dark, custom palettes,
scheduled changes, etc.).

That means you usually don’t need a separate theme switcher integration such as:

- https://github.com/mise42/pi-theme-sync
- https://github.com/ferologics/pi-system-theme

## 🎨 Tinted palette slots

The `terminal-tinted` theme treats palette slots `16..21` as package-specific
background colors:

| Slot | Theme use |
| --- | --- |
| `16` | Selected item background |
| `17` | Tool error background |
| `18` | Tool success background |
| `19` | Tool pending background |
| `20` | User message background |
| `21` | Custom message background |

These are not standard dim ANSI colors. If your terminal does not remap these
slots, it will use the built-in xterm 256-color cube, which can produce harsh
or unreadable backgrounds.

## 🧹 Uninstall

```sh
pi remove npm:pi-terminal-theme
```

## 📄 License

[MIT](LICENSE)
