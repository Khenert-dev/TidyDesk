# Third-party components

TidyDesk uses Python (Python Software Foundation license), PySide6/Shiboken6 and Qt (LGPLv3 or other applicable Qt license). The portable folder keeps Qt dynamically linked. Do not remove the bundled libraries or their license notices.

Python license: https://docs.python.org/3/license.html

Qt/PySide licensing and source: https://doc.qt.io/qtforpython-6/licenses.html

Qt source and corresponding versions: https://download.qt.io/official_releases/QtForPython/

PyInstaller is used to build the executable and provides a bootloader exception permitting distribution of bundled applications: https://pyinstaller.org/en/stable/license.html

## Library source and replacement rights

This release uses the unmodified PySide6 Essentials / Shiboken6 **6.12.0** wheels and Qt **6.12.0**. TidyDesk application source is private; that does not remove your rights to the third-party libraries or their corresponding source.

- [Qt 6.12.0 complete source archive](https://download.qt.io/official_releases/qt/6.12/6.12.0/single/qt-everywhere-src-6.12.0.tar.xz)
- [PySide6 / Shiboken6 6.12.0 source archive](https://download.qt.io/official_releases/QtForPython/pyside6/PySide6-6.12.0-src/pyside-setup-everywhere-src-6.12.0.tar.xz)
- [Python 3.13.15 source and release information](https://www.python.org/downloads/release/python-31315/)

These are source downloads for the third-party components, not the TidyDesk application. Their source archives include upstream build scripts and license notices. The source links must remain clearly available beside distributed releases; maintainers must preserve corresponding-source access for the libraries they distribute.

Qt/PySide libraries remain dynamically linked and replaceable. Exit TidyDesk first, then replace compatible libraries in `_internal/PySide6` and, where relevant, `_internal/shiboken6`. Keep matching Qt/PySide/Shiboken versions and the Windows x64 ABI; preserve the folder layout and plugins. Upstream source/build guidance is at https://doc.qt.io/qtforpython-6/building_from_source/index.html . No signing or integrity restriction is added to prevent library replacement. Application terms allow reverse engineering for debugging modifications to LGPL-covered libraries and do not restrict rights under the LGPL.

Copies of LGPLv3, GPLv3, and Python notices are included under `_internal/licenses` in the installed application. Additional third-party notices in the upstream source and library distribution remain applicable. This notice does not claim that Qt endorses TidyDesk.
