# Speed to Lead — brand notes

The Speed to Lead marketing site inherits the Async Digital brand foundation. There is no separate visual identity for the service.

## Async Digital brand

Canonical tokens, voice rules, and visual decisions live in [async-digital-site](https://github.com/async-digital-ltd/async-digital-site). When this site disagrees with that one, that one wins.

- Canonical brand index: [`async-digital-site/BRAND.md`](https://github.com/async-digital-ltd/async-digital-site/blob/main/BRAND.md)
- Coding-agent derived view: [`async-digital-site/DESIGN.md`](https://github.com/async-digital-ltd/async-digital-site/blob/main/DESIGN.md)
- Voice rules: [`async-digital-site/brand/voice.md`](https://github.com/async-digital-ltd/async-digital-site/blob/main/brand/voice.md). Sentence case, no em dashes, no exclamation marks, no terminal punctuation on H1, en-GB, "we" not "I".
- Positioning: [`async-digital-site/brand/positioning.md`](https://github.com/async-digital-ltd/async-digital-site/blob/main/brand/positioning.md). Speed to Lead and Audient are never side-by-side as a services menu. Audient is not mentioned on Speed to Lead surfaces.

## Shared runtime tokens

This site loads `brand.css` and `brand.js` cross-domain from `https://async-digital.com/assets/...`. There is no local copy. When `BRAND.email`, `BRAND.privacyEmail`, palette, or type tokens change in the parent repo, this site picks them up at the next page load (subject to the `?v=` cache-bust on the script tag).

The page-specific CSS does carry a small block of design-system extras (spacing, radius, motion, base reset) that the canonical `brand.css` doesn't currently include. If `brand.css` upstream ever absorbs those, delete the block.

## Voice carve-outs for this site

None. All voice rules from the parent repo apply unchanged.

## Coding agents

If you're a coding agent generating or editing copy on this site, run [`marketing-auditor`](../../../.claude/agents/marketing-auditor.md) before publishing — it checks voice, positioning, cross-channel consistency, and propagation gaps against the canonical brand foundation.
