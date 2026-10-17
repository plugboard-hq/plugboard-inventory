# plugboard-inventory

A skill agent for [Plugboard](https://github.com/wrabit/plugboard): stock questions over
the sales warehouse. No code. `SKILL.md` is the whole agent: frontmatter for the manifest
(name, routing description, the capabilities it takes and their settings, example prompts)
and the persona as the body. It takes `database_tools` and `ask_user` from the host.

## Install into a host

```
cd plugboard
echo 'PLUGBOARD_EXTRA_SKILLS=../plugboard-inventory' >> .env   # comma-separated paths to skill directories
uv run uvicorn project.asgi:application --port 8010
```

A path may point at one skill directory (holding `SKILL.md`) or at a directory of them.
