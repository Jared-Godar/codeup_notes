# What?

- Virtual environments are separate project spaces. 

# So What?

- They are optimal for individual projects or tools for reproducibility and to resolve issues from multiple libraries needing different versions of dependencies.

# Now what?

- Can make virtual envireonments through either Python or Conda

---

## Python VE

1. `python3 -m venv {name}`
2. `source {name}/bin/activate`
3. `deactivate`

Once you have installed all the packages that your project needs, you can run:

>`pip freeze > requirements.txt`

Other people using your program will then run:

>`pip install -r requirements.txt`