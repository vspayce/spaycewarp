# spaycewarp

Jason Taylor's fork of [warpdotdev/warp](https://github.com/warpdotdev/warp).

## Goals

1. **Windows builds from GitHub**: no local toolchain needed.
2. **Local-first**: works without a Warp account, cloud sync or cloud agents; telemetry off by default.
3. **Bring your own AI**: point the AI at your own provider (OpenAI-compatible, Anthropic, local models).

## Getting a build

- Download the latest installer from this repo's **Releases** page, or
- run **Actions -> Spayce Windows build -> Run workflow** to build the current code (takes 1-3 hours).

The installer is unsigned: when Windows SmartScreen warns, click **More info -> Run anyway**.

The build is upstream's open-source app (`warp-oss`), so it installs as **WarpOss** and sits alongside an official Warp install without conflict.

## Keeping up with upstream

On GitHub, use **Sync fork** on the repo page, or:

```bash
git remote add upstream https://github.com/warpdotdev/warp.git
git fetch upstream
git merge upstream/master
```

Fork-specific files: `SPAYCE.md` and `.github/workflows/spayce_windows.yml`. Upstream's own workflows are disabled in this fork's Actions settings (they need Warp's private infrastructure), so they don't run here.
