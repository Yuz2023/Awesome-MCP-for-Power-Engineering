# Contribution Guidelines

Thanks for helping keep this list useful and evidence-based. Please read these guidelines before
opening a pull request.

## What belongs here

The main [README](README.md) lists publicly accessible MCP integrations relevant to power
engineering. Entries may be:

- **Operational integrations:** MCP tools that act on an engineering application, solver, device,
  industrial endpoint, or engineering workflow.
- **Engineering-data services:** narrowly scoped engineering-data MCP services, clearly described
  as data access rather than simulator or device control.

A library or API without an MCP transport and tool/resource surface does not qualify.
Documentation-search or RAG-only servers are not treated as operational integrations; they may
appear in the [extended catalog](awesome-mcp-power-engineering-full-catalog.md) only when clearly
labeled.

Inclusion is evidence-limited. Source inspection does not imply successful installation,
licensed-software execution, simulator runtime, HIL, instrument, target, or hardware validation.

## Adding an entry

Open a pull request that:

1. Adds the entry to the correct domain section.
2. Provides a working, publicly accessible repository or first-party documentation link.
3. Records the publisher as `First-party`, `Project steward`, `Institutional`, or `Community`.
4. Records availability as `Available`, `Unassessed`, `Alpha`, `Early Access`, `Experimental`, or
   `Reference`.
5. Describes access accurately: source available, bundled, hosted, commercial, and any required
   product. Do not describe source as open source unless its license has been checked.
6. States only the validation obtained: `Repository-checked`, `Vendor-documented`,
   `Source-inspected`, `Mock-tested`, `Install-checked`, `Runtime-tested`, or
   `Hardware/HIL-tested`.
7. Summarizes the supporting evidence in the pull-request description. Mocked or unit tests must not
   be presented as simulator, HIL, instrument, target, or hardware validation.

If a tool already has representative implementations in the main list, add further alternatives to
the [extended catalog](awesome-mcp-power-engineering-full-catalog.md).

## Proposing a gap

The [public implementation gaps](README.md#public-implementation-gaps) section records a dated
search for publicly accessible implementations. Search the existing issues first, then
[open an issue in this repository](https://github.com/Yuz2023/Awesome-MCP-for-Power-Engineering/issues)
with the tool name, its public automation documentation, and the date checked.

## Quality bar

- Links must resolve; moved links should use the canonical destination, and dead links should be
  removed or explicitly marked archived.
- All submitted evidence must be publicly accessible. Do not include private URLs, local filesystem
  paths, confidential projects, customer data, credentials, or unpublished validation artifacts.
- Validation labels must not exceed the evidence supplied.
- Do not infer maturity from stars, tool counts, or mocked test counts.
- No self-promotion of empty or non-functional repositories.
- Keep tables and terminology consistent with the main list.

By contributing, you agree to license your contributions under
[CC BY 4.0](LICENSE), the same license as this list.
