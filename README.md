# Game of Life Studio

A modern, interactive implementation of Conway's Game of Life built with TypeScript and Vite.

## Features

- **Drawing tools** - Cell, line, rectangle, circle, eraser, selection, and pattern stamps
- **Pattern library** - Built-in patterns (gliders, spaceships, oscillators, etc.) with rotation support
- **Recording & timeline** - Record simulations, scrub through generations, adjust playback speed
- **Custom rules** - Define custom birth/survival rules beyond classic B3/S23
- **Visual settings** - Grid overlay, cell fade trails, maturity coloring, cell shapes
- **Auto-stop** - Automatically pause when simulation reaches a stable state
- **Session history** - Undo/redo for grid states
- **Dark/light theme** - System-aware with manual toggle
- **Full state persistence** - Settings and grid state saved to localStorage
- **Fullscreen mode** - Distraction-free simulation viewing
- **Inspector** - Click cells to view their state and neighborhood

## Getting Started

### Install dependencies
```bash
npm install
```

### Development (client + server with HMR)
```bash
npm run dev
```

### Static release build
```bash
npm run build:release
```

Output goes to `dist-client/`.

### Preview release build
```bash
npm run preview:release
```

### Run tests
```bash
npm test
```

## Project Structure

```
├── src/
│   ├── app.ts                  # Main app entry, DI wiring
│   ├── core/                   # Event bus, storage, DOM registry, defaults
│   ├── js/                     # Game engine, patterns, recording manager
│   ├── modules/                # Feature modules (sidebar, tools, renderer, etc.)
│   ├── css/style.css           # All styles
│   └── __tests__/              # Unit tests
├── server/                     # Express backend for recording storage
├── e2e/                        # Playwright end-to-end tests
├── index.html                  # Main app page
├── explanation.html            # Guide to cellular automata
├── vite.config.ts              # Dev config (with server proxy)
└── vite.config.client.ts       # Release build config (static output)
```

## License

MIT
