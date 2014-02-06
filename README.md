pkg-deb
=======

Debian packages for projects.

## How to use

1. Make sure that the source is ready for shipping (git tag it).

2. Make a compressed file with the following naming convention:

>project_name-0.x.orig.tar.gz

3. Move the compressed file to the root of pkg-deb.

4. Copy the source code to pkg-deb/project_name/. The source files must match 
the ones in the compressed file (i.e. if you make a change in the source, you
have to start again).

5. Create a symbolic link pkg-deb/project_name/ -> pkg-deb/project_name-0.x

6. Change the version number in debian/changelog to 0.x, add info if necessary.

7. Build the package

   a) If not signing it:

>dpkg-buildpackage -us -uc -tc