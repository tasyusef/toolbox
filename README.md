# Toolbox

Four design tools in one app: logo packages, colour systems, type specimens
and image conversion. macOS, Windows and Linux. Every tool also runs from a
terminal and over MCP.

This repository holds the release builds. The app, its tools and the
command-line and MCP reference live at
**[timothyali.com/toolbox](https://www.timothyali.com/toolbox/)**.

## Download

Grab the latest build from the [Releases](../../releases/latest) page.

| Platform | File |
| --- | --- |
| macOS, Apple silicon | `Toolbox-<version>-arm64.dmg` |
| macOS, Intel | `Toolbox-<version>.dmg` |
| Windows, x64 and arm64 | `Toolbox-Setup-<version>.exe` |
| Linux, x86_64 | `toolbox-<version>-x86_64.AppImage` |
| Linux, arm64 | `toolbox-<version>-arm64.AppImage` |

Every release ships a `SHA256SUMS` file. Check a download with
`shasum -a 256 -c SHA256SUMS --ignore-missing` on macOS or Linux, or
`certutil -hashfile <file> SHA256` on Windows.

### macOS

Builds are signed with a Developer ID and notarized by Apple. Open the dmg
and drag Toolbox to Applications.

### Windows

The installer is **not code-signed**, so SmartScreen shows "Windows protected
your PC" the first time. Click **More info**, then **Run anyway**. Check the
SHA-256 against `SHA256SUMS` first if you want to be sure of what you have.

### Linux

The AppImage needs to be executable once: `chmod +x toolbox-*.AppImage`.
A `.deb` will join the AppImage once releases are built on Linux.

## From a terminal

The installed app is also the `toolbox` command and an MCP server:

```
toolbox                      # what tools exist
toolbox convert --help       # the options for one tool
toolbox --mcp                # serve the tools to an agent
```

The full reference is at
[timothyali.com/toolbox/agents](https://www.timothyali.com/toolbox/agents/).
