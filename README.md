# Horizon Libraries

The page that fronts **[libraries.horizon36596.org](https://libraries.horizon36596.org)** — a list of the
open-source libraries [Horizon](https://github.com/Horizon-36596), *FIRST* Tech Challenge team 36596,
publishes. No library's source is here; each one lives in its own repository and serves its own
documentation.

Three files, no build step, no framework, no dependency:

| File | What it is |
|------|------------|
| `index.html` | The list of libraries. |
| `404.html` | Served for any unmatched path. It exists mainly to explain the one mistake people will make — the path is the repository name and it is case-sensitive, so `/simloop` works and `/SimLoop` does not. |
| `horizon-mark.svg` | The team mark. |

## Why the library documentation lives under this domain

GitHub serves a project site under the organisation site's custom domain, at the project's repository
name, as long as that project has **no custom domain of its own**:

```
libraries.horizon36596.org/            <- this repository
libraries.horizon36596.org/simloop/    <- the Horizon-36596/simloop repository's Pages site
libraries.horizon36596.org/<next>/     <- whatever comes next, with no DNS work at all
```

So the domain is attached here, once, and every library repository leaves its **Custom domain** field
empty. That emptiness is load-bearing, which is the opposite of how a settings field usually reads: fill
it in on a library repository and that repository tries to claim a domain root instead of taking a path
under this one.

The settings this depends on, in this repository: **Settings → Pages → Source: Deploy from a branch →
`main` → `/ (root)`**, with **Custom domain** set to `libraries.horizon36596.org` and **Enforce HTTPS**
ticked once the certificate has issued. The DNS record is a `CNAME` on the name `libraries` pointing at
`horizon-36596.github.io`.

## Adding a library to the list

Copy the `<a class="library">` block in `index.html` and edit it. The tags are plain text: status,
language, licence, package root. Nothing on this page is generated, so nothing on it can go stale
without someone choosing not to update it.

## Keeping it looking like everything else

The colours, the three type faces and the amber→orange→crimson rule under the heading are the same
tokens as the documentation sites and the team website. If one of those drifts from the others, it is
wrong rather than different.

Dark only, with no toggle, because the team site declares `color-scheme: dark` and ships no light mode —
offering one here would mean inventing a second brand nobody has designed.

---

Copyright © 2026 Horizon (FTC 36596).
