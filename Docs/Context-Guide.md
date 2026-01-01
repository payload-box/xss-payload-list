# XSS Context Guide

Understanding the context where your input is reflected is crucial for successful XSS exploitation.

## 1. HTML Context

Input is placed directly into the HTML body.
**Example:** `<div>USER_INPUT</div>`
**Payload:** `<script>alert(1)</script>`
**Why?** You need to introduce a new HTML tag to execute code.

## 2. Attribute Context

Input is placed inside an HTML attribute.
**Example:** `<input value="USER_INPUT">`
**Payload:** `"><script>alert(1)</script>`
**Why?** You need to break out of the attribute string (`"`) and the tag (`>`) to start a new script tag.
**Alternative:** `" onmouseover=alert(1) autofocus="` (Uses event handler without breaking the tag).

## 3. JavaScript Context

Input is placed inside a `<script>` block.
**Example:** `<script>var x = 'USER_INPUT';</script>`
**Payload:** `'; alert(1); //`
**Why?** You need to terminate the existing string (`'`) and the statement (`;`), then execute your code. The `//` comments out the rest of the line.

## 4. URL Context

Input is placed inside an `href` or `src` attribute.
**Example:** `<a href="USER_INPUT">Click</a>`
**Payload:** `javascript:alert(1)`
**Why?** The browser executes the `javascript:` pseudo-protocol.

## Filter Evasion Tips

- **HTML Entities:** `<` becomes `&lt;` (Browser decodes entities in attributes).
- **URL Encoding:** `%3C` becomes `<` (Backend might decode).
- **Case Sensitivity:** `<ScRiPt>` might bypass case-sensitive regex.
