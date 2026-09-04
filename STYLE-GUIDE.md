# Style guide (internal)

This file is **not** listed in `SUMMARY.md`, so GitBook does not publish it. It exists so every page in this docs set is written the same way.

## 1. Audience and voice

- Write for a **merchant or a store staff member**, not a developer. Assume they know Shopify admin basics (products, variants, themes, orders) and nothing about this app.
- Second person, present tense, active voice: "Select **Save**", not "The Save button should be clicked".
- Never assume prior knowledge from another page. If a page needs an option set to exist, say so in **Before you start** and link to the page that creates one.
- No marketing language, no exclamation marks, no emoji in body text.
- Say what happens, then why it matters. Prefer a concrete number over "several" or "many".

## 2. Naming

| Always write | Never write |
| --- | --- |
| Globo Product Options, Variant | Globo Options / GPO / the plugin |
| option set | option group, options set |
| option (or option element) | field, element (in body text) |
| option value | choice, variant |
| **Label** | option name on product page |
| **Name** | name on cart page, internal name |
| add-on | addon, add on |
| add-on product | addon product, linked product |
| app embed | app embed block, embed block |
| app block | section block |
| Product Personalizer | personalizer app, live preview app |

UI text is copied **exactly** from the app and set in bold: **Min character**, **Advanced settings**, **Apply to All Products**. If the app writes it in sentence case, so do we. Never invent or "tidy up" a label.

Menu paths use `>` with bold segments: **Settings > Design > Theme style**.

## 3. Page skeleton

Every task page follows this order. Skip a section only if it genuinely does not apply.

1. Frontmatter: `description` (one sentence, no trailing period issues) + `icon` (Font Awesome slug).
2. `# Title` — matches the `SUMMARY.md` entry exactly.
3. One or two opening sentences: what this page gets you, and when you would use it.
4. `## Before you start` — required plan, required app embed, required option set, anything that must exist first.
5. `## Steps` — a `{% stepper %}` block. One action per step. Every step names the exact control the reader clicks.
6. `## Settings reference` — a table of every field on that screen: `Setting | Where | Default | What it does | Notes`.
7. `## Example` — one or two realistic scenarios with real numbers.
8. `## What customers see` — the storefront result.
9. `## Notes` — plan gating, POS support, theme dependencies, interactions with other features.
10. `## Notes` — plan gating, POS support, theme dependencies, and anything that does not fit the main flow.

Reference pages (shared settings, operator tables, matrices) may drop steps 5 and 8.

Pages do **not** end with a "Next steps" list — GitBook provides previous/next navigation and the section hub pages do the routing.

## 4. GitBook blocks

| Use | For |
| --- | --- |
| `{% stepper %}` / `{% step %}` | Any ordered procedure. Never a numbered markdown list for procedures. |
| `{% hint style="info" %}` | Useful aside, alternative path. |
| `{% hint style="warning" %}` | Something that will bite them (saving rules, POS gaps, theme gaps). |
| `{% hint style="danger" %}` | Data loss or irreversible actions. |
| `{% hint style="success" %}` | Confirmation that a step worked. |
| `<details>` | FAQ and troubleshooting entries. |
| Tables | Settings reference, operator lists, comparison matrices. |
| `<table data-view="cards">` | Only on hub pages, for routing to child pages. |
| `<figure>` | Every image. Always with `alt` and `figcaption`. |

Code fences: use `liquid`, `css`, `html`, `json`, or `text`. Never paste app internals (endpoints, job names, environment variables, feature flags).

## 5. Screenshots

Screenshots are added manually later. Until then every image points at the one shared placeholder.

Write each figure exactly like this:

```
<!-- SCREENSHOT: <id> | <where to capture> | <what must be visible> | <what to outline> -->

<figure><img src="../.gitbook/assets/placeholder.png" alt="<describe the finished screenshot>"><figcaption><p><complete sentence caption></p></figcaption></figure>
```

Rules:

