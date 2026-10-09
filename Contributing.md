# Contributing to BootForge

First off — thank you. BootForge is better because people like you take the
time to open an issue, fix a typo, or send a pull request. This document
describes the small set of rules we ask contributors to follow so that your
work can be reviewed and merged quickly.

## Ways to contribute

- **Report a bug.** If something crashes, hangs, writes the wrong bytes, or
  behaves differently than the documentation says, open an issue. Include
  the exact version, the OS build, and the steps to reproduce.
- **Request a feature.** New format support, additional verification modes,
  UI improvements — all welcome. Keep requests scoped and explain the use
  case.
- **Improve the documentation.** README fixes, clearer error messages,
  translated glossaries — documentation PRs are reviewed as seriously as
  code.
- **Write code.** Fix a bug, implement a feature from the roadmap, improve
  performance, or add tests.

## Reporting bugs

Before filing a new issue, please search existing issues to avoid duplicates.
A good bug report contains:

1. BootForge version (shown in the About dialog).
2. Windows build number (`winver`).
3. Target device (vendor, model, capacity, interface — USB 2.0 / 3.x / UASP).
4. The source image, if public (name, SHA-256, size).
5. Exact steps to reproduce.
6. Observed behaviour vs. expected behaviour.
7. The relevant portion of the log file (BootForge → Help → Open log folder).

Please redact serial numbers, machine identifiers, and anything you consider
private before uploading logs.

## Suggesting enhancements

Open a new issue with the `enhancement` label. Explain:

- What problem the change solves.
- Who benefits from it.
- Alternatives you considered.
- Whether you are willing to work on it.

We prefer small, incremental proposals over large architectural rewrites.

## Pull requests

1. Fork the repository and create a feature branch from `main`.
2. Keep the pull request focused — one logical change per PR.
3. Match the existing coding style. No reformatting unrelated files.
4. Add or update tests for behavioural changes.
5. Update the `CHANGELOG.md` under the "Unreleased" section.
6. Confirm that the full test suite passes locally before pushing.
7. Describe *why* the change is needed, not just *what* it does.

### Commit messages

Use the imperative mood in the subject line (`Fix stall when flashing a
dirty UDF image`, not `Fixed stalls`). Keep the subject under 72 characters.
Add a body if the change is non-trivial.

### Review

A maintainer will review your PR within a few business days. Expect
questions and change requests — they are a sign the review is thorough,
not that the work is bad.

## Code style

- Four-space indentation, no tabs.
- One statement per line.
- Prefer explicit names over abbreviations.
- Public APIs are documented with a short paragraph and an example.
- Error messages are complete sentences and name what the user can do next.

## Testing

- Unit tests cover individual modules and must not touch disks.
- Integration tests write to virtual devices only. Never target real hardware
  in CI.
- Manual test plans for release candidates live under `docs/testing/`.

## Security

If you discover a vulnerability, please do **not** open a public issue.
See the Security section of the README for the private disclosure channel.

## Code of conduct

This project follows the [Code of Conduct](code_of_conduct.md). By
participating, you agree to abide by its terms. Report incidents through the
same channels you would use for a security report.

## License

By contributing you agree that your work is released under the project's
[MIT License](LICENSE.md).
