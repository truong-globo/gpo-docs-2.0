# Screenshot shot list

Internal working file — not part of the published documentation and not listed in `SUMMARY.md`.

**150 required shots**, 2 optional, across 110 pages. Generated from the `<!-- SCREENSHOT: ... -->` markers in the pages, in `SUMMARY.md` order.

Every `<figure>` currently points at `.gitbook/assets/placeholder.png`. Replace that path with the real file as each shot is taken.

## Conventions

* Capture on the **production** app, never a dev build.
* Viewport at least 1920 wide; use full-page capture when the content is taller than the viewport.
* No mouse cursor in frame. Hide live chat completely before capturing, and clear any focus ring.
* Outline the part of the widget the caption is about — not the whole card, not the whole page.
* Arrows only where the target could be confused with something beside it.
* Save as `.gitbook/assets/screenshot-<area>-<subject>.png`.

## Required shots


### Globo Product Options, Variant

`README.md`

**1. `home-dashboard`**

* Where: App admin → Dashboard
* Must show: Toàn trang 1920×1400: Setup guide card + chart analytics
* Outline: Không khoanh vùng


### Install the app

`getting-started/install-the-app.md`

**2. `start-appstore-listing`**

* Where: Shopify App Store, trang listing "Globo Product Options, Variant"
* Must show: Tiêu đề app + nút Install
* Outline: Khoanh nút Install

**3. `start-pricing-first-run`**

* Where: App admin → Pricing, lần đầu cài
* Must show: 4 plan card + switch Monthly/Yearly + nút "Continue as Free" và "Start 14-day trial"
* Outline: Khoanh switch Monthly/Yearly và 1 nút Start 14-day trial (có mũi tên nhỏ vì nhiều card giống nhau)

**4. `start-dashboard-setup-guide`**

* Where: App admin → Dashboard
* Must show: Setup guide card mở, thấy 3 step + progress "0 / 3 completed"
* Outline: Khoanh riêng card Setup guide


### Tour of the app

`getting-started/admin-tour.md`

**5. `start-nav-menu`**

* Where: App admin, mở bất kỳ trang
* Must show: Menu trái của app với đủ 7 item
* Outline: Khoanh cả khối menu

**6. `start-dashboard-full`**

* Where: App admin → Dashboard
* Must show: Toàn trang: setup guide, app embed status, app block status, chart, quick tutorial
* Outline: Không khoanh

**7. `start-builder-anatomy`**

* Where: App admin → Option Sets → mở 1 option set
* Must show: 4 vùng: header, left rail, panel Setup flow, preview
* Outline: Khoanh 4 vùng, mỗi vùng 1 outline (dùng mũi tên nhỏ để phân biệt left rail và panel)


### Quickstart

`getting-started/quickstart.md`

**8. `start-qs-create-from-scratch`**

* Where: App admin → Option Sets
* Must show: Nút Create option set đang mở, thấy 2 lựa chọn Create from scratch và Use a template
* Outline: Khoanh "Create from scratch" (mũi tên nhỏ vì có 2 mục giống nhau)

**9. `start-qs-name`**

* Where: App admin → builder, mới tạo
* Must show: Ô tên option set ở header đang nhập "Engraving"
* Outline: Khoanh ô tên

**10. `start-qs-add-option`**

* Where: App admin → builder → Build option
* Must show: Popover chọn option type đang mở, thấy 3 nhóm Input / Selection / Static
* Outline: Khoanh mục "Text" trong nhóm Input (mũi tên nhỏ vì danh sách dài)

**11. `start-qs-basic-settings`**

* Where: App admin → builder → chọn option Text
* Must show: Tab Basic Settings với Label và Name đã điền "Engraving text"
* Outline: Khoanh 2 field Label và Name

**12. `start-qs-assign-products`**

* Where: App admin → builder → Assign products
* Must show: 3 khối Manual Selection / Automatic Rules / Apply to All Products, khối Apply to All Products đang bật
* Outline: Khoanh khối Apply to All Products

**13. `start-qs-status-active`**

* Where: App admin → builder → menu Status
* Must show: Status đặt Active, Sales channels tick Online Store
* Outline: Khoanh khối Status và Sales channels

