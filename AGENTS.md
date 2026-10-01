# Windows Package Manager manifests

This fork contains community package manifests. Read [CONTRIBUTING.md](CONTRIBUTING.md), [manifest authoring](doc/Authoring.md), and [the first-contribution checklist](doc/FirstContribution.md) before editing a package. Keep changes compatible with upstream microsoft/winget-pkgs conventions and the affected package's existing layout.

Routine manifest PRs are limited to one package version and must not include non-manifest changes. They do not require a separate issue. Feature work, repository tooling, and broader fixes follow the contributing guide's issue/design discussion process. Preserve installer identities, architecture, locale, scope, switches, dependencies, URLs, and hashes; investigate changed vendor artifacts rather than copying unverified metadata.

The manifest corpus is large. Inspect the affected package subtree and nearby versions instead of recursively loading every manifest. Check for nested agent guidance in the selected subtree before editing. Use the validation and installer-testing steps documented by the authoring/checklist pages for the installed Windows Package Manager version; report tool versions and exact results. Do not claim a repository-wide test suite exists merely because a manifest parses.

Downloaded installers are executable software. Hash verification and schema validation do not establish safe execution. Any install, uninstall, upgrade, or registry/filesystem verification must use an approved disposable environment, with the intended installer and package identity confirmed first. Preserve an operator's installed applications and user data.

Follow upstream PR templates and bot review requirements. Security vulnerabilities go to the Microsoft Security Response Center through [SECURITY.md](SECURITY.md), not public issue contents. Keep upstream contributions and fork-only maintenance distinct in the handoff.
