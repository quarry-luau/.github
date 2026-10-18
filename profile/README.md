<p align="center">
  <img width="120" height="120" src="https://raw.githubusercontent.com/quarry-luau/.github/main/assets/logo.png" alt="Quarry logo">
</p>

<h1 align="center">Quarry</h1>

<p align="center">
  Open-source tools for Roblox: the web's best libraries, in Luau.
</p>

Quarry brings the libraries web developers rely on to Roblox, so what you already know from the web
works the same in a game: Quarry Query is TanStack Query ported from its own source, and
quarry-tailwind compiles Tailwind CSS's classes into Roblox's style engine. Every tool is a
`quarry-*` package for [Wally](https://wally.run), MIT licensed, typed in strict mode and tested.

### Tools

| Tool | Wally | What it is |
|---|---|---|
| [**quarry-query**](https://github.com/quarry-luau/quarry-query) | `quarry-luau/quarry-query` | [TanStack Query](https://tanstack.com/query) for Luau: server data cached by key, deduplicated, retried and kept fresh, with optimistic updates |
| [**quarry-react-query**](https://github.com/quarry-luau/quarry-query/tree/main/lib/quarry-react-query) | `quarry-luau/quarry-react-query` | Its hooks for [React-Lua](https://github.com/jsdotlua/react-lua): `useQuery`, `useQuerySelect`, `useMutation` |
| [**quarry-tailwind**](https://github.com/quarry-luau/quarry-tailwind) | `quarry-luau/quarry-tailwind` | [Tailwind CSS](https://tailwindcss.com) for React-Lua: class names compiled into Roblox's style engine, with states, transitions and Tailwind 4's theme |

```toml
[dependencies]
Query = "quarry-luau/quarry-query@0.1.0"
ReactQuery = "quarry-luau/quarry-react-query@0.1.0"
Tailwind = "quarry-luau/quarry-tailwind@0.1.0"
```

> The `quarry-luau` scope is waiting for Wally to approve it
> ([wally-index#131](https://github.com/UpliftGames/wally-index/pull/131)). Until then, each
> release has its packages as `.rbxm` models.

### Start here

- [Quarry Query](https://github.com/quarry-luau/quarry-query#readme): server data, cached and kept
  fresh, as TanStack Query does it
- [quarry-tailwind](https://github.com/quarry-luau/quarry-tailwind#readme): what compiles, the API,
  and where Roblox differs from the web
- [How to contribute](https://github.com/quarry-luau/.github/blob/main/CONTRIBUTING.md)

Issues and pull requests are welcome.