**14. `start-qs-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Field "Engraving text" hiện phía trên nút Add to cart
* Outline: Khoanh riêng field do app tạo, không khoanh cả form


### Enable the app embed

`getting-started/enable-the-app-embed.md`

**15. `start-embed-setupguide-step2`**

* Where: App admin → Dashboard
* Must show: Setup guide card, step 2 đang mở với nút "Enable app embed"
* Outline: Khoanh nút Enable app embed

**16. `start-embed-theme-setup`**

* Where: App admin → Settings → Theme Setup
* Must show: Dropdown chọn theme + badge Deactivated + nút Go to Theme Editor
* Outline: Khoanh badge và nút Go to Theme Editor

**17. `start-embed-theme-editor-toggle`**

* Where: Shopify theme editor → App embeds
* Must show: Danh sách app embeds, toggle "Globo Product Options" đang bật
* Outline: Khoanh dòng Globo Product Options (mũi tên nhỏ vì nhiều dòng giống nhau)


### Add the app block

`getting-started/add-the-app-block.md`

**18. `start-block-add-button`**

* Where: App admin → Dashboard
* Must show: Card "Active app blocks" với số lượng và nút Add app block
* Outline: Khoanh nút Add app block

**19. `start-block-drag-position`**

* Where: Shopify theme editor → product template
* Must show: Block "Globo Product Options" trong danh sách block của section, đang được đặt trên nút Add to cart
* Outline: Khoanh dòng block Globo Product Options (mũi tên nhỏ vì nhiều block trong list)


### Walkthrough: engraving and gift wrap

`getting-started/first-option-set-walkthrough.md`

**20. `start-wt-section-label`**

* Where: App admin → builder → chọn Section
* Must show: Field Label của Section đang là "Personalize your bracelet" + dropdown Style
* Outline: Khoanh field Label và dropdown Style

**21. `start-wt-text-basic`**

* Where: App admin → builder → option Text
* Must show: Basic Settings đã điền Label, Name, Max character 20, Character counter = Show
* Outline: Khoanh nhóm Min/Max character + Character counter

**22. `start-wt-addon-add-price`**

* Where: App admin → builder → option Text → mở dialog Price
* Must show: Dialog Add-on Configuration với 3 tab, tab "Add price" đang chọn, giá 5
* Outline: Khoanh hàng 3 tab (mũi tên nhỏ vào tab Add price)

**23. `start-wt-checkbox-values`**

* Where: App admin → builder → option Checkbox
* Must show: Bảng Option values với các cột Value / Price / Product / Action, 1 dòng "Yes, wrap it as a gift"
* Outline: Khoanh cả bảng Option values

**24. `start-wt-addon-auto-product`**

* Where: App admin → builder → dialog Price của 1 option value
* Must show: Tab "Automatically generate product" với giá 3
* Outline: Khoanh field giá trong tab

**25. `start-wt-clo-rule`**

* Where: App admin → builder → option Textarea
* Must show: Khối Conditional logic đã bật, rule Show / all conditions / Gift wrap / contains / "Yes, wrap it as a gift"
* Outline: Khoanh khối rule

**26. `start-wt-preview-logic`**

* Where: App admin → builder
* Must show: Preview bên phải: Gift wrap đã tick và Gift message hiện ra
* Outline: Khoanh vùng Gift message vừa xuất hiện trong preview

**27. `start-wt-automatic-rule`**

* Where: App admin → builder → Assign products
* Must show: Automatic Rules đang bật với điều kiện Product tag is equal to engravable
* Outline: Khoanh dòng điều kiện

**28. `start-wt-storefront-filled`**

* Where: Storefront → trang sản phẩm
* Must show: Cả 3 option hiện ra, Gift wrap đã tick, Gift message hiện, giá đã tăng
* Outline: Khoanh riêng widget do app tạo

**29. `start-wt-cart`**

* Where: Storefront → trang cart
* Must show: Line item chính có option properties + line item add-on gift wrap riêng
* Outline: Khoanh phần properties dưới line item và dòng add-on


### Label vs Name

`concepts/label-vs-name.md`

**30. `concept-label-name-fields`**

* Where: App admin → builder → 1 option bất kỳ
* Must show: 2 field Label và Name cạnh nhau trong Basic Settings, có icon tooltip
* Outline: Khoanh cả 2 field


### Working with option values

`concepts/option-values.md`

**31. `concept-ov-table`**

* Where: App admin → builder → 1 option kiểu Checkbox hoặc Dropdown
* Must show: Bảng Option values đầy đủ cột + 3 nút Add value / Bulk add / Delete all option values
* Outline: Khoanh hàng nút ở dưới bảng

**32. `concept-ov-bulk-add`**

* Where: App admin → builder → dialog Bulk Add Values
* Must show: Textarea nhiều dòng giá trị + nút Select
* Outline: Không khoanh (modal đơn)


### Status and sales channels

`concepts/status-and-sales-channels.md`

**33. `concept-status-header`**

* Where: App admin → builder
* Must show: Khối Status cạnh tên option set, đang bật Active
* Outline: Khoanh khối Status

**34. `concept-sales-channels`**

* Where: App admin → builder → mở popover Sales channels
* Must show: 2 dòng Online Store và Point of Sale với switch
* Outline: Khoanh popover


### Plans and locked features

`concepts/plans-and-feature-gating.md`

**35. `concept-locked-setting`**

* Where: App admin → builder → 1 setting bị khoá (ví dụ Personalizer Settings trên plan thấp)
* Must show: Field mờ + link upgrade
* Outline: Khoanh field bị khoá và link upgrade

**36. `concept-pricing-compare`**

* Where: App admin → Pricing
* Must show: Bảng so sánh feature theo nhóm, plan hiện tại được đánh dấu
* Outline: Khoanh cột plan hiện tại


### Create an option set

`option-sets/create-an-option-set.md`

**37. `set-create-setup-flow`**

* Where: App admin → builder mới tạo
* Must show: Tab Setup flow với 2 step Build option / Assign products + dòng status phía trên
* Outline: Khoanh 2 thẻ step


### Build your options

`option-sets/build-options.md`

**38. `set-build-option-list`**

* Where: App admin → builder → Build option
* Must show: Danh sách option với icon, title, description, badge Required và badge giá
* Outline: Khoanh 1 dòng option kèm các badge (mũi tên nhỏ vì nhiều dòng)

**39. `set-build-change-type`**

* Where: App admin → builder → panel setting của 1 option
* Must show: Control đổi option type ở header panel đang mở
* Outline: Khoanh control đổi type


### Live preview and inspector

`option-sets/live-preview-and-inspector.md`

**40. `set-preview-header-controls`**

* Where: App admin → builder
* Must show: Header với các control: editor/preview, desktop/mobile, inspector, language
* Outline: Khoanh nhóm control (mũi tên nhỏ vào nút inspector)

**41. `set-preview-inspector`**

* Where: App admin → builder, inspector đang bật
* Must show: 1 option trong preview được highlight kèm thanh action Duplicate / Half width / Full width / Hide / Delete
* Outline: Khoanh thanh action

**42. `set-preview-matching-products`**

* Where: App admin → builder → modal Preview matching products
* Must show: Danh sách sản phẩm khớp rule, mỗi dòng có ảnh, tên, vendor, type, status, nút Preview
* Outline: Không khoanh (modal đơn)


### Assign to products

`option-sets/assign-to-products.md`

**43. `set-assign-three-methods`**

* Where: App admin → builder → Assign products
* Must show: 3 khối Manual Selection / Automatic Rules / Apply to All Products, đều đang tắt
* Outline: Khoanh 3 khối

**44. `set-assign-manual-table`**

* Where: App admin → builder → Assign products → Manual Selection đang bật
* Must show: Bảng sản phẩm đã chọn với ảnh, tên, status + nút Select products và Deselect all products
* Outline: Khoanh bảng và 2 nút

**45. `set-assign-automatic-conditions`**

* Where: App admin → builder → Assign products → Automatic Rules đang bật
* Must show: "Products must match: all conditions" + 2 điều kiện (Product tag is equal to ... và Product type is equal to ...) + nút Add another condition
* Outline: Khoanh vùng điều kiện


### Assign to customers

`option-sets/assign-to-customers.md`

**46. `set-customers-methods`**

* Where: App admin → builder → tab Customers
* Must show: 3 khối Everyone / Manual Selection / Automatic Rules, Everyone đang bật
* Outline: Khoanh 3 khối

**47. `set-customers-automatic`**

* Where: App admin → builder → tab Customers → Automatic Rules đang bật
* Must show: Điều kiện "Customer tags is equal to wholesale" + selector all/any conditions
* Outline: Khoanh dòng điều kiện


### Assign to countries

`option-sets/assign-to-countries.md`

**48. `set-countries-panel`**

* Where: App admin → builder → tab Countries
* Must show: Country restrictions đang bật, chọn Include, đã chọn vài quốc gia
* Outline: Khoanh 2 radio Include/Exclude và ô chọn quốc gia


### Manage option sets

`option-sets/manage-option-sets.md`

**49. `set-list-overview`**

* Where: App admin → Option Sets
* Must show: Bảng danh sách với các cột, tab filter All/Active/Draft, ô search, nút Create option set
* Outline: Không khoanh

**50. `set-list-bulk-actions`**

* Where: App admin → Option Sets, đã tick vài dòng
* Must show: Thanh bulk action với Set as active / Set as draft / Duplicate + menu chứa Save as Template và Delete
* Outline: Khoanh thanh bulk action


### Duplicate and delete

`option-sets/duplicate-and-delete.md`

**51. `set-duplicate-result`**

* Where: App admin → Option Sets sau khi duplicate
* Must show: 2 dòng cùng tên, cùng status Active
* Outline: Khoanh 2 dòng trùng tên (mũi tên nhỏ)


### Import and export

`option-sets/import-and-export.md`

**52. `set-export-modal`**

* Where: App admin → Option Sets → modal Export option sets
* Must show: Nhóm "Export" với 3 lựa chọn và nhóm "Export as" với Plain CSV file
* Outline: Không khoanh (modal đơn)

**53. `set-import-modal`**

* Where: App admin → Option Sets → modal Import
* Must show: Drop zone + link sample CSV template + danh sách "Select app for import" 7 lựa chọn + checkbox Set all imported option sets as Active
* Outline: Khoanh khối "Select app for import"


### Option set analytics

`option-sets/analytics.md`

**54. `set-analytics-open`**

* Where: App admin → Option Sets
* Must show: Menu action của 1 dòng đang mở với mục View Analytics
* Outline: Khoanh mục View Analytics

**55. `set-analytics-summary`**

* Where: App admin → Analytics của 1 option set
* Must show: 5 ô số liệu Total revenue / Revenue from add-ons / Total products / Total orders / Average order value kèm chỉ số so sánh
* Outline: Khoanh hàng 5 ô

**56. `set-analytics-charts`**

* Where: App admin → Analytics của 1 option set
* Must show: Các chart: Total sales, Most valued options, Total products quantity, Orders revenue distribution, Average order value
* Outline: Không khoanh


### Labels and visibility

`option-types/shared-settings/labels-and-visibility.md`

**57. `type-shared-label-name`**

* Where: App admin → builder → 1 option Text
* Must show: Basic Settings: Label, Name, Required field, Hidden label
* Outline: Khoanh 4 field


### Placeholder and help text

`option-types/shared-settings/placeholder-and-help-text.md`

**58. `type-shared-helptext-positions`**

* Where: Storefront → trang sản phẩm
* Must show: 4 option giống nhau minh hoạ 4 vị trí help text khác nhau
* Outline: Khoanh từng vùng help text


### Required field and default value

`option-types/shared-settings/required-and-default-value.md`

**59. `type-shared-required-default`**

* Where: App admin → builder → 1 option Select
* Must show: Basic Settings với Required field bật và Default value đã chọn 1 giá trị
* Outline: Khoanh Required field và Default value


### Limits

`option-types/shared-settings/limits.md`

**60. `type-shared-limits`**

* Where: App admin → builder → option Text
* Must show: Basic Settings với Min character, Max character, Character counter = Show
* Outline: Khoanh nhóm min/max và character counter


### Text input rules

`option-types/shared-settings/text-input-rules.md`

**61. `type-shared-text-rules`**

* Where: App admin → builder → option Text → tab Advanced Settings
* Must show: Allowed value và Text transform
* Outline: Khoanh 2 field


### Selection behaviour

`option-types/shared-settings/selection-behaviour.md`

**62. `type-shared-selection-behaviour`**

* Where: App admin → builder → option Dropdown
* Must show: Allow multiple ở Basic Settings; Search suggestion và Not allow deselect ở Advanced Settings
* Outline: Khoanh Allow multiple và nhóm Search suggestion / Not allow deselect


### Swatch style and previews

`option-types/shared-settings/swatch-style-and-previews.md`

**63. `type-shared-swatch-style`**

* Where: App admin → builder → option Checkbox
* Must show: Swatch style ở Basic Settings với 3 lựa chọn Default / Color / Image
* Outline: Khoanh field Swatch style

**64. `type-shared-tooltip-zoom`**

* Where: Storefront → trang sản phẩm
* Must show: Hover 1 image swatch, tooltip Text & image hiện ảnh phóng to
* Outline: Khoanh tooltip


### Collapsible layouts and sliders

`option-types/shared-settings/collapsible-layouts-and-sliders.md`

**65. `type-shared-slider-settings`**

* Where: App admin → builder → option Image swatch → Advanced Settings
* Must show: Enable custom layout bật, Layout type = Slider, các setting Number of rows / Swatches per row / arrows / indicators / Slider style
* Outline: Khoanh nhóm slider

**66. `type-shared-slider-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Image swatch dạng slider 2 hàng, có arrow, thấy 1 swatch bị cắt ở mép
* Outline: Khoanh vùng slider


