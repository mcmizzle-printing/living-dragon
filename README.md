# Living Dragon

Project scaffold for a dragon-shaped planter with modular scale sockets and experimental inserts.

**Status:** Concept and planning. No validated CAD, printable parts, printer profiles, material specifications, or experimental results are included yet.

## Project layout

- `docs/`: concept, architecture, materials, safety, and concept imagery.
- `cad/`: editable dragon, scale socket, insert, and planter designs.
- `stl/`: prototype and production mesh exports.
- `3mf/`: printer-specific project files for the requested Bambu P2S and H2C folders; compatibility remains unverified.
- `experiments/`: seed retention, water exposure, insert geometry, and glow-versus-growth trials.
- `profiles/`: working material notes.
- `build-log/`: dated decisions, builds, and results.

## Working with Claude and Codex

The local checkout lives at `~/Printing/living-dragon`.

- [AGENTS.md](AGENTS.md): shared project context and working rules.
- [CLAUDE.md](CLAUDE.md): Claude Code entry point importing the shared rules.
- [Project status](docs/status.md): current state, open decisions, and the next proposed step.

Start either tool in this repository. Keep durable decisions and handoff context in the tracked documents so work can continue across tools and sessions.

The entry points follow the official [Codex AGENTS.md guidance](https://developers.openai.com/codex/guides/agents-md/) and [Claude Code shared-instruction guidance](https://code.claude.com/docs/en/memory#agentsmd).

## Getting started

1. Define the concept, dimensions, plant species, and operating conditions in `docs/concept.md`.
2. Identify the exact materials and review supplier documentation.
3. Design and test individual sockets and inserts before assembling a complete planter.
4. Record prototype revisions and results in the build log.

`docs/images/living-dragon-concept.png` is a transparent placeholder, not a concept rendering. Empty design and experiment directories contain `.gitkeep` files so Git can preserve them.

## License

A license has not been selected. See `LICENSE` before reuse or distribution.
