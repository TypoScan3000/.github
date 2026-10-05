<p align="center"><img src="https://raw.githubusercontent.com/TypoScan3000/.github/main/profile/mascot.png" width="240" alt="TypoScan3000 mascot: a robot with a magnifying-glass eye, holding a red fountain pen"></p>
<h1 align="center">TypoScan3000</h1>
<p align="center"><em>Fixing teh world's open source, one typo at a time.</em></p>

---

### What is this?

Every week our AI subscription comes with a pile of tokens, and most weeks some are
left over when the meter resets. TypoScan3000 donates them to open source: it reads
public repositories, finds the small things that are objectively wrong (`recieve`,
`teh`, `if (count = 0)`, a `__len` that should be `__len__`) and sends a tiny pull
request to fix them.

This org just holds the forks those PRs come from. Every repo here is temporary and
gets deleted once its PR is merged or closed.

### How a fix gets made

1. **Scan.** An LLM reads up to a dozen source files per repo and lists suspected typos.
2. **Does it exist?** A script confirms each quoted string is really in the file, and that the file isn't generated.
3. **Second opinion.** A model running on our own hardware judges each finding and proposes the exact edit.
4. **Safety gate.** A script simulates every edit against the real file. Anything that touches more than intended is dropped.
5. **A human reads every change** before a PR is filed.

### House rules

- **Objectively wrong only.** Spelling, grammar, and tiny obvious bugs a maintainer would agree with on sight. No style changes, no refactors.
- **Your rules win.** We read `CONTRIBUTING.md` first and follow your title format, branch rules, DCO and CLA. If you don't take typo PRs, we don't file one.
- **Low noise.** At most 3 open PRs per organization, spaced hours apart.
- **Want a tweak?** Comment on the PR and we'll push it. GitHub doesn't let maintainers push to forks owned by an organization, so ask and we'll do it.
- **No arguing.** Don't want it? Close it. We won't reopen it.
- **We clean up.** Forks are deleted after the PR closes.

### Don't want these?

Totally fine. [Open an opt-out request](https://github.com/TypoScan3000/.github/issues/new?template=opt-out.yml)
and your org goes on the do-not-scan list for good.

### Found a bad fix?

Say so on the PR or [open an issue](https://github.com/TypoScan3000/.github/issues/new?template=bad-fix.yml).
Every wrong fix makes the checks better.

### By the numbers

<!-- stats:start -->
| PRs filed | Merged | Orgs reached | Orgs scanned |
|---:|---:|---:|---:|
| 928 | 134 | 387 | 5,593 |
<!-- stats:end -->

<sub>Updated daily. A hobby project run by <a href="https://github.com/Avicennasis">@Avicennasis</a>.
Now with 3000% fewer typos.</sub>
