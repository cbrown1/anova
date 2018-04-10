# _anova.py

The anova module from the pyvttbl package, which appears to be unmaintained.

The module in the pyvttble package has some issues having to do with age. This version attempts to fix them, with a little bit of code cleanup and other minor refactoring.

Since there is no usable anova module in pystatsmodels, or anywhere else for that matter, this module is crucial for those who need it in python.

## Installing

1. Install pyvttbl from pip. 
2. Download this module.
3. Copy it into the pyvttbl dir in site-packages, overwriting the original anova module.

Something like:

```bash
pip install pyvttbl
git clone https://github.com/cbrown1/anova.git
cd anova
cp _anova.py /usr/lib/python2.7/site-packages/pyvttbl/stats
```

## Usage
```python
>>> import pyvttbl
>>> df = pyvttbl.DataFrame()
>>> df.read_tbl('test.csv')    
>>> aov = df.anova('PC', sub='Subjects', wfactors=['within_var1', 'within_var2'])
>>> print(aov)
```

