# Atlas documentation

Public documentation for **Atlas Community** — the self-hostable landscape and
asset catalogue. These pages are the targets the Atlas product deep-links into
from its in-app contextual help.

## Pages

- [Atlas AI](ai.md) — setup and chat for the in-product AI panel
  ([`#atlas-ai-setup`](ai.md#atlas-ai-setup),
  [`#atlas-ai-chat`](ai.md#atlas-ai-chat)).

## Doc-anchor registry

The product links against **stable slugs**, not against page layout. The
authoritative list of those slugs — what each one means and which markdown
target it resolves to — lives in the anchor registry:

- [`anchors.md`](anchors.md) — source of truth for Atlas deep-link anchors.

When you rename a heading, move a page, or add a new contextual-help target,
update `anchors.md` in the same change so the product and the docs stay in
agreement.
