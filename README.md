gmrender-resurrect-debian
=========================

Files for creating a Debian package file from the CVS sources for gmrender-resurrect

See http://www.coraline.org/non-fiction/raspi-upnp-renderer for further details.

To build, in the base directory:

    ./unpack-source
    cd gmrender-resurrect
    debbuild -uc -us

Note that the unpack script copies files from /debian into the build directory
(gmrender-resurrect).  The build directory is not kept in CVS, and files in that
directory should not be edited directly.  Rerun *unpack-source* after changing
files in /debian.  If files in /debian have been deleted, it will be necessary
to run *clean-repo* then *unpack-source*.

To clean up, ensure you have commited any changes to your local
repository, and then, again in the base directory:

    ./clean-repo

