---
tags:
    - cli
    - python
    - template
    - ix.io
    - pastebin
---

# A rich CLI template for pastebin CLI tools

ix is a command line interface for [ix.io](https://ix.io), a pastebin service.

I tried to make this CLI as "reusable" as possible, so that you can clone this repository and use it as a template for your own pastebin CLI tool.

## How to use this template

1. Clone this repository
2. Rename the `ix_cli` directory to the name of your pastebin service
3. Replace the variable `PROVIDER_URL` in `ix_cli/utils.py` with the URL of your pastebin service (e.g. `https://paste.example.com`)
4. Replace the name of the app in `pyproject.toml` with the name of your pastebin service in both the `name` and `[tool.poetry.scripts]` sections
5. Install [poetry](https://python-poetry.org) and run `poetry install` to install the dependencies
6. Run a basic command to make sure everything works: `<new-app-name> s "Hello, world!"`
7. Edit the README to your liking
8. Commit your changes and push them to your repository
9. Publish your app to [PyPI](https://pypi.org) using `poetry build` and `poetry publish`

## Installation

### Using pip

```bash
pip install ix-cli
```

### Cloning the repository

```bash
git clone https://github.com/arnos-stuff/ix.git
```

## Basic usage

### As a Python module

```python
from ix_cli import uploadFromFile, uploadFromStdin, download, getHistory

# Upload from stdin
url = uploadFromStdin("Hello, world!")
print(url)

# Upload from file
url = uploadFromFile("README.md")
print(url)

# Download
data = download(url)
print(data)
```

### As a CLI tool

Using ix is simple. Just pipe some text into it:

```bash
echo "Hello, world!" | ix s
```

This will print the URL of the paste to stdout. You can also use ix to upload files:

```bash
ix f README.md
```

This CLI has an extra feature: it stores the past 100 URLs in a local cache. You can use this to quickly access your pastes:

```bash
ix h
```

This will print a list of your pastes, with the most recent at the top. You also have the option to limit the number of pastes shown:

```bash
ix h -n 3
```

This will print the 3 most recent pastes.

## Getting the data back

You can use ix to retrieve the data from a paste by using the `g` command:

```bash
ix g https://ix.io/1QZp
```

or simply

```bash
ix g 1QZp
```

This will print the contents of the paste to stdout.

For more details, go to [the detailed commands page](cli.md)

## License

This project is licensed under the MIT License - see the [LICENSE](../LICENSE) file for details
