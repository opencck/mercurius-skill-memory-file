**English** | [Русский](README.ru.md)

# mercurius-skill-memory-file

A built-in skill of [Mercurius](https://github.com/opencck/mercurius): how the agent keeps a participant's
`MEMORY.md` within its limit. The file goes whole into the prompt of the participant's private chat, up to
`MEMORY_FILE_LIMIT` characters (8000 by default); past it only its head goes in, with a note. The skill tells the agent
to read the whole file, take a snapshot, merge repeats, drop what is done or stale, move lasting knowledge into the fact
memory, rewrite the file in one call to 70–80% of the limit, check its length and say what it did — never dropping a
rule the participant stated, and stopping after two attempts instead of looping.

The text of the skill is in Russian, the agent's default language.

## Contents

| File | What it is |
|------|------------|
| `SKILL.md` | When to compress, the order of work, what not to do |
| `references/structure.md` | Sections of a compact `MEMORY.md`, how to shorten a line, how the length is counted |
| `BRIEF.md` | The specification of this repository (in Russian) |

## Use

The skill is a submodule `skills/memory-file` of Mercurius and is loaded at the start as a built-in skill; the agent
opens it with `skill_view` when the prompt says `MEMORY.md` is over its limit. Its format — a folder with `SKILL.md` —
is the common one of agent skills.

## License

[MIT](LICENSE)