- `<id>` is `kebab-case`, unique across the whole docs set, and prefixed by area: `home-`, `start-`, `set-`, `type-`, `clo-`, `addon-`, `pp-`, `store-`, `auto-`, `pos-`, `settings-`, `plan-`.
- The `alt` text describes the finished screenshot, not the placeholder — it must still read correctly after the real image is dropped in.
- The `figcaption` is a complete sentence, and adds information rather than repeating the heading.
- Relative path depth must match the page location: `.gitbook/assets/...` at root, `../.gitbook/assets/...` one level deep, `../../.gitbook/assets/...` two levels deep.
- Add every figure to `SCREENSHOTS.md` in the same commit.
- If an illustration would be nice but is not required, write `<!-- SCREENSHOT-OPTIONAL: <id> | ... -->` with no `<figure>`.

## 6. Plans and gated features

- Never print prices. Plan prices differ by pricing version and for Shopify Plus stores. Write "available on paid plans" or "requires the Advanced plan", and link to [Compare plans](plans/compare-plans.md) and the in-app **Pricing** page.
- When a setting is gated, say so inline in the settings table's **Notes** column, not in a separate paragraph.
- Feature names in plan tables must match the app's own **Pricing** page wording.

## 7. Links

- Internal links are relative and always include `.md`: `[Label](../option-types/shared-settings/label.md)`.
- Link the first meaningful mention on a page, not every mention.
- No page is an orphan: everything is reachable from `SUMMARY.md`, which is the navigation.
- Do not add a "Next steps" list at the end of a page. Cross-link inline instead, where the reader actually needs the link.
- External links: Shopify Help Center is fine. Do not link to the old docs site.

## 8. Never include

- Internal endpoints, queue or job names, environment variables, database columns.
- Hidden or staff-only settings, or feature flags that are off for merchants.
- Real store URLs or store IDs, tokens, personal email addresses, real people's names.
- Third-party brand logos, or invented theme or app names.
- `TODO`, `lorem`, or made-up links. The only permitted placeholder is the shared screenshot image.

## 9. Scope

- These docs describe the current version of the app only. Do not mention or contrast with the older app version.
- Support email: `contact@globo.io`.

Call it `## Notes` — never "Limits and notes". One trailing notes section per page, five bullets at most.

## 9. Troubleshooting

Do **not** add a `## Troubleshooting` section to a normal page. Troubleshooting lives on three dedicated pages only:

- `help/troubleshooting.md` — cross-cutting problems, plus the table of app messages.
- `conditional-logic/troubleshooting.md`
- `personalizer/troubleshooting.md`

Anything a reader must know to avoid a mistake belongs inline, as a `hint`, at the point where they would make it — not in a list of symptoms at the bottom.

## 10. Settings-page pattern

Two separate things, set by the merchant on 2026-08-31. Do not mix them up.

### Formatting — keep the existing form

Match the pages the merchant rewrote (SUMMARY 1–27). This is for consistency across the set:

- **HTML tables**, not markdown pipe tables.
- Meta table under each setting's `##`, in this exact form:
  `<table><thead><tr><th width="180">Tab</th><th>Advanced Settings</th></tr></thead><tbody><tr><td>Default</td><td>Off</td></tr><tr><td>Available on</td><td>...</td></tr></tbody></table>`
- Other tables: `<th width="290">` on the first column for two columns, `230` for three, `200` for more.
- Escape `&` as `&#x26;` inside table cells.
- `##` per setting. **No `###`.** Sub-topics are bold mini-headings on their own line: `**Prefix icon**`, `**How it behaves**`.
- No steppers and no `<details>` on a settings page.
- One or two `<figure>` blocks at the end. No `<!-- SCREENSHOT -->` markers.

### Writing — the merchant's brief

Per setting:

1. One sentence on what the setting does.
2. A table of its values, **one simple sentence each**.
3. A short recommendation, only when useful.
4. Critical limits or plan restrictions, briefly.

Cut these — the merchant called them redundant and distracting:

- **"Available on" lists.** Do not list which option types a setting appears on.
- Per-type availability tables.
- A separate `##` or paragraph per value. One table row is enough.
- Example-configuration tables and "which should I use" decision tables.
- Repeating the tab name under every setting. State it once in the intro.

State the default inline: `**Expand** (default)` in the value table, or "Off by default." in the description.

Wording rules:

- "customers", not "shoppers".
- American spelling: color, behavior, capitalization.
- Short sentences, one idea each, under about 25 words.
- No em dashes.
- State what a setting does before why or when to use it.
- Use the exact UI label for every setting, button, and field.

