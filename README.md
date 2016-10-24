# Python CLI  structure

## Why?

This repo serves as a good reference point for a simple and basic CLI
structure. This can either be consumed visually or cloned in which case you
should change `pycli` to whatever your CLI name will be.

## Steps

1.  Change setup tools to name the tool (like below, from pycli to pytoolname)

```
 from setuptools import setup
 
 setup(
-    name = 'pycli',
+    name = 'pytoolname',
     version = '0.1.0',
     packages = ['pycli'],
     entry_points = {
         'console_scripts': [
-            'pycli = pycli.__main__:main'
+            'pytoolname = pycli.__main__:main'
         ]
     })
```

2.  Update pycli/classmodule.py or pycli/funcmodule.py to reflect the functionality of the tool.

3.  Update main.py to remove calls to classmodule or funcmodule if not needed.

4.  `pip install .` to install the tool.  `pip uninstall -y <pytoolname>` to uninstall.

## Links

[The easy (and nice) way to do CLI apps in Python – Medium](https://medium.com/@trstringer/the-easy-and-nice-way-to-do-cli-apps-in-python-5d9964dc950d#.ns1l1a9b5)
