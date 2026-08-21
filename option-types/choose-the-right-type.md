---
description: >-
  A decision table — start from what you are asking the customer for and end at
  the option type to use.
icon: circle-question
---

# Choose the right option type

Thirty-two types is a lot to hold in your head. This page works backwards: find what you are trying to ask for, and it tells you which type to use.

## By what you are asking for

<table><thead><tr><th width="330">You want the customer to…</th><th>Use</th></tr></thead><tbody><tr><td>Type a short message, name, or engraving</td><td><a href="input-types/text.md">Text</a></td></tr><tr><td>Type a longer message with line breaks</td><td><a href="input-types/textarea.md">Textarea</a></td></tr><tr><td>Enter a quantity or a measurement</td><td><a href="input-types/number.md">Number</a></td></tr><tr><td>Enter two or three measurements with units</td><td><a href="input-types/dimension.md">Dimension</a></td></tr><tr><td>Pick a number from a range, visually</td><td><a href="input-types/range-slider.md">Range slider</a></td></tr><tr><td>Give you a phone number</td><td><a href="input-types/phone.md">Phone</a></td></tr><tr><td>Give you an email address, for example for a digital gift</td><td><a href="input-types/email.md">Email</a></td></tr><tr><td>Choose a delivery or event date</td><td><a href="input-types/date-and-time-picker.md">Date and time picker</a></td></tr><tr><td>Upload a photo, logo, or artwork</td><td><a href="input-types/file-upload.md">File upload</a></td></tr><tr><td>Choose any colour at all</td><td><a href="input-types/color-picker.md">Color picker</a></td></tr><tr><td>Say yes or no to one thing</td><td><a href="input-types/switch.md">Switch</a>, or a single <a href="selection-types/checkbox.md">Checkbox</a></td></tr><tr><td>Choose one from a short list</td><td><a href="selection-types/radio-button.md">Radio button</a> or <a href="selection-types/button.md">Button</a></td></tr><tr><td>Choose one from a long list</td><td><a href="selection-types/dropdown.md">Dropdown</a> with search</td></tr><tr><td>Choose several from a list</td><td><a href="selection-types/checkbox.md">Checkbox</a></td></tr><tr><td>Choose a colour from your palette</td><td><a href="selection-types/color-swatch.md">Color swatch</a></td></tr><tr><td>Choose a pattern, material, or design you photograph</td><td><a href="selection-types/image-swatch.md">Image swatch</a></td></tr><tr><td>Choose a colour from a long list, compactly</td><td><a href="selection-types/color-dropdown.md">Color dropdown</a></td></tr><tr><td>Choose a design from a long list, compactly</td><td><a href="selection-types/image-dropdown.md">Image dropdown</a></td></tr><tr><td>Choose a font for their engraving</td><td><a href="selection-types/font-picker.md">Font picker</a></td></tr><tr><td>Jump to a related product instead of choosing an option</td><td><a href="selection-types/product-links.md">Product links</a></td></tr></tbody></table>

## When you are not asking for anything

<table><thead><tr><th width="330">You want to…</th><th>Use</th></tr></thead><tbody><tr><td>Group options under a heading, or make a group collapsible</td><td><a href="static-types/section.md">Section</a></td></tr><tr><td>Add a heading between options</td><td><a href="static-types/heading.md">Heading</a></td></tr><tr><td>Separate two groups visually</td><td><a href="static-types/divider.md">Divider</a> or <a href="static-types/spacing.md">Spacing</a></td></tr><tr><td>Explain something in a sentence or two</td><td><a href="static-types/paragraph.md">Paragraph</a></td></tr><tr><td>Explain something at length without lengthening the page</td><td><a href="static-types/pop-up-modal.md">Pop-up modal</a></td></tr><tr><td>Show a size table</td><td><a href="static-types/size-chart.md">Size chart</a></td></tr><tr><td>Show care instructions, delivery information, and returns in one place</td><td><a href="static-types/tabs.md">Tabs</a></td></tr><tr><td>Embed something the other types cannot produce</td><td><a href="static-types/html.md">HTML</a></td></tr><tr><td>Send a fixed value to the order without showing anything</td><td><a href="input-types/hidden-field.md">Hidden field</a></td></tr></tbody></table>

## Choices that look similar

### Text or Textarea?

