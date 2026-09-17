# Coupling
A project to explore the details of "[Balancing Coupling in Software Design][coupling:book]",
a book by [Vlad Khononov][coupling:author].

## Development setup

This repository uses [uv][uv] for Python installation, dependency management, and
running development tools.

Install uv by following the [official installation instructions][uv:install].
Then install Python 3.14 and the project dependencies:

```sh
uv python install 3.14
uv sync --dev
```

Install the pre-commit hooks after syncing the dependencies:

```sh
uv run pre-commit install
```

Run the checks locally with:

```sh
uv run pytest
uv run ruff check .
uv run ruff format --check .
uv run pyright
uv run pre-commit run --all-files
```

The pre-commit configuration runs formatting, linting, type checking, and the
test suite, so it covers more than tests alone.

The project uses a `src` layout for application code and a `tests` directory for
the test suite.

## Goal
The goal of this project is to acquire hands-on experience with the concepts from
[the book][coupling:book].
We intent to develop software and critique it through the lens of coupling.

Since the purpose is to explore, a lot of knowledge will not be in code.
So do not forget to checkout:

* [discussions][project:discussions]
* [issues][project:issues]
* [wiki][project:wiki]
* [projects][project:projects]

[coupling:author]: https://vladikk.com/page/about/
[coupling:book]: https://vladikk.com/page/books/
[project:discussions]: https://github.com/fifth-postulate/coupling/discussions
[project:issues]: https://github.com/fifth-postulate/coupling/issues
[project:projects]: https://github.com/fifth-postulate/coupling/projects
[project:wiki]: https://github.com/fifth-postulate/coupling/wiki
[uv]: https://docs.astral.sh/uv/
[uv:install]: https://docs.astral.sh/uv/getting-started/installation/
