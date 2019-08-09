# Python 3.7.4 embed(Portable)

source: https://www.python.org/downloads/windows [(zip)](https://www.python.org/ftp/python/3.7.4/python-3.7.4-embed-amd64.zip)

use portable python 3.7.4 on windows and install all packages offline

step1. download [(zip)](https://www.python.org/ftp/python/3.7.4/python-3.7.4-embed-amd64.zip) and unzip file

step2. delete python37._pth(we had already deleted in this repo)

step3. download [get-pip.py](<https://bootstrap.pypa.io/get-pip.py>)

step4. wheels of [pip](https://files.pythonhosted.org/packages/62/ca/94d32a6516ed197a491d17d46595ce58a83cbb2fca280414e57cd86b84dc/pip-19.2.1-py2.py3-none-any.whl), [wheel](https://files.pythonhosted.org/packages/bb/10/44230dd6bf3563b8f227dbf344c908d412ad2ff48066476672f3a72e174e/wheel-0.33.4-py2.py3-none-any.whl) and [setuptools](https://files.pythonhosted.org/packages/ec/51/f45cea425fd5cb0b0380f5b0f048ebc1da5b417e48d304838c02d6288a1e/setuptools-41.0.1-py2.py3-none-any.whl) from [pypi](<https://pypi.org/>) (download in package/pip_install in this repo)

step5. command: "\python.exe .\get-pip.py --no-index --find-links=.\package\pip_install" to install pip, it will create Scripts and Lib files

step6. download other packages which you need (download tensorflow and keras in package/other in this repo)

step6. write what you want to install into requirements.txt

step7. command:" .\Scripts\pip3.7.exe install --no-index --find-links=./package/other -r requirements.txt"

* if you are online, skip step4~7, just use two command on terminal
  * .\python.exe  .\get-pip.py
  * .\Scripts\pip3.7.exe install (packages you want)
* you can add .\python.exe and .\Scripts to path
* you can get all packages data on an online computer and copy data to other offline, for example: 
  * command: "pip install tensorflow"
  * command: "pip install keras"
  * command: "pip list" #ckeck packages
  * command: "pip freeze > requirements.txt"
  * command: "pip install --download any_path_you_want/packages -r requirements.txt"
  * copy packages file and requirements.txt 