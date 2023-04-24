---
tags:
    - ix
    - pastebin
    - cli
    - python
    - upload
    - temphost
    - hosting

---

# Command line tool`ix`

A CLI for interacting with the ix.io pastebin service.

**Usage**:

```console
$ ix [OPTIONS] COMMAND [ARGS]...
```

**Options**:

* `--install-completion`: Install completion for the current shell.
* `--show-completion`: Show completion for the current shell, to copy it or customize the installation.
* `--help`: Show this message and exit.

**Commands**:

* `f`: Upload a file to ix.io
* `file`
* `g`: Download a file from ix.io
* `get`
* `h`: Show the history of uploaded files.
* `hist`
* `rmh`: Clear the history of uploaded files.
* `s`: Upload stdin to ix.io
* `stdin`
* `x`: Export the history of uploaded files.
* `xl`: Export last line of the history of...

## Command `ix f`

Upload a file to ix.io

**Usage**:

```console
$ ix f [OPTIONS] FILEPATH
```

**Arguments**:

* `FILEPATH`: The path to the file to upload.  [required]

**Options**:

* `-d, --debug`: Enable debug mode.
* `--help`: Show this message and exit.

## Command `ix file`

**Usage**:

```console
$ ix file [OPTIONS] FILEPATH
```

**Arguments**:

* `FILEPATH`: The path to the file to upload.  [required]

**Options**:

* `-d, --debug`: Enable debug mode.
* `--help`: Show this message and exit.

## Command `ix g`

Download a file from ix.io

**Usage**:

```console
$ ix g [OPTIONS] PARAM
```

**Arguments**:

* `PARAM`: The URL/ID/Name of the file to download.  [required]

**Options**:

* `-d, --debug`: Enable debug mode.
* `--help`: Show this message and exit.

## Command `ix get`

**Usage**:

```console
$ ix get [OPTIONS] PARAM
```

**Arguments**:

* `PARAM`: The URL/ID/Name of the file to download.  [required]

**Options**:

* `-d, --debug`: Enable debug mode.
* `--help`: Show this message and exit.

## Command `ix h`

Show the history of uploaded files.

**Usage**:

```console
$ ix h [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.

## Command `ix hist`

**Usage**:

```console
$ ix hist [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.

## Command `ix rmh`

Clear the history of uploaded files.

**Usage**:

```console
$ ix rmh [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.

## Command `ix s`

Upload stdin to ix.io

**Usage**:

```console
$ ix s [OPTIONS] [PARAM]
```

**Arguments**:

* `[PARAM]`: sdtin input to upload to ix.io, defaults to sys.argv

**Options**:

* `-d, --debug`: Enable debug mode.
* `--help`: Show this message and exit.

## Command `ix stdin`

**Usage**:

```console
$ ix stdin [OPTIONS] [PARAM]
```

**Arguments**:

* `[PARAM]`: sdtin input to upload to ix.io, defaults to sys.argv

**Options**:

* `-d, --debug`: Enable debug mode.
* `--help`: Show this message and exit.

## Command `ix x`

Export the history of uploaded files.

**Usage**:

```console
$ ix x [OPTIONS]
```

**Options**:

* `-n, --num-lines INTEGER`: Number of past lines to export.
* `--help`: Show this message and exit.

## Command `ix xl`

Export last line of the history of uploaded files.

**Usage**:

```console
$ ix xl [OPTIONS]
```

**Options**:

* `--help`: Show this message and exit.
