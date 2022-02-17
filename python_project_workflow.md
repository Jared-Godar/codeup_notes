# Make A Virtual Environment

- In either Python or conda
  - See `virtual_env.md` notes.

# Create a separate directory for tests

- Look into `pytest`

- For files to access things in that folder, you can pretend `text` directory is a package.
- In the directory, create a file called __init__.py (completely empty file)

### if you have something like this:
`another_directory/__init__.py`
`another_directory/module.py`

### you can import the code in module.py as
`from another_directory import module`
or
`import another_directory.module`

Basically, `__init__.py` is used to mark directories as Python package directories


# Create separate logical directories

images
helper modules
etc

