# ColSON

This extension provides syntax highlighting for ColSON, a minimalist language that can be converted into JSON.

## Syntax

| ColSON         | JSON             |
| -------------- | ---------------- |
| `::`           | `[`              |
| `:::`          | `{`              |
| `True`         | `true`           |
| `False`        | `false`          |
| `None`         | `null`           |
| `123.5e-2`     | `123.5e-2`       |
| `key :: value` | `"key": "value"` |
| `key :::`      | `"key": {}`      |
| `key ::`       | `"key": []`      |
| `:: comment`   | _skipped_        |
| `\\`           | `""`             |
| `\False\`      | `"False"`        |
| `~snippet`     | `"~snippet"`     |

- Consistent indentation is important.
- Empty lines are optional.
- Snippets start with `~` and may contain only letters, numbers, `-` and `_`.
- Snippets are treated as strings but allow you to see suggestions.

## Example

### ColSON file

![ColSON example file](https://raw.githubusercontent.com/shushtain/colson-vscode/refs/heads/main/example.png)

### JSON file

```json
{
  "meta": {
    "language": "en",
    "title": ""
  },
  "body": [
    {
      "type": "h1",
      "content": "Double space:  "
    },
    {
      "type": "ul",
      "content": ["first", "~my_snippet", 123.05, true, "False"]
    }
  ],
  "footer": {
    "path": "/",
    "script": "script.js"
  }
}
```
