<p align="center">
  <img width="120" height="120" src="https://raw.githubusercontent.com/quarry-luau/.github/main/assets/logo.png" alt="Quarry logo">
</p>

<h1 align="center">Quarry</h1>

<p align="center">
  Open-source tools for Roblox: the web's best libraries, ported to Luau.
</p>

Quarry ports the libraries web developers rely on to Luau, from their own source, so what you
already know from the web works the same in a Roblox game. Every tool is a `quarry-*` package on
[Wally](https://wally.run), MIT licensed, typed in strict mode and tested.

### Tools

| Tool | Wally | What it is |
|---|---|---|
| [**quarry-query**](https://github.com/quarry-luau/quarry-query) | `quarry-luau/quarry-query` | [TanStack Query](https://tanstack.com/query) for Luau: server data cached by key, deduplicated, retried and kept fresh, with optimistic updates |
| [**quarry-react-query**](https://github.com/quarry-luau/quarry-query/tree/main/lib/quarry-react-query) | `quarry-luau/quarry-react-query` | Its hooks for [React-Lua](https://github.com/jsdotlua/react-lua): `useQuery`, `useQuerySelect`, `useMutation` |
| **quarry-tailwind** (coming) | `quarry-luau/quarry-tailwind` | [Tailwind CSS](https://tailwindcss.com) classes compiled to Roblox's style engine, for React-Lua |

```toml
[dependencies]
Query = "quarry-luau/quarry-query@0.1.0"
ReactQuery = "quarry-luau/quarry-react-query@0.1.0"
```

### Start here

- [Quarry Query's README and API](https://github.com/quarry-luau/quarry-query#readme)
- [Releases](https://github.com/quarry-luau/quarry-query/releases), also as `.rbxm` models for places
  without Wally
- [How to contribute](https://github.com/quarry-luau/.github/blob/main/CONTRIBUTING.md)

Issues and pull requests are welcome.
