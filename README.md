# JabberDock
JabberDock provides a mechanism to dock two protein STID maps together in conjunction with the POW engine
and BioBox

Note that it requires BioBOx as a means to generate the STID maps, and POW to run the optimisation.

This version of JabberDock ships with a version of BioBOx intended to allow it to work.
See below for a brief introduction to installation / where to find POW.

auto_scripts
Command line features are provided in the auto_scripts folder.
* Help for each one for be provided by typing the command follows by -h, e.g. dock.py -h
* The commands should be accessible in your PYTHONPATH
* More information on each command is provided in the accompanying manual

methods
* In here you will find all the python scripts called by the various commands in auto_scripts
* Each one has documentation written out, this can be read either directly in the file, or via the manual
* There are a few additional commands provided for users which are not used by the commands in auto_scripts...
* For example, the create_pqr_dat in data, which can convert an rtp file into a readable dat pqr file to create STID maps

## INSTALLATION AND REQUIREMENTS ##

JabberDock requires python 2.7 and the following packages (and their associated packages):
* numpy
* biobox
* cython
* scipy
* scikit-image
* subprocess

JabberDock requires the following software to be installed to run:
* gromacs 5.x
* VMD 1.9.x
* POWer

Both biobox and POWer are available with this module.

Install JabberDock with: 'python setup.py install'

After downloading from github, this JabberDock folder might be called JabberDock-master. Ensure it's called JabberDock for the imports to work:
mv JabberDock-master JabberDock

Please read the full installation instructions in the manual.

## Biobox installation ##
Shipped with this version of JabberDock is a heavily stripped version of biobox containing the functions JabberDock requires.
Please move the biobox folder into whatever directory you like (e.g. your home), just make sure it's in your pythonpath
There is a readme file in the biobox folder containing instructions on requirements and installation instructions.

This is an unpubished PDB manipulation module, and therefore is unavaliable elsewhere. We are aiming to publish the full module at some point in the future.

## POW installation ##
The original version of POW can be found on the EPFL website:
https://www.epfl.ch/labs/lbm/resources/

However this is an outdated version, the current version of JabberDock requires the updated version of POW (POW_v2) shipped with JabberDock.

To install, simply move the POW_v2 folder into your home (or other) directory - where JabberDock and biobox should now be located.

You will also need to install dill. To do this, type:
pip install dill
On your command line. For the mpi4py installation, we would recommend mpi4py 3.0.0:
pip install mpi4py==3.0.0

## Usage ##

Please see the manual in the home directory for more details on how to use JabberDock. Email the author if you have any questions.

When using JabberDock in your work, please cite the following publication: https://pubs.acs.org/doi/10.1021/acs.jctc.9b00474

## Contact ##

This is a work in progress, and there are bound to be bugs. If you have any issues, please email the author at l.s.rudden@durham.ac.uk.
