
# Copy right
I am not the original author, i just increased the requirements because the original author didn't, the focus of this repo is primarily for my own.

[Original](https://github.com/piotrpawlaczek/python-blacken)

# python-blacken [new]

A customisable GitHub action to check the style of Python code with [black](https://github.com/psf/black).

Uses black version **22.1.0**

# Inputs
You can use inputs to alter how `black` will check your code.

## Path (optional)
This tells `black` where to look for files to check.

**Default**: `.`, i.e. looks for files in the whole repository.

## Line-length (optional)
This tells `black` how long each line of Python code can be.

## Sanity-check (optional)
If --fast given, skip temporary sanity checks. Options `[fast|safe]`. Default `fast`.

## Only-check (optional)
Only check the files instead of modify them. Options `[yes|no]`. Default `yes`.

# Example usage
Include this in your `.github/workflows/main.yaml`:

```yaml
uses: extreme4all/python-black-check-v22.3.0@master

```
or, if you want to override any of the defaults,

```yaml
uses: extreme4all/python-black-check-v22.3.0@master
with:
  line-length: '88'
  path: '.'
  sanity-check: 'safe'
  only-check: 'no'
```
