SXDM
=======


SXDM is a library for analyzing Scanning X-Ray Diffraction Micriscopy data
for materials science, chemistry and similar fields. The major focus is on
Scanning Micriscopy frames collected at multiple incident angles. One can
import, retrieve, and analyze 26 - ID - C datasets all from a Python format.


Motivation & Features
---------------------

- Importing and analysis of scanning x-ray diffraction microscopy framesets
- Analysis of scanning x-ray diffraction microscopy (centroids & region of interest)


Installation
------------

- Make a clone of the SXDM project onto your machine
- Possibly create a virtual environment
- Run the requirements.txt file


Virtual Environment & Jupyter Setup
------------

- cd to directory you would like to keep the virtual environment
- run `python3 -m venv projectname` in the terminal projectname can be anything the User would like it to be
- run `source projectname/bin/activate`
- run `pip3 install ipykernel`
- run `ipython kernel install --user --name=projectname`
- run `pip3 install -r requirements.txt` for the sxdm repository
- in jupyter notebook/lab run `import sys` and `sys.path.append("/path/to/module/")`

- if you are running on a Mac then:
- run in jupyter notebook/lab `import sys`
- run in jupyter notebook/lab `sys.path.append('/Users/usr/virtual_environment/lib/python3.7/site-packages/')`

Usage
-----

Please see the SXDM Wiki for more details


License
-------

This project is released under the `GNU General Public License version 3`_.

This program is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
General Public License for more details.

.. _GNU General Public License version 3: https://www.gnu.org/licenses/gpl-3.0.en.html