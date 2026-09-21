# phi

**Build apps for iOS, Android, macOS and the web from one codebase: the app in Rust, its
screens in HTML and CSS.**

phi draws its own pixels on iOS, Android and macOS — no web view, no JavaScript engine, no
garbage collector in the app — and the same screens become the browser's own DOM in a
browser build. One `App` contract, one platform host each.

## Status

🚧 **Pre-release.** phi runs a shipping-grade app today; the crate isn't published yet and
its API will change before 1.0.

## Principles

- **Markup is the contract.** Screens are HTML and CSS, bound to Rust view models with a
  small Mustache subset; app logic stays in Rust.
- **One app, every platform.** A platform supplies a window, input and a clock — the app
  code does not change.
- **Small by default.** Few dependencies, and optional features (full international text,
  localisation) stay optional.
- **Measured, not assumed.** Layout is checked against a real browser, and performance is
  tracked on old, low-end phones as well as new hardware.
