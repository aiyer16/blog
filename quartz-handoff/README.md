# field notes — Quartz theme handoff

Two files translate the mockup into your Quartz site:

1. **`quartz.config.ts` colors** — paste the `colors` block into your existing config.
2. **`custom.scss`** — replace `quartz/styles/custom.scss` (typography, spacing, accents).

---

## 1. Colors → `quartz.config.ts`

Find the `theme: { ... colors: { ... } }` block in `quartz.config.ts` and replace
the `colors` object with this. Quartz keys mean:

- `light` — page background
- `lightgray` — borders / hr / subtle lines
- `gray` — graph links, secondary borders, muted icons
- `darkgray` — body text
- `dark` — headings / strong text
- `secondary` — links + active states (the sage accent)
- `tertiary` — hover / visited
- `highlight` — internal-link background, search highlight (soft accent)
- `textHighlight` — `==marker==` background

```ts
colors: {
  lightMode: {
    light: "#f7f6f2",
    lightgray: "#e6e4db",
    gray: "#a3a299",
    darkgray: "#34332e",
    dark: "#2a2a26",
    secondary: "#5f8f6a",
    tertiary: "#7aa882",
    highlight: "rgba(95, 143, 106, 0.10)",
    textHighlight: "#cfe3c788",
  },
  darkMode: {
    light: "#181a17",
    lightgray: "#2b2d28",
    gray: "#66655d",
    darkgray: "#d9d8d0",
    dark: "#eceae2",
    secondary: "#93b88c",
    tertiary: "#a8cda1",
    highlight: "rgba(147, 184, 140, 0.14)",
    textHighlight: "#93b88c44",
  },
},
```

> Want a different accent? Change `secondary` (and a slightly lighter `tertiary`)
> in both modes. Mockup alternates: blue `#6f8fae`, terracotta `#b07a5f`,
> violet `#8a6fae` — lighten ~30% toward white for dark mode.

---

## 2. Typography & polish → `custom.scss`

Fonts are set in `quartz.config.ts` under `theme.typography`:

```ts
typography: {
  header: "Hanken Grotesk",
  body: "Hanken Grotesk",
  code: "JetBrains Mono",
},
```

Then use the accompanying `custom.scss` for the spacing, mono labels, soft cards,
and link styling that give the mockup its feel.
