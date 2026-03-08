# thtml — VS Code Extension

Syntax highlighting, autocomplete, and type checking for `.thtml` template files.

## Features

- **Syntax highlighting** — TextMate grammar for `.thtml` files with embedded TypeScript and HTML
- **Autocomplete** — full IntelliSense inside `{{ }}` and `{% %}` expressions powered by the TypeScript language service
- **Hover docs** — type information on hover
- **Diagnostics** — real-time type errors and template syntax errors

## Template Syntax

```thtml
---
interface Context {
  name: string;
  items: string[];
}
---
<h1>Hello, {{ name }}!</h1>

{% if items.length > 0 %}
  <ul>
    {% for item of items %}
      <li>{{ item }}</li>
    {% endfor %}
  </ul>
{% endif %}

{# This is a comment #}
{{ !rawHtml }}  <!-- unescaped output -->
```

## Requirements

- VS Code `^1.85.0`
- The `@thtml/language-server` npm package is bundled — no separate install needed

## Extension Settings

| Setting | Default | Description |
|---------|---------|-------------|
| `thtml.languageServer.enabled` | `true` | Enable/disable the language server |
| `thtml.languageServer.trace` | `off` | LSP trace level: `off`, `messages`, `verbose` |
| `thtml.validate.enable` | `true` | Enable real-time validation |

## Commands

| Command | Description |
|---------|-------------|
| `thtml: Restart Language Server` | Restart the LSP server |
| `thtml: Show Output Channel` | Show language server logs |
| `thtml: Preview Template` | Preview rendered template (coming soon) |

## Related

- [`@thtml/core`](https://www.npmjs.com/package/@thtml/core) — template compiler and runtime
- [`@thtml/language-server`](https://www.npmjs.com/package/@thtml/language-server) — LSP server
- [GitHub](https://github.com/denislibs/thtml-vscode)