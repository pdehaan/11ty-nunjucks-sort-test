---
numberArr:
  - 1
  - 11
  - 2
  - 5
  - 79
  - 227
---

{%- include "_header.njk" %}

### `numberArr` <small>(array of numbers)</small>

```json
{{ numberArr | dump(2) }}
```

#### Default number sort (ascending)
```njk
{% raw %}{{ numberArr | sort }}{% endraw %} = {{ numberArr | sort | dump }}
```

#### Descending number sort

```njk
{% raw %}{{ numberArr | sort(true) }}{% endraw %} = {{ numberArr | sort(true) | dump }}
```
