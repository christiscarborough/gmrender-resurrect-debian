gmrender-resurrect-debian
=========================

Files for creating a Debian package file from the CVS sources for gmrender-resurrect

See http://www.coraline.org/non-fiction/raspi-upnp-renderer for further details.

To build, in the base directory:

    tar xvzf gmrender-resurrect_<version>.git.orig.tar.gz
    cd gmrender-resurrect
    debbuild -uc -us

To clean up, ensure you have commited any changees to your local
repository, and then, again in the base directory:

    ./clean-repo