### Direction, width, and CSS

`option-types/shared-settings/direction-width-and-css.md`

**67. `type-shared-width-css`**

* Where: App admin → builder → 1 option → Advanced Settings
* Must show: Direction style, Column width (6 lựa chọn), HTML class
* Outline: Khoanh Column width


### Prefix, suffix, and icons

`option-types/shared-settings/prefix-suffix-and-icons.md`

**68. `type-shared-prefix-suffix`**

* Where: App admin → builder → option Number → Advanced Settings
* Must show: Prefix (Icon/Text), Prefix icon hoặc Prefix text, Suffix
* Outline: Khoanh nhóm Prefix/Suffix

**69. `type-shared-prefix-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 field Number có prefix "$" và suffix "cm" hiển thị trong ô input
* Outline: Khoanh vùng prefix và suffix


### Out of stock options

`option-types/shared-settings/out-of-stock-options.md`

**70. `type-shared-oos-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 hàng color swatch trong đó 1 swatch hết hàng đang bị blur
* Outline: Khoanh swatch bị blur


### Conditional logic and add-on fields

`option-types/shared-settings/conditional-logic-and-add-on-fields.md`

**71. `type-shared-clo-field`**

* Where: App admin → builder → 1 option
* Must show: Switch Conditional logic đã bật, rule builder hiện bên dưới
* Outline: Khoanh switch và rule builder

