# Quality Assurance

## Coding Style

Follow these standard conventions:

- [PEP 20 -- The Zen of Python](http://www.python.org/dev/peps/pep-0020/)
- [PEP 8 -- Style Guide for Python Code](http://www.python.org/dev/peps/pep-0008/)
- [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html)
- [Django coding style](https://docs.djangoproject.com/en/3.1/internals/contributing/writing-code/coding-style/)

With the following variations:

- **Line max length:** 100 characters.
- **Quotes:** Always use double quotes for strings _(as texts contain more often single than double quotes)_. Except if it requires escaping characters, then if there are only 1-2 escapes, use single quotes, else triple double quotes.
- **Format Strings:** Prefer `f"{var}"` over `"{}".format(var}`.
- **Regexes:** Use double quoted raw string literals (e.g. `r"[0-9]+"`).


## Documentation

The documentation is generated using [MkDocs](https://www.mkdocs.org/).


- Use smart quotes. Use `I’ll do “this”` not `don't do "that"`.


### Docstrings

The sources documentation is generated using [mkdocstrings](https://pawamoy.github.io/mkdocstrings/).

Follow these standard conventions:

- [PEP 257 -- Docstring Conventions](https://www.python.org/dev/peps/pep-0257/)
- [Google Python Style Guide](https://google.github.io/styleguide/pyguide.html#38-comments-and-docstrings)

With the following variations:

- Use triple double quotes.
- The first line is the summary line. It always starts on the same line as the quotes and ends with `.?!`.
- Single line:
  - Close the quotes on the same line.
- Multilines:
    - Leave a blank line after the summary line.
    - Start aligned with the `"""`.
- Module doc: Leave a blank line between the ending quotes and the beginning of the code.


## Editor

Configure the coding styles in [`/.editorconfig`](https://editorconfig.org/).


## Lint

@TODO


## Test

@TODO


## CI/CD

@TODO
