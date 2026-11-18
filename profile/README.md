<p align="center">
  <img src="https://raw.githubusercontent.com/scry-mcp/scry-core/main/docs/scry-logo.png" alt="SCRY" width="240">
</p>

<p align="center"><b>SCRY turns your AI client into a debugger for old machines: ask what a program in MAME or DOSBox-X is doing, and it finds out.</b></p>

<p align="center">
  <a href="https://github.com/scry-mcp/scry-dosbox-x"><picture><source media="(prefers-reduced-motion: reduce)" srcset="https://raw.githubusercontent.com/scry-mcp/scry-core/main/docs/scry-dosbox-x.png"><img src="https://raw.githubusercontent.com/scry-mcp/scry-core/main/docs/scry-dosbox-x.webp" alt="Monkey Island's lookout answering as written, then with a line written into memory" width="444"></picture></a>
  <a href="https://github.com/scry-mcp/scry-mame"><picture><source media="(prefers-reduced-motion: reduce)" srcset="https://raw.githubusercontent.com/scry-mcp/scry-core/main/docs/scry-mame.png"><img src="https://raw.githubusercontent.com/scry-mcp/scry-core/main/docs/scry-mame.webp" alt="LineUp played on the arcade board: three shots, each from another column or colour" width="320"></picture></a>
</p>
<p align="center"><em>scry-dosbox-x rewrites a line of Monkey Island while the game runs; scry-mame plays LineUp on its arcade board, one call a shot.</em></p>

SCRY is two [MCP](https://modelcontextprotocol.io) servers, one per emulator. Each keeps its
emulator open at the debugger, so your client can stop the program, read its memory by name
and press its inputs. Every reply carries its evidence.

- **[scry-mame](https://github.com/scry-mcp/scry-mame#install)**: an arcade board or a home
  computer running in MAME.
- **[scry-dosbox-x](https://github.com/scry-mcp/scry-dosbox-x#install)**: a DOS program running
  in DOSBox-X.
- **[scryai.net](https://scryai.net)**: both servers in one place, with a page for every tool
  and every demo.

Both run on macOS and Windows, and need git and [uv](https://docs.astral.sh/uv/). Each server's
README has the lines to paste into your MCP client, and a first question to ask.

## What you can ask

- **"Who writes this byte?"** A watch stops the program as soon as the byte changes.
- **"Where does the game keep its credits?"** A scan narrows memory to the bytes that changed
  with the value.
- **"What happens if I press this?"** Press a control or a key, then read the screen.

Both servers are built on [scry-core](https://github.com/scry-mcp/scry-core), the shared
package; [scry-site](https://github.com/scry-mcp/scry-site) builds scryai.net from their
documents.

Developed by Optimiza ([Marcos Hernández](https://www.linkedin.com/in/optimiza/)), in collaboration with [MS-DOS Club](https://msdos.club) and its [podcast](https://www.ivoox.com/podcast-ms-dos-club_sq_f11160693_1.html).
