# Contributing to Quarry

Thanks for helping. Quarry's tools are ports of libraries from the web (Quarry Query of
[TanStack Query](https://github.com/TanStack/query)), so the first question for any change is what
the original does: a fix that makes a tool behave as the original does is welcome; a change in
behaviour the original does not have needs a reason a game has and a web app does not.

## Before you start

- **Bugs**: open an issue with the smallest code that shows it, what you expected, and what
  happened. If the library it ports behaves differently, say how.
- **Features**: open an issue first, so we can agree on the shape before you write it.
- **Security problems**: never in a public issue; see [SECURITY.md](SECURITY.md).

## Working on the code

You need [Rokit](https://github.com/rojo-rbx/rokit).

```sh
rokit install
lune run install   # React for type checking the bindings, sourcemap, package types
lune run check     # what CI runs: license, format, style, lint, types, tests, builds
```

- Each repository's README says where its packages live (in Quarry Query, `lib/quarry-query`
  and `lib/quarry-react-query`).
- Every file is `--!strict`. Values of unknown type are `unknown`, read through `Unknown.luau`;
  an `any` needs a comment directly above it starting `-- Invariant:` that says why it is safe.
- Port from the original's source where there is one, and name the file you ported from in
  the module's header comment.
- Every change in behaviour comes with a test, run in Lune with no waiting on real time (in
  Quarry Query, `lib/quarry-query/test`, on the fake scheduler). Check that the test fails
  without your change.
- The code follows the Linux kernel coding style, read for Luau: see
  [STYLE.md](https://github.com/quarry-luau/quarry-query/blob/main/STYLE.md). StyLua lays it out
  (`stylua lib .lune`) and `lune run style` checks the rest.

## Pull requests

- Branch from `main` and open the pull request against it. `main` is protected: CI must pass and a
  maintainer must approve before it merges.
- One change per pull request, described as what changed and why.
- Commit messages follow [Conventional Commits](https://www.conventionalcommits.org): `fix: ...`,
  `feat: ...`, `docs: ...`, with a body that says why.
- Add a line to `CHANGELOG.md` under "Unreleased" for anything a user would notice.

By contributing you agree your work is released under the MIT License, as the repository's
`LICENSE` says, and that you follow the [Code of Conduct](CODE_OF_CONDUCT.md).
