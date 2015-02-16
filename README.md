Pairfq
======

Sync paired-end FASTA/Q files and keep singleton reads

[![Build Status](https://travis-ci.org/sestaton/Pairfq.png?branch=master)](https://travis-ci.org/sestaton/Pairfq)

**BASIC USAGE**

There is a standalone script in the 'scripts' directory that has no dependencies and will work with Perl version 5.6 or newer. This script has fewer features (mainly, it lacks the indexing function for working with large data) than the main application but it may be useful in an environment where installing libraries is not convenient. Obtaining this version can be done with curl:

    curl -L git.io/pairfq_lite > pairfq_lite

You can then make the script executable and check the usage:

    chmod +x pairfq_lite
    ./pairfq_lite -h

It is recommended that users follow the directions below to install and use Pairfq. Note that the commands below require Perl version 5.10. To obtain a full explanation of all commands, please see the Support and Documenation section below.
 
**INSTALLATION**

The following command will install Pairfq (note that this requires [git](http://git-scm.com/)):

    curl -L cpanmin.us | perl - git://github.com/sestaton/Pairfq.git

Alternatively, download the latest [release](https://github.com/sestaton/Pairfq/releases) and run the following command in the top directory:

    perl Makefile.PL

If any Perl dependencies are listed after running this command, install them through the CPAN shell or any method you like (see the [installing dependencies](https://github.com/sestaton/Pairfq/wiki/Installing-dependencies) page for instructions). Then build and install the package.

    perl Makefile.PL
    make
    make test
    make install

The last command is optional, you can put the program in a custom location or use it in place.

**TYPICAL USAGE CASES**

See the [Pairfq wiki](https://github.com/sestaton/Pairfq/wiki) for examples with each method.

**SUPPORT AND DOCUMENTATION**

After installation, you can find documentation for Pairfq with the `perldoc` command.

    perldoc pairfq

The documentation can also be accessed by specifying the manual option with `pairfq -m` or `pairfq --man`. The `pairfq` program will also print a diagnostic help message when executed with no arguments. In addition, there is extensive documentation on the Pairfq [wiki](https://github.com/sestaton/Pairfq/wiki) online.

**ISSUES**

Report any issues at the Pairfq issue tracker: https://github.com/sestaton/Pairfq/issues

Be aware that Pairfq will not work for every data set given the wide range of FASTA/Q formats. Feel free to fork the project and modify the code to your needs, or submit code changes if you find any bugs. 
 
**ATTRIBUTION**

This project uses the [readfq](https://github.com/lh3/readfq) library written by Heng Li. The readfq code has been modified for error handling and to parse the comment line in the Casava header.

**LICENSE**

The MIT License should included with the project. If not, it can be found at: http://opensource.org/licenses/mit-license.php

Copyright (C) 2013-2015 S. Evan Staton
