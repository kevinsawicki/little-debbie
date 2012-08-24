# little-debbie

Simple application using automake, autoconf, and debhelper to generate
a `.deb` file that installs a Hello World executable.

## Building the .deb

```
$ aclocal
$ autoheader
$ automake --add-missing
$ autoconf
$ ./configure
$ sudo debian/rules binary
```

## Installing the .deb

Assuming the created `.deb` file is named `little-debbie_1.0_amd64.deb`:

```
$ sudo dpkg -i little-debbie_1.0_amd64.deb
$ debbie
> Hello World!
```
