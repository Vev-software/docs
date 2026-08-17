# Atlas doc-anchor registry

This file is the **single source of truth** for the documentation anchors the
Atlas product deep-links into. The product links against the **stable slugs**
listed here, so an anchor may be referenced by the UI before its page is fully
written. Keep this registry authoritative: when a slug's target changes, update
it here in the same change.

## How links resolve

The product builds documentation links from a configurable docs base URL. Its
default is the GitHub view of this repository:

```
https://github.com/Vev-software/docs/blob/main/docs
```

A registry entry's **target** is a repo-relative path plus a heading anchor,
resolved against that base. For example, target `atlas/ai.md#atlas-ai-setup`
becomes:

```
https://github.com/Vev-software/docs/blob/main/docs/atlas/ai.md#atlas-ai-setup
```

Anchors are GitHub's own heading slugs (lower-cased, spaces to hyphens,
punctuation dropped). A heading `## Atlas AI setup` therefore has the anchor
`#atlas-ai-setup`. **Do not change a Live heading's text without updating both
the heading and this registry**, or the product's deep link will break.

## Where these docs live (one site or two?)

**Decision (interim): no separate documentation site.** The product links
straight into this public repository on GitHub. There is currently **no**
`docs.vev.software` (or any other hosted `docs.*`) site, and neither one nor two
such sites are being stood up yet. This keeps product links stable now with
nothing extra to build, host or operate.

If a hosted site is introduced later, it should be generated from this same
markdown and preserve these slugs, so the registry stays the contract and the
product links keep resolving. Any change to that decision belongs in an ADR
under [`../adr/`](../adr/).

## Registry

Status legend: **Live** — target exists and the anchor resolves today;
**Planned** — slug is reserved and authoritative, page/anchor still to be
written.

| Slug              | Target                          | Status  | Description |
| ----------------- | ------------------------------- | ------- | ----------- |
| `atlas-ai-setup`  | `atlas/ai.md#atlas-ai-setup`    | Live    | Setting up the in-product AI panel: consent and bring-your-own-key (BYOK) provider setup. |
| `atlas-ai-chat`   | `atlas/ai.md#atlas-ai-chat`     | Live    | Using the AI chat panel grounded in the tenant's own landscape. |
| `new-asset`       | `atlas/assets.md#new-asset`     | Planned | Creating a new asset in the catalogue. |
| `edit-asset`      | `atlas/assets.md#edit-asset`    | Planned | Editing an existing asset's details. |
| `relationships`   | `atlas/assets.md#relationships` | Planned | Modelling relationships between assets. |
| `setup-copilot`   | `atlas/ai.md#atlas-ai-setup`    | Planned | Legacy slug for AI/copilot setup; superseded by `atlas-ai-setup`. Kept reserved to avoid reuse. |
| `data-catalogue`  | `atlas/catalogue.md#data-catalogue` | Planned | Browsing and searching the data catalogue. |
| `export`          | `atlas/export.md#export`        | Planned | Exporting landscape and asset data. |
| `secure-setup`    | `atlas/secure-setup.md#secure-setup` | Planned | Hardening a self-hosted Atlas deployment. |
| `users`           | `atlas/users.md#users`          | Planned | Managing users and access. |

## Adding or changing an anchor

1. Add or rename the heading in the target markdown file.
2. Add or update the row here (slug, target, status, description).
3. If the product deep-links the slug, keep the slug value stable even if the
   heading text changes wording — only re-map the target, never rename the slug
   the UI already ships.