**72. `type-shared-addon-fields`**

* Where: App admin → builder → option Text
* Must show: Add-on Settings với field Price và dropdown Advanced settings; nếu chọn Fixed quantity thì hiện Set quantity
* Outline: Khoanh nhóm Add-on Settings


### Text

`option-types/input-types/text.md`

**73. `type-text-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 field Text có label, placeholder, help text và character counter
* Outline: Khoanh riêng field Text


### Textarea

`option-types/input-types/textarea.md`

**74. `type-textarea-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 field Textarea nhiều dòng đã nhập vài dòng chữ, có counter
* Outline: Khoanh riêng field Textarea


### Number

`option-types/input-types/number.md`

**75. `type-number-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 field Number có prefix/suffix và help text nêu min-max
* Outline: Khoanh riêng field Number


### Phone

`option-types/input-types/phone.md`

**76. `type-phone-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Field Phone có validate bật: cờ quốc gia + mã vùng ở đầu ô
* Outline: Khoanh vùng cờ và mã vùng


### Email

`option-types/input-types/email.md`

**77. `type-email-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Field Email với help text, và trạng thái lỗi "Invalid email"
* Outline: Khoanh field và thông báo lỗi


### Date and time picker

`option-types/input-types/date-and-time-picker.md`

**78. `type-datetime-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Field Date đang mở calendar, có ngày bị chặn (cuối tuần) không chọn được
* Outline: Khoanh calendar và vài ngày bị chặn


