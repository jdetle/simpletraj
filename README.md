

Simple coordinate-only trajectory reader based on code from GROMACS, MDAnalysis and VMD.


Installation
============


Some libraries need to be installed. First, make sure you have the python development files installed, e.g.

    sudo apt-get install python-dev python-numpy


Then install the NetCDF libraries

    sudo apt-get install libhdf5-serial-dev libnetcdf-dev
    sudo pip install netCDF4


In case you get "ValueError: did not find HDF5 headers" try:

    sudo su
    find / -name "libhdf5*.so*"
    # use what the above 'find' suggests to set 'HDF5_DIR'
    export HDF5_DIR=/usr/lib/i386-linux-gnu/hdf5/serial/
    pip install netCDF4

Finally install simpletraj itself

    sudo python setup.py develop