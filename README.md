##Requirements:
* Craftcoin
* Python
* Twisted
* python-argparse (for Python <=2.6)
* litecoin_scrypt (included)


##Setup:
####Linux:

    sudo apt-get install python-zope.interface python-twisted python-twisted-web

If Python version <= 2.6 :

    sudo apt-get install python-argparse

    cd litecoin_scrypt
    sudo python setup.py install

####Windows:
* Install MinGW: http://www.mingw.org/wiki/Getting_Started
* Install Python 2.7: http://www.python.org/getit/
* Install Twisted: http://twistedmatrix.com/trac/wiki/Downloads
* Install Zope.Interface: http://pypi.python.org/pypi/zope.interface/3.8.0
* Install python win32 api: http://sourceforge.net/projects/pywin32/files/pywin32/Build%20218/
* Install python win32 api wmi wrapper: https://pypi.python.org/pypi/WMI/#downloads
* Unzip the files into C:\Python27\Lib\site-packages
* In MinGW bash:

    cd litecoin_scrypt
    C:\Python27\python.exe setup.py build --compile=mingw32 install

If you run into an error with unrecognized command line option '-mno-cygwin', see this:
http://stackoverflow.com/questions/6034390/compiling-with-cython-and-mingw-produces-gcc-error-unrecognized-command-line-o


##Running P2Pool:
To use P2Pool for Craftcoin, you must be running your own local craftcoind. For standard
configurations, using P2Pool should be as simple as:

    python run_p2pool.py --net craftcoin

Then run your miner program, connecting to 127.0.0.1 on port 8830 with any
username and password.

If you are behind a NAT, you should enable TCP port forwarding on your
router. Forward port 23336 to the host running P2Pool.

Run for additional options.

    python run_p2pool.py --help


###Donations towards further development:
forrestv: 1HNeqi3pJRNvXybNX4FKzZgYJsdTSqJTbk (Original P2Pool creator)

###Official wiki:
https://en.bitcoin.it/wiki/P2Pool

###Alternate web front end:
* https://github.com/hardcpp/P2PoolExtendedFrontEnd
