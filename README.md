# Occam

<p align="center">
  <img src="assets/occam.png" width="220" alt="Occam">
</p>

<p align="center">
  <em>Entia non sunt multiplicanda praeter necessitatem.</em><br>
  <sub>Do not multiply entities beyond necessity.</sub>
</p>

Occam is a minimal agent skill/plugin. It makes coding agents classify the
current context as engineering, research, or mixed work, then choose the
smallest implementation path that remains correct, inspectable, and
maintainable.

For research work, Occam keeps reproducibility small and mechanical: emitted
run artifacts should carry one adjacent `metadata.json` with input lineage,
command lineage, parameters, outputs, seeds, and metric definitions when
applicable.

This repository does only three things:

- Provides the `occam` skill.
- Supports Claude Code marketplace/plugin installation.
- Supports Codex marketplace/plugin installation.

It intentionally does not include hooks, benchmarks, review/audit commands, or
large multi-agent compatibility layers.

## Claude Code

Add the marketplace and install the plugin in Claude Code:

```text
/plugin marketplace add https://github.com/chenghuzi/Occam
/plugin install occam@occam
```

After installation, use:

```text
/occam
/occam lite
/occam full
/occam ultra
```

## Codex

Add the marketplace in Codex:

```bash
codex plugin marketplace add chenghuzi/Occam
codex
```

Then open `/plugins`, select the Occam marketplace, and install Occam.

## Structure

```text
.
|-- .agents/plugins/marketplace.json
|-- .claude-plugin/marketplace.json
|-- .claude-plugin/plugin.json
|-- .codex-plugin/plugin.json
|-- LICENSE
`-- skills/occam/SKILL.md
```

## Attribution

Occam is inspired by [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail).

Thanks to Dietrich Gebert and the Ponytail project. Occam keeps Ponytail's core
idea: YAGNI, stdlib/native first, no unnecessary abstractions, and the smallest
correct implementation that completes the task.

Occam is not officially affiliated with Ponytail. It is a smaller adaptation
focused on engineering/research profile selection, correctness,
inspectability, and reproducibility.

Ponytail is licensed under the MIT License. Because Occam's rule text and
structure are inspired by Ponytail and include derivative content, this
repository preserves Ponytail's copyright and license notice.
