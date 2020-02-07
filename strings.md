---
stringArr:
  - One
  - two
  - Three
  - four
  - Five
  - six
---

{%- include "_header.njk" %}

### `stringArr` <small>(array of mixed case strings)</small>

```json
{{ stringArr | dump(2) | safe }}
```

#### Default string sort (ascending, case-insensitive)

```njk
{% raw %}{{ stringArr | sort }}{% endraw %} =
    {{ stringArr | sort | dump | replace(",", ", ") | safe }}
```

#### Descending string sort

```njk
{% raw %}{{ stringArr | sort(true) }}{% endraw %} =
    {{ stringArr | sort(true) | dump | replace(",", ", ") | safe }}
```

#### Ascending, case-insensitive string sort

```njk
{% raw %}{{ stringArr | sort(false, false) }}{% endraw %} =
    {{ stringArr | sort(false, false) | dump | replace(",", ", ") | safe }}
```

#### Ascending, case-sensitive string sort

```njk
{% raw %}{{ stringArr | sort(false, true) }}{% endraw %} =
    {{ stringArr | sort(false, true) | dump | replace(",", ", ") | safe }}
```

#### Descending, case-sensitive string sort

```njk
{% raw %}{{ stringArr | sort(true, true) }}{% endraw %} =
    {{ stringArr | sort(true, true) | dump | replace(",", ", ") | safe }}
```
