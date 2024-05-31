# Typst-div Extension For Quarto

Adds a filter to pick up divs with a class that starts with `.typst_`. The contents of the div is passed to a function that matches the suffix of the class, e.g. `.typst_page` passes the content to the `page()` function.  Attributes to the div are passed as named arguments.

## Installing

```bash
quarto add cwickham/typst-div
```

This will install the extension under the `_extensions` subdirectory.
If you're using version control, you will want to check in this directory.

## Using

````
::: {.typst_page fill='rgb("#39729E")'}

This content will be passed to `page()` setting the `fill` argument:

```typst
#page(fill: rgb("#39729E"))[
  {{ Div contents }}
]
```

::: 
````

## Example

Minimal example: [Source](example.qmd), [PDF](example.pdf)

