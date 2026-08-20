# Technical Writing output style

A Claude Code output style that makes Claude's prose shorter, more direct, and
easier to scan, aimed at making Claude Opus 5 outpus easier to parse. It's inspired 
by various technical writing style guides, turned into rules Claude applies to 
every reply.

The style covers chat replies, documentation, commit messages, PR text, and
code comments. It does not cover code, identifiers, command syntax, or quoted
material.

An output style occupies one slot in the Claude Code system prompt. The
environment blocks around it (tool schemas, working directory, model data,
memory rules) stay in place whatever style is active. This style sets
`keep-coding-instructions: true`, so Claude Code keeps its coding behavior and
applies the writing standard on top.

## Files

| File | Contents |
|---|---|
| `output-styles/technical-writing.md` | The Technical Writing style. |

## Install the style

1. Copy the style into your Claude Code styles directory:

   ```bash
   cp output-styles/technical-writing.md ~/.claude/output-styles/
   ```

2. In Claude Code, run `/output-style` and select **Technical Writing**.

To scope the style to one project, copy the file to `.claude/output-styles/`
inside that project instead.

## What the style covers

- **Succinctness** — answer first, say each thing once.
- **Sentences** — one idea per sentence, named actors, active voice, condition
  before action.
- **Words and terminology** — the plainest precise word, one name per concept,
  vocabulary taken from the layer being described.
- **Claims and numbers** — no unsupported certainty, no time anchors,
  defensible precision.
- **Structure** — headings, lists, tables, warnings, and numbered procedures.
- **Code comments** — no comment by default; a comment must carry what the code
  cannot.

## Sources

- [Google developer documentation style guide](https://developers.google.com/style)
- [Google technical writing courses](https://developers.google.com/tech-writing/resources)
- [Gernot Heiser's style guide](https://gernot-heiser.org/style-guide.html)
- [nbj-write-clearly](https://github.com/daniel-p-green/nbj-write-clearly)
- [developer-documentation-skill](https://github.com/NateBJones-Projects/developer-documentation-skill)

## License

[MIT](LICENSE). The rules are inspired by the sources above, not copied from
them.
