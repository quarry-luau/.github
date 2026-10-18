<h1 align="center">Quarry for Luau</h1>

<p align="center">
  Server data for Roblox, the way the web does it: a port of
  <a href="https://tanstack.com/query">TanStack Query</a> to Luau.
</p>

Quarry caches what your game asks the server for, by key; shares one request between everything
that asks for the same thing; retries failures; refetches what you invalidate; and lets you update
the cache optimistically and roll it back. It is ported from TanStack's own source, so if you have
used TanStack Query on the web, you already know it.

### Packages

| Package | Wally | What it is |
|---|---|---|
| [**quarry**](https://github.com/quarry-luau/quarry/tree/main/lib/quarry) | `quarry-luau/quarry` | The core: `QueryClient`, its cache and observers. Plain Luau, no dependencies |
| [**react-quarry**](https://github.com/quarry-luau/quarry/tree/main/lib/react-quarry) | `quarry-luau/react-quarry` | Hooks for [React-Lua](https://github.com/jsdotlua/react-lua): `useQuery`, `useQuerySelect`, `useMutation` |

```toml
[dependencies]
Quarry = "quarry-luau/quarry@0.1.0"
ReactQuarry = "quarry-luau/react-quarry@0.1.0"
```

### Start here

- [README and API](https://github.com/quarry-luau/quarry#readme)
- [Differences from TanStack Query](https://github.com/quarry-luau/quarry#differences-from-tanstack-query)
- [Releases](https://github.com/quarry-luau/quarry/releases) (also as `.rbxm` models, for places without Wally)

Quarry is MIT licensed, as TanStack Query is. Issues and pull requests are welcome.
