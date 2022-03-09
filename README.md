# map-machine-cookbook
“Why errors was given about map-machine?”

---

Here is a unofficial guidebook about how to point out where go weong when configure a map-machine environment.

[map-machine](https://github.com/enzet/map-machine) is a OpenStreetMap based image generator library that @enzet maintancing.

This repository is my diary about meet with error and error. Sometimes when I'm lazy, I will write in Chinese.

---

Catalog:

+ 1. Installing
  + 1.1 `python setup.py egg_info Check the logs for full command output.`
  + 1.2 `Could not find a version that satisfies the requirement Shapely>=1.7.1`

+ 2. Using

---

### 1.1

Q:

```
ERROR: Command errored out with exit status 1:
     command: /usr/bin/python3 -c 'import sys, setuptools, tokenize; sys.argv[0] = '"'"'/tmp/pip-req-build-dx27l95w/setup.py'"'"'; __file__='"'"'/tmp/pip-req-build-dx27l95w/setup.py'"'"';f=getattr(tokenize, '"'"'open'"'"', open)(__file__);code=f.read().replace('"'"'\r\n'"'"', '"'"'\n'"'"');f.close();exec(compile(code, __file__, '"'"'exec'"'"'))' egg_info --egg-base /tmp/pip-req-build-dx27l95w/pip-egg-info
         cwd: /tmp/pip-req-build-dx27l95w/
    Complete output (7 lines):
    Traceback (most recent call last):
      File "<string>", line 1, in <module>
      File "/tmp/pip-req-build-dx27l95w/setup.py", line 7, in <module>
        from map_machine import (
      File "/tmp/pip-req-build-dx27l95w/map_machine/__init__.py", line 16, in <module>
        REQUIREMENTS: list[str] = [
    TypeError: 'type' object is not subscriptable
    ----------------------------------------
ERROR: Command errored out with exit status 1: python setup.py egg_info Check the logs for full command output.
```

A:

Do you using **exactly Python 3.9** ? Maybe you are using python version lower than **3.9**.

This problem had been reported in https://github.com/enzet/map-machine/issues/111

The solve way is change your python version, this may differ from your operation system.

### 1.2

Q:

```
ERROR: Command errored out with exit status 1:
   command: 'C:\Users\azumu\AppData\Local\Programs\Python\Python310\python.exe' -c 'import io, os, sys, setuptools, tokenize; sys.argv[0] = '"'"'C:\\Users\\azumu\\AppData\\Local\\Temp\\pip-install-fp9m3brr\\shapely_d5d15fe21b2f42cf8d975b48d63f4eb0\\setup.py'"'"'; __file__='"'"'C:\\Users\\azumu\\AppData\\Local\\Temp\\pip-install-fp9m3brr\\shapely_d5d15fe21b2f42cf8d975b48d63f4eb0\\setup.py'"'"';f = getattr(tokenize, '"'"'open'"'"', open)(__file__) if os.path.exists(__file__) else io.StringIO('"'"'from setuptools import setup; setup()'"'"');code = f.read().replace('"'"'\r\n'"'"', '"'"'\n'"'"');f.close();exec(compile(code, __file__, '"'"'exec'"'"'))' egg_info --egg-base 'C:\Users\azumu\AppData\Local\Temp\pip-pip-egg-info-hyqn0qow'
       cwd: C:\Users\azumu\AppData\Local\Temp\pip-install-fp9m3brr\shapely_d5d15fe21b2f42cf8d975b48d63f4eb0\
  Complete output (9 lines):
  Traceback (most recent call last):
    File "<string>", line 1, in <module>
    File "C:\Users\azumu\AppData\Local\Temp\pip-install-fp9m3brr\shapely_d5d15fe21b2f42cf8d975b48d63f4eb0\setup.py", line 74, in <module>
      from shapely._buildcfg import geos_version_string, geos_version, \
    File "C:\Users\azumu\AppData\Local\Temp\pip-install-fp9m3brr\shapely_d5d15fe21b2f42cf8d975b48d63f4eb0\shapely\_buildcfg.py", line 204, in <module>
      lgeos = CDLL("geos_c.dll")
    File "C:\Users\azumu\AppData\Local\Programs\Python\Python310\lib\ctypes\__init__.py", line 374, in __init__
      self._handle = _dlopen(self._name, mode)
  FileNotFoundError: Could not find module 'geos_c.dll' (or one of its dependencies). Try using the full path with constructor syntax.
  ----------------------------------------

ERROR: Could not find a version that satisfies the requirement Shapely>=1.7.1 (from map-machine) (from versions: 1.0a7, 1.0b1, 1.0b2, 1.0b3, 1.0b4, 1.0rc1, 1.0rc2, 1.0, 1.0.1, 1.0.2, 1.0.3, 1.0.4, 1.0.5, 1.0.6, 1.0.7, 1.0.11, 1.0.12, 1.0.13, 1.0.14, 1.0.15, 1.2b1, 1.2b2, 1.2b3, 1.2b4, 1.2b5, 1.2b6, 1.2b7, 1.2rc1, 1.2rc2, 1.2, 1.2.1, 1.2.2, 1.2.3, 1.2.4, 1.2.5, 1.2.6, 1.2.7, 1.2.8, 1.2.9, 1.2.10, 1.2.12, 1.2.13, 1.2.14, 1.2.15, 1.2.16, 1.2.17, 1.2.18, 1.2.19, 1.3.0, 1.3.1, 1.3.2, 1.3.3, 1.4.0, 1.4.1, 1.4.2, 1.4.3, 1.4.4, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.5.12, 1.5.13, 1.5.14, 1.5.15, 1.5.16, 1.5.17, 1.6a1, 1.6a2, 1.6b1, 1.6b2, 1.6b3, 1.6b4, 1.6b5, 1.6.0, 1.6.1, 1.6.2, 1.6.2.post1, 1.6.3, 1.6.4, 1.6.4.post1, 1.6.4.post2, 1.7a1, 1.7a2, 1.7a3, 1.7b1, 1.7.0, 1.7.1, 1.8a1, 1.8a2, 1.8a3, 1.8rc1, 1.8rc2, 1.8.0)
ERROR: No matching distribution found for Shapely>=1.7.1
```
A:

Do you using **exactly Python 3.9** ? Maybe you are using python version Higher than **3.9**.

This problem had been reported in https://github.com/enzet/map-machine/issues/101

The solve way is change your python version, this may differ from your operation system.

### 2.1

Q: 

"cannot load library 'libcairo.so.2': error 0x7e"

A: 

https://stackoverflow.com/questions/28211418/python-oserror-cannot-load-library-libcairo-so-2
