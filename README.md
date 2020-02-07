# 11ty-nunjucks-sort-test

Testing the Nunjucks sort filter in Eleventy for sorting arrays of <a href="numbers.md">numbers</a>, <a href="strings.md">strings</a>, and <a href="objects.md">objects</a>.</p>

## `{{ arr | sort(reverse=false, caseSens=false, attr) }}`

<p>Sort <code>arr</code> with JavaScript's <code>arr.sort</code> function.
  If <code>reverse</code> is <code>true</code>, result will be reversed.
  Sort is case-insensitive by default, but setting <code>caseSens</code> to <code>true</code> makes it case-sensitive.
  If <code>attr</code> is passed, will compare <code>attr</code> from each item.</p>