### File upload

`option-types/input-types/file-upload.md`

**79. `type-file-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Field File upload đã upload 1 ảnh, hiện thumbnail preview
* Outline: Khoanh vùng upload và thumbnail


### Color picker

`option-types/input-types/color-picker.md`

**80. `type-colorpicker-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Field Color picker đang mở bảng chọn màu
* Outline: Khoanh vùng picker


### Switch

`option-types/input-types/switch.md`

**81. `type-switch-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 Switch đã bật, có label và switch label, giá phụ phí hiện cạnh
* Outline: Khoanh riêng switch


### Range slider

`option-types/input-types/range-slider.md`

**82. `type-range-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 Range slider với giá trị hiện tại, prefix/suffix
* Outline: Khoanh riêng slider


### Dimension

`option-types/input-types/dimension.md`

**83. `type-dimension-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 option Dimension với 2-3 ô Width / Height / Depth kèm unit
* Outline: Khoanh cả nhóm Dimension

**84. `type-dimension-values`**

* Where: App admin → builder → option Dimension
* Must show: Bảng option values với 3 hàng X/Y/Z và các cột Label / Placeholder / Unit / Default value / Min / Max
* Outline: Khoanh cả bảng


### Select

`option-types/selection-types/select.md`

**85. `type-select-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 native Select đang đóng và 1 đang mở
* Outline: Khoanh riêng field Select


### Dropdown

`option-types/selection-types/dropdown.md`

**86. `type-dropdown-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Dropdown đang mở, có search box và vài entry, 1 entry hết hàng bị blur
* Outline: Khoanh vùng dropdown đang mở


### Color dropdown

`option-types/selection-types/color-dropdown.md`

**87. `type-colordropdown-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Color dropdown đang mở, mỗi entry có chip màu + tên
* Outline: Khoanh vùng dropdown đang mở


### Image dropdown

`option-types/selection-types/image-dropdown.md`

**88. `type-imagedropdown-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Image dropdown đang mở, mỗi entry có ảnh nhỏ + tên
* Outline: Khoanh vùng dropdown đang mở


### Radio button

`option-types/selection-types/radio-button.md`

**89. `type-radio-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Radio list dọc, mỗi value có help text riêng, 1 value đang chọn
* Outline: Khoanh riêng nhóm radio


### Checkbox

`option-types/selection-types/checkbox.md`

**90. `type-checkbox-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Checkbox list với vài value đã tick, mỗi value có giá phụ phí hiện cạnh
* Outline: Khoanh riêng nhóm checkbox


### Button

`option-types/selection-types/button.md`

**91. `type-button-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 hàng button size (S M L XL) với 1 button đang chọn và 1 button hết hàng bị strike-through
* Outline: Khoanh riêng hàng button


### Color swatch

`option-types/selection-types/color-swatch.md`

**92. `type-colorswatch-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Grid color swatch, 1 chip đang chọn, 1 chip hết hàng bị blur, hover hiện tooltip tên màu
* Outline: Khoanh riêng grid swatch


### Image swatch

`option-types/selection-types/image-swatch.md`

**93. `type-imageswatch-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Grid image swatch, 1 swatch đang chọn, hover 1 swatch hiện tooltip Text & image phóng to
* Outline: Khoanh riêng grid và tooltip


### Font picker

`option-types/selection-types/font-picker.md`

**94. `type-fontpicker-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Font picker đang mở, mỗi tên font được vẽ bằng chính font đó
* Outline: Khoanh vùng danh sách font


### Product links

`option-types/selection-types/product-links.md`

**95. `type-productlinks-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Product links dạng button, mỗi button là 1 sản phẩm khác
* Outline: Khoanh riêng nhóm product links


