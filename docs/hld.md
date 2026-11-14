# EazyEatz: High-Level Design

A responsive food-ordering website: browse specialities, popular dishes, gallery and reviews, then place an order through a simple form. Live at [eazy-eatz-pink.vercel.app](https://eazy-eatz-pink.vercel.app). For code-level detail see the [Low-Level Design](lld.md).

## 1. Context

```mermaid
flowchart LR
  V([Customer]) -->|browser| Site[index.html + style.css + script.js]
  Site -->|order form, mailto| Mail([Email client])
  Host[Vercel] --> Site
```

## 2. Page sections

```mermaid
flowchart TB
  Header[Header + menu bar] --> Home
  Home --> Speciality
  Speciality --> Popular[Popular dishes]
  Popular --> Gallery
  Gallery --> Review[Reviews]
  Review --> Order[Order form]
  Order --> Footer
```

## 3. Tech

| Item | Choice |
|---|---|
| Stack | HTML, CSS, vanilla JavaScript |
| Ordering | Form with `action="mailto:…"` (opens the visitor's email app) |
| Hosting | Vercel |
