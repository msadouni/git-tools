# Git Tools

Various Git tools.

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
