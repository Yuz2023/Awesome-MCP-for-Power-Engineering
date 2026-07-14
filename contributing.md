# Contribution Guidelines

Thanks for helping keep this list accurate and complete! Please read these guidelines before opening
a pull request.

## What belongs here

The main [README](README.md) lists **MCP servers that genuinely drive a power-engineering tool** —
open a project, set parameters, run a simulation/build, read results — over the Model Context
Protocol. For each tool we feature the **most mature one or two** servers plus any **vendor-official**
one. Everything else verified goes in the
[full catalog](awesome-mcp-power-engineering-full-catalog.md).

**Does qualify:** a server exposing MCP tools that control the actual tool (simulator, solver, EDA
suite, HIL rig, instrument, PLC).

**Does not qualify for the main list:** plain API/SDK wrappers, generic chatbots, or docs-only / RAG
servers that only search documentation. If it's real but doc-only, add it to the full catalog with a
note.

## Adding an entry

Open a pull request that:

1. Adds the entry to the correct section, keeping the tables tidy and alphabetical where reasonable.
2. Includes a **working link** to the MCP server (GitHub repo or vendor page).
3. Marks it **official** (published by the software vendor) or **community** (third party).
4. Confirms — ideally in the PR description — how you verified it drives the tool over MCP (tried it,
   read the source, saw the `@mcp.tool` surface, etc.).
5. Keeps the description short: the tool, and one phrase on maturity or what's distinctive.

If a tool already has one or two mature servers listed, add further alternatives to the
[full catalog](awesome-mcp-power-engineering-full-catalog.md) rather than the main list.

## Claiming a gap

The [*APIs available, no MCP yet*](README.md#apis-available-no-mcp-yet) section tracks tools with an
automation API but no MCP server. Want to build one? Open an issue at
[Yuz2023/PE-MCP](https://github.com/Yuz2023/PE-MCP/issues) to claim it first, so two people don't
build the same server twice.

## Quality bar

- Links must resolve; dead links get removed.
- No self-promotion of empty or non-functional repos.
- One entry per line; keep formatting consistent with existing rows.

By contributing, you agree to license your contributions under
[CC BY 4.0](LICENSE), the same license as this list.
