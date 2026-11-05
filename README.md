# Background Chrome skill

A Codex skill for using the connected Chrome extension to work in tabs while the user continues using their computer. It documents a tested workflow and its limits; it does not install a browser extension or guarantee that every Chrome action stays in the background.

The skill is in [`skills/background-chrome`](skills/background-chrome/SKILL.md). To install it, give Codex the repository URL and ask it to install the skill at `skills/background-chrome` using its skill installer. Access to this repository is required if it is private. The existing Chrome integration must also be available and connected separately.

Once installed, ask Codex to use `$background-chrome` for a task, or ask it to work in Chrome without taking over your screen. Availability and supported browser features depend on the Codex environment and Chrome integration.
