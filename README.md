# Sinsy

This is our unofficial git mirror of the source found at the [official site](http://sinsy.sourceforge.net/).

## Installation

    git clone git@github.com:zyamusic/sinsy.git

Now change into the sinsy directory and get its submodules

    cd sinsy
    git submodule init
    git submodule update

Now go into hts-engine and pre-build it:

    cd hts-engine/src
    ./configure
    make

You can install it too if you wish with "sudo make install". But the following instructions will work whether or not you install it. Now change into the sinsy directory and build sinsy:

    cd ../../src
    ./configure --with-hts-engine-header-path=`realpath ../hts-engine/src/include` --with-hts-engine-library-path=`realpath ../hts-engine/src/lib`
    make

If you wish, you may now install sinsy with:

    sudo make install