### Section

`option-types/static-types/section.md`

**96. `type-section-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 2 Section: 1 style Default mở, 1 style Collapse đang đóng
* Outline: Khoanh 2 tiêu đề section


### Heading

`option-types/static-types/heading.md`

**97. `type-heading-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 2 Heading khác cấp (h3 và h5) phân tách các nhóm option
* Outline: Khoanh 2 heading


### Divider

`option-types/static-types/divider.md`

**98. `type-divider-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 2 divider khác style (solid và dashed) phân tách các nhóm option
* Outline: Khoanh 2 divider


### Paragraph

`option-types/static-types/paragraph.md`

**99. `type-paragraph-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 Paragraph có chữ in đậm và 1 link, đặt trên nhóm option
* Outline: Khoanh riêng paragraph


### Pop-up modal

`option-types/static-types/pop-up-modal.md`

**100. `type-modal-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Link mở modal và modal đã mở với nội dung rich text
* Outline: Khoanh link và modal


### HTML

`option-types/static-types/html.md`

**101. `type-html-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: 1 block HTML tuỳ chỉnh (ví dụ bảng nhỏ hoặc badge) trong widget
* Outline: Khoanh riêng block HTML


### Size chart

`option-types/static-types/size-chart.md`

**102. `type-sizechart-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Link mở size chart và bảng size đã mở
* Outline: Khoanh link và bảng

**103. `type-sizechart-presets`**

* Where: App admin → builder → option Size chart
* Must show: Danh sách 13 preset dạng icon để chọn
* Outline: Khoanh vùng chọn preset


### Tabs

`option-types/static-types/tabs.md`

**104. `type-tabs-storefront`**

* Where: Storefront → trang sản phẩm
* Must show: Tabs ngang với 3 tab, tab đầu đang mở với nội dung
* Outline: Khoanh hàng tab và panel


### Overview

`conditional-logic/README.md`

**105. `clo-rule-anatomy`**

* Where: App admin → builder → 1 option có conditional logic bật
* Must show: Toàn bộ rule builder: Show/Hide, All/Any, 1 dòng điều kiện
* Outline: Khoanh 4 phần: action, match, source, operator+value


### Turn on conditional logic

`conditional-logic/turn-it-on.md`

**106. `clo-switch-on`**

* Where: App admin → builder → 1 option
* Must show: Switch Conditional logic vừa bật, rule builder xuất hiện bên dưới
* Outline: Khoanh switch


### Build a condition

`conditional-logic/build-a-condition.md`

**107. `clo-three-dropdowns`**

* Where: App admin → builder → rule builder
* Must show: 1 dòng điều kiện với 3 ô: source, operator, value
* Outline: Khoanh 3 ô, đánh số 1-2-3


### Conditions based on Shopify variants

`conditional-logic/conditions-on-shopify-variants.md`

**108. `clo-variant-condition`**

* Where: App admin → builder → rule builder
* Must show: Điều kiện với source "Shopify variant", operator "is equal to", value "Silver", ô value có suffix hiển thị locale
* Outline: Khoanh dòng điều kiện, mũi tên nhỏ vào suffix locale


### Where you can set add-ons

`add-on-pricing/where-you-can-set-add-ons.md`

**109. `addon-two-levels`**

* Where: App admin → builder
* Must show: Bên trái: option Text với field Price ở Add-on Settings. Bên phải: option Checkbox với cột Price trong bảng option values
* Outline: Khoanh 2 chỗ đặt giá


### Add price directly

`add-on-pricing/add-price-directly.md`

**110. `addon-add-price-tab`**

* Where: App admin → builder → dialog Add-on Configuration
* Must show: Tab "Add price" đang chọn, có banner giải thích và ô Price
* Outline: Khoanh tab Add price và ô giá


### Use an existing product

`add-on-pricing/use-an-existing-product.md`

**111. `addon-existing-product`**

* Where: App admin → builder → dialog Add-on Configuration
* Must show: Tab "Use existing product": danh sách sản phẩm có search, đã chọn 1 sản phẩm và đang hiện danh sách variant
* Outline: Khoanh danh sách variant


### Automatically generate a product

`add-on-pricing/auto-generate-a-product.md`

**112. `addon-auto-generate`**

* Where: App admin → builder → dialog Add-on Configuration
* Must show: Tab "Automatically generate product": banner, Product title và Variant title readonly, ô Price
* Outline: Khoanh ô Price và 2 field readonly


### Advanced add-on modes

`add-on-pricing/advanced-add-on-modes.md`

**113. `addon-advanced-modes`**

* Where: App admin → builder → option có Price → Advanced Settings
* Must show: Dropdown "Advanced settings" đang mở với đủ các mode và help text
* Outline: Khoanh dropdown


### Merge main product and add-ons

`add-on-pricing/merge-as-bundle.md`

**114. `addon-merge-setting`**

* Where: App admin → Settings → Add-on price
* Must show: Switch "Merge Main product & Add-on products"
* Outline: Khoanh switch


### Add-on price display settings

`add-on-pricing/price-display-settings.md`

**115. `addon-price-settings`**

* Where: App admin → Settings → Add-on price
* Must show: Toàn bộ các setting của tab
* Outline: Không khoanh


### Overview

`personalizer/README.md`

**116. `pp-storefront-hero`**

* Where: Storefront → trang sản phẩm có personalizer
* Must show: Ảnh sản phẩm với text khách nhập được vẽ lên, cạnh là field nhập
* Outline: Khoanh vùng preview trên ảnh sản phẩm


### Set the preview background

`personalizer/set-the-background.md`

**117. `pp-background-panel`**

* Where: App admin → builder → preview → Change background
* Must show: Panel với nhóm Background (Product image/Custom image) và Apply to (4 lựa chọn)
* Outline: Khoanh 2 nhóm lựa chọn


### Enable personalizer on an option

`personalizer/enable-on-an-option.md`

**118. `pp-enable-tab`**

* Where: App admin → builder → option Text → tab Personalizer Settings
* Must show: Switch "Enable personalize" đã bật, các nhóm setting hiện ra bên dưới
* Outline: Khoanh switch


### Text layers

`personalizer/text-layers.md`

**119. `pp-text-layer-settings`**

* Where: App admin → builder → option Text → Personalizer Settings
* Must show: Nhóm setting Text color, Font size, Font style, Font family
* Outline: Khoanh nhóm này


### Fonts

`personalizer/fonts.md`

**120. `pp-font-family`**

* Where: App admin → builder → option Text → Personalizer Settings
* Must show: Font family với 3 lựa chọn Default/Google/Custom và picker font đang mở
* Outline: Khoanh Font family và picker


### Text effects

`personalizer/effects.md`

**121. `pp-effects`**

* Where: App admin → builder → option Text → Personalizer Settings
* Must show: Custom Effect với 5 lựa chọn dạng image button
* Outline: Khoanh nhóm Custom Effect


### Position, size, and rotation

`personalizer/position-size-rotation.md`

**122. `pp-position-settings`**

* Where: App admin → builder → option có personalizer
* Must show: Nhóm X-Axis, Y-Axis, Opacity, Rotation dạng slider
* Outline: Khoanh nhóm này


### Curve and auto-fit width

`personalizer/curve-and-auto-fit.md`

**123. `pp-curve`**

* Where: App admin → builder → option Text → Personalizer Settings
* Must show: Slider Curve và preview text đang uốn theo cung trên ảnh sản phẩm
* Outline: Khoanh slider Curve và text uốn trong preview


### Clip area

`personalizer/clip-area.md`

**124. `pp-clip-area`**

* Where: App admin → builder → option có personalizer
* Must show: Nhóm setting clip area + preview hiện vùng clip có viền
* Outline: Khoanh vùng clip trong preview


### Image layers

`personalizer/image-layers.md`

**125. `pp-image-layer`**

* Where: App admin → builder → option File upload → Personalizer Settings
* Must show: Image shape picker và Background mode với 5 lựa chọn
* Outline: Khoanh 2 setting


### Customer controls

`personalizer/customer-controls.md`

**126. `pp-customer-controls`**

* Where: App admin → builder → option có personalizer
* Must show: Nhóm "Allow customers to" với 3 checkbox
* Outline: Khoanh nhóm này


### Designs in cart and orders

`personalizer/cart-and-orders.md`

**127. `pp-cart-preview`**

* Where: Storefront → trang cart
* Must show: Line item có option details và link "Preview Your Design", modal preview đã mở
* Outline: Khoanh link và modal


### Personalized templates

`personalizer/personalized-templates.md`

**128. `pp-templates-tab`**

* Where: App admin → Templates → tab Personalized Templates
* Must show: Grid các template có ảnh xem trước và nút Use template
* Outline: Không khoanh


### Overview

`templates/README.md`

**129. `tpl-tabs`**

* Where: App admin → Templates
* Must show: 3 tab với badge số lượng, grid template có ảnh xem trước
* Outline: Khoanh hàng 3 tab


### Custom templates

`templates/custom-templates.md`

**130. `tpl-custom-list`**

* Where: App admin → Templates → tab Custom Templates
* Must show: Bảng danh sách template với cột ID, Name, Option elements, Date created, Actions
* Outline: Không khoanh


### App admin language

`translations/app-admin-language.md`

**131. `trans-admin-language`**

* Where: App admin → Dashboard
* Must show: Popover chọn ngôn ngữ đang mở với danh sách các ngôn ngữ kèm cờ
* Outline: Khoanh nút chọn ngôn ngữ


### Translate option content

`translations/translate-option-content.md`

**132. `trans-builder-switcher`**

* Where: App admin → builder
* Must show: Language switcher ở header đang mở với danh sách ngôn ngữ storefront
* Outline: Khoanh language switcher


### Translate widget text

`translations/translate-widget-text.md`

**133. `trans-widget-text`**

* Where: App admin → Settings → Translations
* Must show: 4 nhóm text với các field, nút Add language
* Outline: Khoanh nút Add language


### Widget placement

`storefront/widget-placement.md`

**134. `store-widget-placement`**

* Where: App admin → Settings → General → Widget Settings
* Must show: Dropdown Widget placement đang mở với 8 lựa chọn chia nhóm Default và Custom
* Outline: Khoanh dropdown


### Match your theme style

`storefront/match-your-theme-style.md`

**135. `store-match-theme`**

* Where: App admin → Settings → Design → Theme style
* Must show: Switch Match theme style và tip banner có link View supported themes
* Outline: Khoanh switch


### Borders and typography

`storefront/borders-and-typography.md`

**136. `store-borders-typography`**

* Where: App admin → Settings → Design
* Must show: Nhóm Border (3 family với size/radius) và nhóm Typography (4 style)
* Outline: Khoanh 2 nhóm


### Widget behavior

`storefront/widget-behavior.md`

**137. `store-widget-behavior`**

* Where: App admin → Settings → General → Widget Settings
* Must show: Alignment, Show tooltip, Display selected value, Limit widget height
* Outline: Khoanh nhóm 4 setting


### Quickview and other pages

`storefront/quickview-and-other-pages.md`

**138. `store-other-pages`**

* Where: App admin → Settings → General
* Must show: Nhóm Collection page và Other pages với các switch
* Outline: Khoanh 2 nhóm


### Cart page

`storefront/cart-page.md`

**139. `store-cart-settings`**

* Where: App admin → Settings → General → Cart page
* Must show: 3 setting: hide quantity/remove, Edit Options, Personalize preview mode
* Outline: Khoanh nhóm Cart page


### Show options on orders

`storefront/show-options-on-orders.md`

**140. `store-order-details`**

* Where: Shopify admin → 1 order có option
* Must show: Line item với danh sách option properties bên dưới
* Outline: Khoanh phần properties


### Overview

`automations/README.md`

**141. `auto-templates`**

* Where: App admin → Automations → Workflow templates
* Must show: 3 thẻ workflow với icon và mô tả
* Outline: Không khoanh


### Email notification

`automations/email-notification.md`

**142. `auto-email-tabs`**

* Where: App admin → Automations → workflow Email notification
* Must show: 3 tab Preview / Edit code / Configure, tab Preview đang mở
* Outline: Khoanh hàng 3 tab


### Update order notes

`automations/update-order-notes.md`

**143. `auto-order-notes`**

* Where: App admin → Automations → workflow Order notes update
* Must show: Editor Content (HTML), checkbox Keep existing order notes, nút Test và Revert to default
* Outline: Khoanh editor và checkbox


### Update order tags

`automations/update-order-tags.md`

**144. `auto-order-tags`**

* Where: App admin → Automations → workflow Order tags update
* Must show: Dropdown Type với 2 mode, và field Tag name hoặc Option element
* Outline: Khoanh dropdown Type


### Set up and use options in POS

`pos/set-up-and-use.md`

**145. `pos-sales-channel`**

* Where: App admin → builder → popover Sales channels
* Must show: Point of Sale đang được bật
* Outline: Khoanh dòng Point of Sale

**146. `pos-cart-items`**

* Where: Shopify POS → app
* Must show: Danh sách line item trong cart, 1 item đang được chọn
* Outline: Khoanh item đang chọn


### Overview

`settings/README.md`

**147. `settings-tabs`**

* Where: App admin → Settings
* Must show: 3 tab Settings / Translations / Theme Setup và 3 section trong tab Settings
* Outline: Khoanh hàng 3 tab


### Theme setup

`settings/theme-setup.md`

**148. `settings-theme-setup`**

* Where: App admin → Settings → Theme Setup
* Must show: Dropdown theme, badge App embed, nút Go to Theme Editor
* Outline: Khoanh badge và nút


### Custom fonts

`settings/custom-fonts.md`

**149. `settings-custom-fonts`**

* Where: App admin → Settings → General → Custom fonts
* Must show: Khu vực upload font với Font name và Font file, danh sách font đã upload
* Outline: Khoanh khu vực upload


### Overview

`plans/README.md`

**150. `plan-pricing-page`**

* Where: App admin → Pricing
* Must show: Các plan card, switch Monthly/Yearly, plan hiện tại được đánh dấu
* Outline: Khoanh switch Monthly/Yearly

## Optional shots

Nice to have. The pages read correctly without them.

* `concept-flow-diagram` — concepts/how-the-app-works.md — Sơ đồ 5 bước: builder → storefront → cart → checkout
* `help-chat-bubble` — help/contact-support.md — Chat bubble ở góc dưới phải
