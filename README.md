spackle
=======

A local package manager for non-root linux users.  

Bringing easy package compiling, dependency resolution, and uninstallation to the masses.

## The problem

All modern package managers (like apt-get, yum, pacman, dpkg, rpm, nixos) believe that only root users should install packages.  But sometimes normal users need to install stuff too.

Most sysadmins would rather be shot than give you root access.  So the normal user who wants to install some software typically has to compile their own software from source.  This usually means downloading a source tarball and running

    tar zxvf foo-source.tar.gz
    cd foo-source
    ./configure --prefix=$HOME/local
    make
    make install
    
If you're lucky, everything worked and you have a binary you can run at `$HOME/local/bin/foo`.  The more likely scenario is that there was an error somewhere: you need to pass some flag to `configure` or there are some dependencies that you need to install first.  Pray that you don't need to patch the source or uninstall.


## The solution

Luckily, there are devoted people who build packages for linux distributions.  You can either extract their binary package  (e.g. .deb, .rpm, .pkg.tar.xz) into your home folder (or somewhere you have write priveleges) or you can use their build scripts to compile the package from source and change the installation location.

They've already listed the dependencies and created the build scripts with proper flags.


## The inspiration

Inspired by ArchLinux's user repository of PKGBUILD scripts, python's pip and virtualenv tools, ruby's rubygems and rvm tools.