Do not write: marketing language, conversational hooks, storytelling, metaphors, analogies, dramatic statements, filler, repeated explanations, "why this matters" sections, generic advice, or claims about what customers "always" or "never" do.

Target 250–450 words for a settings page.

### Anchors

Bold mini-headings have no anchor. Before turning a `###` into one, run `grep -rn "page.md#anchor"` and repoint inbound links to the enclosing `##`.

## 11. Prose style for option-type pages

Set by the merchant on 2026-09-01, from their rewrites of `option-types/input-types/text.md` and `option-types/selection-types/select.md`. This is a **prose** rule. It does not change page structure: option-type pages keep What customers see, Basic Settings, Advanced Settings, Add-on pricing, Personalizer Settings, Examples, and Notes.

**Rewrite patterns**

| Instead of | Write |
| --- | --- |
| "A single-line box" | "A single-line field" |
| "The price belongs to the option" | "The price applies to the whole option" |
| "Prices belong to each option value" | "Prices are set for each option value" |
| "reaches the order as text" | "is stored in the order as text" |
| "the only two types with the Per character mode" | "the only two types that support the Per character mode" |
| "charges by how many characters the customer typed" | "charges based on the number of characters the customer enters" |
| "since there is one answer" | "because there is only one answer" |
| "use Textarea." | "use Textarea instead." |
| "If you need any of those" | "If you need any of the features above" |
| "a shopper can pick a sold-out value" | "A shopper could select a sold-out value" |
| "limited stock" | "limited inventory" |
| "past about thirty entries" | "for lists with more than about 30 entries" |
| "the natural way to price engraving" | "a natural way to price engraving" |

**Rules**

- Complete sentences. No telegraphic fragments such as "Long, plain, no prices."
- Split a sentence that carries two ideas. Do not join them with a dash.
- American spelling: color, personalization, capitalized, centimeter, behavior.
- Numerals for numbers of 10 and above.
- Name the setting rather than describing it: "**Min value** `10`", not "min `10`".
- Drop clever or anthropomorphic wording: "kinder", "fiddly", "invites requests", "the whole navigation experience", "strength and its limitation".
- Soften absolutes. "could select" rather than "can pick"; "a natural way" rather than "the natural way".
- Keep "field" for an input the customer types into. Keep the real UI labels **Select text box** and **search field** as they are.
- Em dashes are acceptable in moderation. The merchant kept them in `text.md`.

## 12. Prose patterns from the Conditional logic rewrite

Added 2026-09-01 from the merchant's rewrite of `conditional-logic/README.md`. These extend section 11.

**Turn inline example lists into bullets.** A sentence that strings three examples together becomes a `For example:` line and a bullet each.

Before: "Ask for a gift message only when they choose gift wrap. Ask for a shoe width only for the sizes you make it in."
After:

```
For example:

* Show a gift message field only when the customer selects gift wrapping.
* Show shoe width options only for sizes that are available in different widths.
```

**Word swaps**

| Instead of | Write |
| --- | --- |
| "It cannot read customer information" | keep "read" for data, but use "reference" for options |
| "conditions can only read options above" | "conditions can only reference options that appear above" |
| "It cannot look at an option below itself" | "It cannot use an option that appears later in the form as a condition" |
| "Every rule reads as one sentence" | "Every rule is presented as a single sentence" |
| "That is deliberate" | "This is intentional" |
| "unbuyable" | "impossible to purchase" |
| "it does not block Add to cart" | "it will not prevent the customer from clicking Add to cart" |
| "Test both branches." | "Be sure to test both branches of every rule." |
| "comes at two levels, and which you have depends on your plan" | "works at two levels, depending on your plan" |
| "One rule ... is impossible to get half-right" | "This is faster to set up, easier to maintain, and helps keep the logic consistent" |

**Rules**

- Split a two-idea sentence rather than joining it with a dash.
- Replace a clever closing clause with a plain statement of the benefit.
- Prefer "the customer" in explanations of behavior. "Shopper" is acceptable but not the default.
- "Plan-gated" becomes "may not be available on all plans".
- "Advanced level" of conditional logic is lower case in body text.
