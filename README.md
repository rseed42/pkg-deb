pkg-deb
=======

Debian packages for projects.

## How to use

1. Make sure that the source is ready for shipping (git tag it).

2. Make a compressed file with the following naming convention (The name of
the directory doesn't matter):

>project_name_0.x.orig.tar.gz

3. Move the compressed file to the root of pkg-deb.

4. Copy the source code to pkg-deb/project_name/. The source files must match 
the ones in the compressed file (i.e. if you make a change in the source, you
have to start again).

5. Update debian/changelog (version 0.x must match the compressed file version).

6. Build the package

   a) If not signing it:

>dpkg-buildpackage -us -uc -tc