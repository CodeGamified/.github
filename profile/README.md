# CodeGamified

**Ship a game where players write real code. We handle the boring parts.**

Compiler. VM. Terminal UI. Simulation clock. You bring the game.

## The Stack

```
Your Game
  ↓ implements 3 interfaces
.engine/CodeGamified.Engine    Python subset → bytecode → sandboxed executor
.engine/CodeGamified.TUI       Monospace terminal UI → TextMeshPro
.engine/CodeGamified.Time      Simulation clock + time warp state machine
```

## Why Clone This

- **You want to build a "learn to code" game** that isn't a disguised tutorial.
- **You need a sandboxed scripting VM** that compiles a Python subset to bytecode and runs it tick-by-tick inside Unity.
- **You want retro terminal UIs** with scramble animations, progress bars, gradient text, resizable panels — out of the box.
- **You need simulation time** with pause, presets, and smooth time warp.

## What You Implement

| Interface | You Define |
|---|---|
| `ICompilerExtension` | Your game's builtins: `radio.send()`, `helm.steer()`, whatever |
| `IGameIOHandler` | What your custom opcodes do at runtime |
| `TerminalWindow` | Your terminal panels — override `Render()` |

That's it. Three interfaces. The rest is wired.

## Repos

| Repo | What |
|---|---|
| [**.engine**](https://github.com/CodeGamified/.engine) | Shared engine submodules (Engine + TUI + Time) |
| [**pong**](https://github.com/CodeGamified/pong) | Minimal example — code-controlled Pong |
| **codegamified.github.io** | This org page |

## Games Built On This

**BitNaughts** — GPU satellite tycoon. Program orbital sensors and transmissions.  
**SeaRauber** — Pirate sandbox. Automate crew, navigation, ship systems.  
**Pong** — Classic arcade. Paddles controlled by player-written code.

---

*Players don't need tutorials. They need a terminal and a reason to type.*