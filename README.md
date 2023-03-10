# A rich CLI for ix.io

ix is a command line interface for [ix.io](https://ix.io), a pastebin service.

## Installation

### Using pip

```bash
pip install ix
```

### Cloning the repository

```bash
git clone https://github.com/arnos-stuff/ix.git
```

## Basic usage

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

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
