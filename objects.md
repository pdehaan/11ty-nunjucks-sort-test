---
objectArr:
  - name: One
    date: 2020-01-04
    int: 1
  - name: two
    date: 2017-03-21
    int: 11
  - name: Three
    date: 2014-04-14
    int: 2
  - name: four
    date: 2020-02-07
    int: 5
  - name: Five
    date: 1999-03-29
    int: 79
  - name: six
    date: 2004-09-09
    int: 227
---

{%- include "_header.njk" %}

### `objectArr` <small>(array of objects)</small>

```json
{{ objectArr | dump(2) | replace(",", ", ") | safe }}
```

#### Sorted object <small>(returns same order as unsorted object, when no params passed)</small>

```njk
{% raw %}{{ objectArr | sort }}{% endraw %} =
{{ objectArr | sort | dump | replace("}," ,"},\n ") | indent(4, true) | safe }}
```

#### Ascending, case-insensitive sort using the String "name" property

```njk
{% raw %}{{ objectArr | sort(false, false, "name") }}{% endraw %} =
{{ objectArr | sort(false, false, "name") | dump | replace("}," ,"},\n ") | indent(4, true) | safe }}
```

#### Descending, case-insensitive sort using the String "name" property

```
{% raw %}{{ objectArr | sort(true, false, "name") }}{% endraw %} =
{{ objectArr | sort(true, false, "name") | dump | replace("}," ,"},\n ") | indent(4, true) | safe }}
```

#### Descending, case-sensitive sort using the String "name" property

```njk
{% raw %}{{ objectArr | sort(true, true, "name") }}{% endraw %} =
{{ objectArr | sort(true, true, "name") | dump | replace("}," ,"},\n ") | indent(4, true) | safe }}
```

#### Ascending, case-insensitive sort using the Date "date" property

```njk
{% raw %}{{ objectArr | sort(false, false, "date") }}{% endraw %} =
{{ objectArr | sort(false, false, "date") | dump | replace("}," ,"},\n ") | indent(4, true) | safe }}
```

#### Descending, case-insensitive sort using the Date "date" property

```njk
{% raw %}{{ objectArr | sort(true, false, "date") }}{% endraw %} =
{{ objectArr | sort(true, false, "date") | dump | replace("}," ,"},\n ") | indent(4, true) | safe }}
```

#### Ascending, case-insensitive sort using the Number "int" property

```njk
{% raw %}{{ objectArr | sort(false, false, "int") }}{% endraw %} =
{{ objectArr | sort(false, false, "int") | dump | replace("}," ,"},\n ") | indent(4, true) | safe }}
```

#### Descending, case-insensitive sort using the Number "int" property

```njk
{% raw %}{{ objectArr | sort(true, false, "int") }}{% endraw %} =
{{ objectArr | sort(true, false, "int") | dump | replace("}," ,"},\n ") | indent(4, true) | safe }}
```
