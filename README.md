# Toolbox

Four design tools in one app: logo packages, colour systems, type specimens
and image conversion. macOS and Linux. Every tool also runs from a
terminal and over MCP.

This repository holds the release builds. The app, its tools and the
command-line and MCP reference live at
**[timothyali.com/toolbox](https://www.timothyali.com/toolbox/)**.

## Download

Starting with 1.1.0, releases support macOS and Linux. Windows builds are discontinued.

Grab the latest build from the [Releases](../../releases/latest) page.

| Platform | File |
| --- | --- |
| macOS, Apple silicon | `Toolbox-<version>-arm64.dmg` |
| macOS, Intel | `Toolbox-<version>.dmg` |
| Linux, x86_64 | `toolbox-<version>-x86_64.AppImage` or `toolbox_<version>_amd64.deb` |
| Linux, arm64 | `toolbox-<version>-arm64.AppImage` or `toolbox_<version>_arm64.deb` |

Every release ships a `SHA256SUMS` file. Run `shasum -a 256 <file>` and compare
the result with that file’s entry in `SHA256SUMS`.

### macOS

Builds are signed with a Developer ID and notarized by Apple. Open the dmg
and drag Toolbox to Applications.

### Linux

The AppImage needs to be executable once: `chmod +x toolbox-*.AppImage`.
The deb installs with `sudo dpkg -i toolbox_*.deb`.

## From a terminal

The installed app is also the `toolbox` command and an MCP server:

```
toolbox                      # open the desktop app
toolbox --help               # what tools exist
toolbox convert --help       # the options for one tool
toolbox --mcp                # serve the tools to an agent
```

The full reference is at
[timothyali.com/toolbox/agents](https://www.timothyali.com/toolbox/agents/).
