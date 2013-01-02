freeFITS
========

Úprava licenčních informací v hlavičce FITS snímku.


Přehled
-------
`freeFITS.py` je jednoduchý a jednoúčelový skript napsaný v jazyce Python, sloužící k úpravě hlavičky [FITS](http://en.wikipedia.org/wiki/FITS) snímku. Dokáže zobrazit, upravit, přidat a odstranit informace o licenci v ní uložené.

K uložení informací o licenci se používají tři **nestandardní** klíčová slova:

* `LICENSE` -- označení licence
* `LICVER` -- číslo verze licence
* `LICURL` -- URL směřující k textu licence


Požadavky
---------
Pro běh programu je zapotřebí interpret jazyka Python ve verzi >= 3.0. Dodatečným požadavkem je modul [PyFITS](http://www.stsci.edu/institute/software_hardware/pyfits), který lze stáhnout z [Python Packaing Index](http://pypi.python.org/pypi/pyfits). Berte na vědomí, že samotný modul PyFITS závisí dále na modulu [NumPy](http://www.numpy.org/).


Instalace
---------
Program není třeba speciálně instalovat. Stačí jej uložit kamkoliv na pevný disk Vašeho počítače a spustit. Případně jej můžete umístit do některého ze systémového nebo uživatelského adresáře bin/ uvedeného v proměnné prostředí `$PATH`.


Použití
-------
Pro získání nápovědy spusťte program s parametrem `--help`, načež získáte následující výpis:

    usage: freeFITS.py [-h] [-l] [-i] [-a ADD] [-d] fitsfile

    positional arguments:
      fitsfile           name of FITS file

    optional arguments:
      -h, --help         show this help message and exit
      -l, --list         list available licenses
      -i, --info         show license information in FITS file
      -a ADD, --add ADD  add license information to FITS file
      -d, --delete       delete license information from FITS file

Pro výpis dostupných licencí spusťte program jako `freeFITS.py --list /dev/null`. (Soubor /dev/null zde supluje FITS snímek, který je povinným parametrem i v případě, že jeho uvedení není nijak opodstatněné.) Identifikátor na první pozici ve výpisu

    cc_by: CC BY 3.0 (http://creativecommons.org/licenses/by/3.0/)
    cc_by_nc_nd: CC BY-NC-ND 3.0 (http://creativecommons.org/licenses/by-nc-nd/3.0/)
    cc_by_nc_sa: CC BY-NC-SA 3.0 (http://creativecommons.org/licenses/by-nc-sa/3.0/)
    cc_by_nd: CC BY-ND 3.0 (http://creativecommons.org/licenses/by-nd/3.0/)
    cc_by_nc: CC BY-NC 3.0 (http://creativecommons.org/licenses/by-nc/3.0/)
    cc0: CC0 1.0 (http://creativecommons.org/publicdomain/zero/1.0/)
    pdm: Public Domain Mark 1.0 (http://creativecommons.org/publicdomain/mark/1.0/)
    cc_by_sa: CC BY-SA 3.0 (http://creativecommons.org/licenses/by-sa/3.0/)

slouží k určení licence, kterou byste rádi přidali do hlavičky Vašeho FITS snímku.

Pro označení vašeho FITS snímku jako *Public Domain* prostě spusťte program jako `freeFITS.py --add pdm fitsfile.fits`.


Licence
-------
Ve výchozím stavu jsou dostupné licence uvedená na [stránce](http://creativecommons.org/licenses/) **Creative Commons**. Prosím ciťte se svobodní při rozšíření seznamu dostupných licencí podle Vašich vlastních potřeb.


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
