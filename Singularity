Bootstrap: docker
From: ubuntu:16.04

%labels
MAINTAINER darachm

%post

    apt-get -y update
    apt-get -y install python python-dev cmake git g++
    
    cd /root
    git clone https://github.com/darachm/BarNone.git
    cd /root/BarNone

    python setup.py build
    python setup.py install
    python setup.py test
    # This one has an error, not sure why, testing on data without
    # this for now...

%test

    BarNone -h
