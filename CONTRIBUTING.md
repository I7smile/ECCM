# Contributing to ECCM

Thanks for taking the time to contribute. ECCM is intentionally a single-file tool — all HTML, CSS, and JavaScript lives in `eccm.html`. Keeping it that way is a core design goal, so contributions should work within that constraint.

## Before you start

- Check [open issues](https://github.com/I7smile/ECCM/issues) to see if your idea or bug is already being tracked.
- For anything beyond a small fix, open an issue first to discuss. This avoids wasted effort if the change isn't a good fit.

## Setting up

No build tools required. Clone the repo and open `eccm.html` in a browser:

```bash
git clone https://github.com/I7smile/ECCM.git
cd ECCM
open eccm.html   # macOS
# or just drag the file into your browser
```

## Making changes

- All code is in `eccm.html`. The structure is: CSS → HTML → JavaScript (in `<script>` blocks).
- The JavaScript section is organised into clearly labelled `/* === SECTION === */` blocks.
- Keep new code in the appropriate section. If there isn't one, add a labelled block.
- Don't add external dependencies, build steps, or separate files — the single-file constraint is intentional.

## Code style

- Match the existing style: `var` declarations, `function` statements, no classes or modules.
- Keep comments minimal — only when the *why* is non-obvious.
- Functions that mutate `state` should call `saveStore()` and `render()` at the end.

## Testing

There is no automated test suite. Before submitting:

1. Open `eccm.html` in Chrome, Firefox, and Safari.
2. Test the golden path: add device → connect ports → view connections table → print.
3. Test the specific area you changed with representative edge cases.
4. Verify dark and light themes both look correct.

## Submitting a pull request

1. Fork the repo and create a branch with a descriptive name (`fix-vlan-parsing`, `add-csv-export`, etc.).
2. Make your changes in `eccm.html`.
3. Update [CHANGELOG.md](CHANGELOG.md) under a new `[Unreleased]` heading.
4. Open a pull request with:
   - A clear title
   - A description of *what* changed and *why*
   - How to test the change manually

## Reporting bugs

Use the [bug report template](.github/ISSUE_TEMPLATE/bug_report.md). Include:
- Browser and OS
- Steps to reproduce
- What you expected vs. what happened
- Whether the issue survives a page reload

## Requesting features

Use the [feature request template](.github/ISSUE_TEMPLATE/feature_request.md). Be specific about the use case — "I need X because Y" is much more useful than "add X".

---

By contributing, you agree that your changes will be licensed under the [MIT License](LICENSE).
