
# this repository is [forked](https://github.com/rodrigogiraoserrao/python-black-check), i only changed the black version.
i did this for personal use but anyone can use this, all credits go to the original creator

# python-black-check
A customisable GitHub action to check the style of Python code with [black](https://github.com/psf/black).

# Inputs
You can use inputs to alter how `black` will check your code.

## Path (optional)
This tells `black` where to look for files to check.

**Default**: `.`, i.e. looks for files in the whole repository.

## Line-length (optional)
This tells `black` how long each line of Python code can be.

**Default**: `81`, which is _different_ from `black`'s default of `88`.

## Include (optional)
This tells `black` which files we should verify the format of.

**Default**: `\.pyi?$`, which matches `black`'s default value.

## Exclude (optional)
This tells `black` which files we should ignore.

**Default**: `/(\.direnv|\.eggs|\.git|\.hg|\.mypy_cache|\.nox|\.tox|\.venv|\.svn|_build|buck-out|build|dist)/`, which matches `black`'s default value.

# Example usage
Include this in your `.github/workflows/main.yaml`:

```yaml
uses: extreme4all/python-black-check-v22.3.0@master
```
or, if you want to override any of the defaults,

```yaml
uses: extreme4all/python-black-check-v22.3.0@master
with:
  line-length: '81'
  path: '.'
  include: 'apps'
  exclude: '(/*.html|/*.mo|/*.po|/*.png|/*.rst)'
```