**Text** is one line; **Textarea** is several. Otherwise they are almost identical, including add-on pricing and the Personalizer. Use Text for names and engravings — the single line discourages people from writing an essay you cannot fit. Use Textarea for gift messages and instructions.

One difference in the Personalizer: Textarea offers **Text alignment**, **Width**, and **Height** because it can be a block of text; Text offers **Curve** and **Auto-fit max width** because it is a single line.

### Select or Dropdown?

<table><thead><tr><th width="230"></th><th width="230">Select</th><th>Dropdown</th></tr></thead><tbody><tr><td>Appearance</td><td>The browser's native dropdown</td><td>Styled by the app, matching your design settings</td></tr><tr><td>Search</td><td>No</td><td>Yes</td></tr><tr><td>Colour or image per entry</td><td>No</td><td>Yes</td></tr><tr><td>Min and max selections</td><td>No</td><td>Yes</td></tr><tr><td>Out-of-stock display</td><td>No</td><td>Yes</td></tr><tr><td>Personalizer</td><td>No</td><td>Yes</td></tr></tbody></table>

**Select** is the plain, dependable choice — it uses the device's own picker, which mobile shoppers know well. **Dropdown** is the one to use for anything richer.

### Radio button, Button, or Color swatch?

All three let the customer choose one of several, and all three support **Swatch style** so they can show colours or images. The difference is presentation:

* **Radio button** — a vertical list. Best when values have long names or per-value help text.
* **Button** — a row of tappable buttons. Best for short values like sizes.
* **Color swatch** / **Image swatch** — a grid. Best when the choice is visual, and the only two that support slider layouts.

### Switch or Checkbox?

A **Switch** is one yes-or-no with its own label — "Add gift wrap". A **Checkbox** is a list, which happens to work fine with one entry. Use Switch for a single toggle, Checkbox as soon as there are two or more things to tick.

### Number, Range slider, or Dimension?

* **Number** — a typed number. Precise, and the shopper can enter any value in range.
* **Range slider** — dragged. Good for approximate choices, bad for precise ones.
* **Dimension** — two or three measurements with their own units, and its own pricing formula. Use it for made-to-measure products.

### Color picker or Color swatch?

**Color picker** lets the shopper choose *any* colour, from the whole spectrum. **Color swatch** lets them choose from *your* colours. If you can only produce twelve colours, use swatches — a picker invites requests you cannot fulfil.

### File upload or the Personalizer?

They work together rather than competing. **File upload** collects the file. Turning on **Personalizer Settings** on that same option additionally draws the uploaded image onto the product photo, live. See [Product Personalizer](../personalizer/README.md).

## By what you need it to do

<table><thead><tr><th width="330">You need…</th><th>Types that can</th></tr></thead><tbody><tr><td>A price attached to the whole option</td><td>Text, Textarea, Number, Switch, Color picker, Dimension</td></tr><tr><td>A price attached to each choice</td><td>All nine selection types with values</td></tr><tr><td>The customer's content drawn on the product photo</td><td>Text, Textarea, Number, File upload, Dropdown, Color dropdown, Image dropdown, Radio button, Checkbox, Button, Color swatch, Image swatch</td></tr><tr><td>Stock tracking per choice</td><td>Any selection type, with values linked to add-on products</td></tr><tr><td>To work in Shopify POS</td><td>Everything except Dimension and Product links</td></tr><tr><td>Several choices at once</td><td>Checkbox always; Select, Dropdown, Color dropdown, Image dropdown, Button, Color swatch, Image swatch with <strong>Allow multiple</strong></td></tr><tr><td>Search within a long list</td><td>Dropdown, Color dropdown, Image dropdown, Font picker</td></tr><tr><td>A collapsible or slider layout</td><td>Checkbox, Radio button, Button, Color swatch, Image swatch</td></tr></tbody></table>

## A rule of thumb

Fewer, simpler options sell better than more, cleverer ones. Before adding a type, ask whether the answer changes what you make or ship. If it does not, leave it out — and if it only matters sometimes, put it behind [conditional logic](../conditional-logic/README.md) so most shoppers never see it.

## Next steps

* [Input types](input-types/README.md), [Selection types](selection-types/README.md), [Static types](static-types/README.md)
* [Shared settings](shared-settings/README.md)
* [Walkthrough: engraving and gift wrap](../getting-started/first-option-set-walkthrough.md) — several types working together.
