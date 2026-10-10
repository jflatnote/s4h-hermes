# s4h-hermes

Structured reasoning toolkits for [Hermes Agent](https://hermes-agent.nousresearch.com). Describe a situation in plain English and the `s4h` skill picks a workflow from 34 toolkits (decision, logic, systems, ethics, strategy, and more) and loads only the methods it needs.

An unofficial Hermes adaptation of [skills-for-humanity](https://github.com/human-avatar/skills-for-humanity). See NOTICE.md.

## What is inside

- 35 skill folders: `s4h` (orchestrator) and `s4h-<domain>` (34 toolkits).
- 177 methods stored in each toolkit's `references/` folder; `s4h/references/catalog.md` lists them all.

## Install

Copy the skill folders into your Hermes skills folder, then start a NEW Hermes session. Running sessions keep the skill list they started with.

    git clone https://github.com/jflatnote/s4h-hermes.git
    cp -R s4h-hermes/skills/. ~/.hermes/skills/

Status: draft. This install command has not yet been tested from a clean Hermes setup.

## Use

In a new session, ask Hermes to use the `s4h` skill for your situation, or name a toolkit directly, such as `s4h-decision`.

## License

MIT. See LICENSE and NOTICE.md.
