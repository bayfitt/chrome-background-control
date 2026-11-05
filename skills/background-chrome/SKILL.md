---
name: background-chrome
description: Use the connected Chrome browser for an explicitly requested task while the user continues working in another app. Use when the user asks for Chrome actions without taking over their screen; do not use for unrelated native desktop automation.
---

# Background Chrome

Use the available Chrome browser integration and its current documentation. Prefer the user's existing Chrome profile and tabs when requested; do not substitute a separate browser profile without explaining the difference.

1. Discover the available browser and tabs through the supported computer-use interface. Select the connected Chrome extension and the relevant tab, following any session-naming and tab-claiming instructions returned by that interface. Create a tab only if needed.
2. Read the current page state before each action and use the documented browser or page-level controls. Choose targets from the current page, not remembered element indices. Prefer operations directed at the tab over native desktop input, which can activate a window.
3. After every meaningful action, inspect the resulting page or site state. If a click times out or its result is unclear, inspect before retrying, especially when a second action could duplicate a purchase, cart item, message, or other change.
4. Report the actual outcome and any interruptions or limitations. Ask the user whether their work was interrupted if foreground focus cannot be measured. If the available method requires taking over the foreground, explain the limitation rather than silently doing so.

An inactive-tab read, an expandable page control, and an Amazon cart addition have worked in one observed Chrome extension session while the user reported no screen takeover. This is not a guarantee for every page, action, minimized window, native dialog, or future version. In that session, requesting `visible: false` when creating a Chrome tab was unsupported; use only visibility options the current interface advertises and do not infer background behavior from a successful call.

Follow the host's current browser safety and confirmation rules. A request to work in the background does not authorize unrelated account changes, purchases, or messages. Handle restricted sites, sign-ins, native dialogs, and site-specific failures using the current interface's documented guidance.
