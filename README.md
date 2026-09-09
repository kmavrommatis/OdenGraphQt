# OdenGraphQt

OdenGraphQt is a fork of jchanvfx [NodeGraphQt](https://github.com/jchanvfx/NodeGraphQt), a node graph UI framework
for `PySide6` that can be implemented and re-purposed into applications.

## Changes from NodeGraphQt

- **PySide6** compatibility (I have not tested PyQt6) courtesy of **jowr** and **rajkundu**
- **PyQt6** compatibility: every module imports Qt through `qtpy`, so the Qt binding is no
  longer a hard dependency of this package and is chosen by the host application (see Install)
- Alternative port accept/reject connection
- Partial type hints for IDE type checker (e.g. PyCharm)
- Minor code reformat, tweaks and comments for code readability

## Install

For now, please install as editable package. I'll be publishing to PyPI after I'm done with a few rounds of sanity
testing.

I highly advise using virtual environment when developing any tools/applications.

Assuming you're on Windows and using command prompt. Git Bash user please change the path to Unix style.

1. Clone this repository (e.g. `D:\Repo\OdenGraphQt`)
2. Navigate to the Python app code you wish to integrate OdenGraphQt (e.g. `D:\Tools\MyAwesomePipelineTool`)
3. Run `pip install -e D:\Repo\OdenGraphQt`
4. ???
5. ~~Profit~~ You can start importing `OdenGraphQt` module in your Python app code.

### Qt binding

Qt is accessed exclusively through [`qtpy`](https://github.com/spyder-ide/qtpy), so this package does
not depend on a specific binding. Supply one yourself, or pull it in with an extra:

- `pip install -e D:\Repo\OdenGraphQt[pyside6]`
- `pip install -e D:\Repo\OdenGraphQt[pyqt6]`

If both are installed, `qtpy` picks one by its own precedence rules; set `QT_API=pyqt6` (or
`pyside6`) to choose explicitly.

## Documentation

Please refer to jchanvfx excellent documentation at https://chantonic.com/NodeGraphQt/api/index.html

I'll update this section in the near future after re-configuring the `sphinx_doc_build.yml`.

See the [basic_example.py](/examples/basic_example.py) script to get started
or [accept_reject_example.py](/examples/accept_reject_example.py) for the alternative port accept/reject connection
logic.

## Why Oden? なぜおでんなのか？

Oden is delicious. おでんはおいしいです。

Real answer: I need to have a different namespace and Node can be rearranged as Oden by shifting N to the back.
