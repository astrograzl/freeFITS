freeFITS
========

Modify license information in FITS header.


Overview
--------
`freeFITS.py` is a simple script written in Python language designed to change [FITS](http://en.wikipedia.org/wiki/FITS) file header. It can display, modify, add and delete license information stored in it.

To store license information is used three non-standard keywords:

* `LICENSE` -- name of the license
* `LICVER` -- version of the license
* `LICURL` -- URL of the license's text


Requirements
------------
Runtime requirement is a Python interpreter with version >= 3.0. Aditional requirement is [PyFITS](http://www.stsci.edu/institute/software_hardware/pyfits), which may be downloaded from [Python Packaing Index](http://pypi.python.org/pypi/pyfits). Note that PyFITS itself depend on [NumPy](http://www.numpy.org/).



Installation
------------
There is no need to install `freeFITS.py`. Just place it somewhere and run. Or you may move it to the user or the system bin/ directory specified in your `$PATH` environment variable.


Usage
-----
To obtain information about usage run as `freeFITS.py -h` and you get this listing

    usage: freeFITS.py [-h] [-l] [-i] [-a ADD] [-d] fitsfile

    positional arguments:
      fitsfile           name of FITS file

    optional arguments:
      -h, --help         show this help message and exit
      -l, --list         list available licenses
      -i, --info         show license information in FITS file
      -a ADD, --add ADD  add license information to FITS file
      -d, --delete       delete license information from FITS file

To list available licenses run as `freeFITS.py -l /dev/null`. The identifier at first position in listing

    cc_by: CC BY 3.0 (http://creativecommons.org/licenses/by/3.0/)
    cc_by_nc_nd: CC BY-NC-ND 3.0 (http://creativecommons.org/licenses/by-nc-nd/3.0/)
    cc_by_nc_sa: CC BY-NC-SA 3.0 (http://creativecommons.org/licenses/by-nc-sa/3.0/)
    cc_by_nd: CC BY-ND 3.0 (http://creativecommons.org/licenses/by-nd/3.0/)
    cc_by_nc: CC BY-NC 3.0 (http://creativecommons.org/licenses/by-nc/3.0/)
    cc0: CC0 1.0 (http://creativecommons.org/publicdomain/zero/1.0/)
    pdm: Public Domain Mark 1.0 (http://creativecommons.org/publicdomain/mark/1.0/)
    cc_by_sa: CC BY-SA 3.0 (http://creativecommons.org/licenses/by-sa/3.0/)

is used to identify the license you would like to add to your FITS file.

To mark your FITS file as *Public Domain* just run `freeFITS.py -a pdm fitsfile.fits`.


Licenses
--------
By default are available licenses listed on the **Creative Commons** [site](http://creativecommons.org/licenses/). Please feel free to extend the list of available licenses according to your needs.


Copyright
---------
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
