packer
======
`packer` is a Bash wrapper for `pacman` and the
[Arch User Repository](https://aur.archlinux.org) (AUR).

Usage
-----
    usage: packer [option] [package] [package] [...]

        -S           - installs package
        -Sd[d]       - skips dependency version checks
        -Syu|-Su     - updates all packages, also takes -uu and -yy options
        -Ss|-Ssq     - searches for package
        -Si          - outputs info for package
        -G           - download and extract aur tarball only

        --quiet      - only output package name for searches
        --force      - bypass file conflict checks
        --ignore     - takes a comma-separated list of packages to ignore
        --noconfirm  - do not prompt for any confirmation
        --noedit     - do not prompt to edit files
        --quickcheck - check for updates and exit
        --aur        - include AUR actions
        --devel      - update devel packages during -Su
        --skipinteg  - when using makepkg, do not check md5s
        --preview    - edit pkgbuild before sourcing
        --help       - outputs this message

License
-------
This software is released under the terms of the **GPLv3 license**.
