# Contributing to Quarry

Thanks for helping. Quarry is a port of [TanStack Query](https://github.com/TanStack/query), so the
first question for any change is what TanStack does: a fix that makes Quarry behave as TanStack
does is welcome; a change in behaviour that TanStack does not have needs a reason a game has and a
web app does not.

## Before you start

- **Bugs**: open an issue with the smallest code that shows it, what you expected, and what
  happened. If TanStack Query behaves differently, say how.
- **Features**: open an issue first, so we can agree on the shape before you write it.
- **Security problems**: never in a public issue; see [SECURITY.md](SECURITY.md).

## Working on the code

You need [Rokit](https://github.com/rojo-rbx/rokit).

```sh
rokit install
lune run install   # React for type checking the bindings, sourcemap, package types
lune run check     # what CI runs: license copies, format, lint, types, tests, builds
```

- The core is `lib/quarry`, the React bindings `lib/react-quarry`.
- Every file is `--!strict`. Values of unknown type are `unknown`, read through `Unknown.luau`;
  an `any` needs a comment directly above it starting `-- Invariant:` that says why it is safe.
- Port from TanStack's source where there is one, and name the file you ported from in the
  module's header comment.
- Every change in behaviour comes with a test in `lib/quarry/test` (Lune, with the fake scheduler:
  no waiting on real time). Check that the test fails without your change.
- StyLua formats the code: `stylua lib .lune`.

## Pull requests

- Branch from `main` and open the pull request against it. `main` is protected: CI must pass and a
  maintainer must approve before it merges.
- One change per pull request, described as what changed and why.
- Commit messages follow [Conventional Commits](https://www.conventionalcommits.org): `fix: ...`,
  `feat: ...`, `docs: ...`, with a body that says why.
- Add a line to `CHANGELOG.md` under "Unreleased" for anything a user would notice.

By contributing you agree your work is released under the [MIT License](https://github.com/quarry-luau/quarry/blob/main/LICENSE),
and that you follow the [Code of Conduct](CODE_OF_CONDUCT.md).
