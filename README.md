# Catthode for Gemini CLI

<p align="center">
  <img src="https://cattho.de/assets/icon.png" alt="Catthode Icon" width="128" />
</p>

> **From CRT to OLED.** Bringing warmth back to a world of cold themes. [cattho.de](https://cattho.de/)

Catthode is a high-contrast, retro-futuristic theme designed for prolonged coding sessions. It blends the crushed blacks of modern OLED displays with the comforting, warm glow of analog tungsten filaments.

## 🎨 Color Palette

### Surface
| Color | Hex | Role |
| :--- | :--- | :--- |
| **Base** | `#000000` | Editor background, pure void |
| **Sidebar** | `#141414` | Sidebars, panels, widgets |
| **Selection** | `#2d2d2d` | Text selection, hover states, buttons |
| **Border** | `#636363` | Borders, subtle dividers |

### Phosphor
| Color | Hex | Role |
| :--- | :--- | :--- |
| **Text** | `#ffffff` | Standard text |
| **Variable** | `#e8e8e8` | Variables, identifiers |
| **Comment** | `#b3b3b3` | Comments, docstrings |
| **Ignored** | `#757575` | Ignored files, disabled elements |

### Glow
| Color | Hex | Role |
| :--- | :--- | :--- |
| **Wheat** | `#fae2c8` | Types, classes, bright glow |
| **Tan** | `#d9b98c` | Secondary glow |
| **Gold** | `#ffb86c` | Keywords, storage, headers |
| **Amber** | `#ff9e3b` | Functions, accents, active states |
| **Clay** | `#f08d49` | Operators, punctuation |

### Accents
| Color | Hex | Role |
| :--- | :--- | :--- |
| **Red** | `#ff6b6b` | Errors, deletions, dangerous actions |
| **Green** | `#b9d665` | Strings, insertions, success |
| **Cyan** | `#aee6d6` | Regex, escapes, information |
| **Blue** | `#9cd9e6` | Links, properties, secondary info |
| **Purple** | `#eba4be` | Constants, numbers, booleans |

## 📦 Installation

### Option 1: Load from file (Recommended)

1.  **Download** `catthode.json` to your home directory (e.g., `~/.gemini/themes/catthode.json`).

    ```bash
    mkdir -p ~/.gemini/themes
    curl -o ~/.gemini/themes/catthode.json https://raw.githubusercontent.com/catthode/gemini-cli/main/catthode.json
    ```

2.  **Update your `settings.json`** (usually located at `~/.gemini/settings.json`) to point to the theme file.

    ```json
    {
      "ui": {
        "theme": "/Users/YOUR_USERNAME/.gemini/themes/catthode.json"
      }
    }
    ```
    *Note: Replace `/Users/YOUR_USERNAME` with your actual home directory path. For security, Gemini CLI only loads themes from within your home directory.*

### Option 2: Add as a Custom Theme

1.  Open your `~/.gemini/settings.json`.
2.  Add Catthode to the `customThemes` block:

    ```json
    {
      "ui": {
        "customThemes": {
          "Catthode": {
            "name": "Catthode",
            "type": "custom",
            "Background": "#000000",
            "Foreground": "#FFFFFF",
            "LightBlue": "#9CD9E6",
            "AccentBlue": "#9CD9E6",
            "AccentPurple": "#EBA4BE",
            "AccentCyan": "#AEE6D6",
            "AccentGreen": "#B9D665",
            "AccentYellow": "#D9B98C",
            "AccentRed": "#FF6B6B",
            "Comment": "#757575",
            "Gray": "#636363",
            "DiffAdded": "#B9D665",
            "DiffRemoved": "#FF6B6B",
            "DiffModified": "#FFB86C",
            "GradientColors": ["#FFB86C", "#FF9E3B", "#F08D49"],
            "text": {
                "primary": "#FFFFFF",
                "secondary": "#E8E8E8",
                "link": "#9CD9E6",
                "accent": "#FF9E3B",
                "response": "#FFFFFF"
            }
          }
        },
        "theme": "Catthode"
      }
    }
    ```

3.  Select the theme using the `/theme` command in Gemini CLI.
