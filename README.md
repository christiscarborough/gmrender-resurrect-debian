gmrender-resurrect-debian
=========================

Files for creating a Debian package file from the CVS sources for gmrender-resurrect

See http://www.coraline.org/non-fiction/raspi-upnp-renderer for further details.

To build, make a new directory in a directory you have write permission in, enter
that directory, then clone the repository as follows:

git clone https://github.com/christiscarborough/gmrender-resurrect-debian/
mv gmrender-resurrect-_0.0.7.git.orig.tar.gz ..
tar xvzf ../gmrender gmrender-resurrect-_0.0.7.git.orig.tar.gz
mv gmrender-resurrect/* .
rmdir gmrender-resurrect
debuild -uc -us

To restore your directory to pristine freshness and you should run the following 
commands then move the tarball back into the directory before attempting a commit.

debclean
ls - 1 | grep -v ^debian$ | xargs rm
