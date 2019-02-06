Python environments
===================
You can create Anaconda environments using
```DOS
conda env create -f test/SparseSC_27.yml
conda env create -f test/SparseSC_35.yml
```

Building docs
=============
Required python packages: `sphinx`, `recommonmark`, `sphinx-markdown-tables`
Index HTML file is at `docs/build/html/index.html`

Testing
=======
We use the built-in `unittest`. Can run from makefile using the `tests` target or you can run python directly from the repo root using the following types of commands:

```python
python -m unittest test/test_fit.py #file (only Python >=3.5)
python -m unittest test.test_fit #module
python -m unittest test.test_fit.TestFit #class
python -m unittest test.test_fit.TestFit.test_retrospective #function
```

Release Process
===============
* Ensure the makefile target `check`  (which does pylint, tests, doc building, and packaging) runs clean
* If new version, check that it's been updated in `SparseSC/__init__.py`
* Updated `Changelog.md`
* Tag/Release in version control