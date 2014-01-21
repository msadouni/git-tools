# Git Tools

Various Git tools.

## Installation

Clone or download a tarball, then:

    $ make install

If you get a permission error, try with `sudo`:

    $ sudo make install

## Uninstallation

    $ make uninstall

## Commands

- `git export`

## git-export

Creates a `tgz` archive of the current branch or tag.

It uses either the SHA (when on a branch) or the tag name to identify the export file.

    # on a branch
    $ git export
    Exporting develop at a6f0720
    Saved to my-project-a6f0720b6acdc98f338ef017410c69e17869afc0.tgz ( 2M)

    # on a tag
    $ git export
    Exporting tags/1.0.0^0 at 6d57c3d
    Saved to my-project-1.0.0.tgz ( 2M)

The archive will expand to a directory named `$project-$sha` or `$project-$tag`. To change the folder name, use the `-p` option :

    # change the parent folder name
    $ git export -p my-project
    Exporting develop at a6f0720
    Saved to my-project-a6f0720b6acdc98f338ef017410c69e17869afc0.tgz ( 2M)
    $ tar -xzf my-project-a6f0720b6acdc98f338ef017410c69e17869afc0.tgz
    $ ls
    my-project
