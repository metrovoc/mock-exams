# mock-exams

An agent skill that builds mock exams replicating a course's upcoming exam in its own medium (paper, browser, media, hands-on or oral), with answer keys, from all of the course's materials.

## Install

The skill lives in `skills/mock-exams`. Copy that directory into your agent's skills directory:

```sh
git clone https://github.com/metrovoc/mock-exams
cp -r mock-exams/skills/mock-exams ~/.claude/skills/   # Claude Code
cp -r mock-exams/skills/mock-exams ~/.codex/skills/    # Codex
```

## Use

```
/mock-exams [course] [exam] [number of mocks]
```

In Codex, write `$mock-exams` instead. The skill runs only when invoked by name. Mocks go to the folder you name or your workspace's agent instructions designate, otherwise to `mocks/` beside the course's folder.
