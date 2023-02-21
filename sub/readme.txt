## sub/readme.txt

Make a symbolic link to this readme on localhost.

    ln -s readme.txt readme.md

Make a symbolic link in another sub directory.

    mkdir dup/ &&
    cd dup/ &&
    ln -s ../readme.txt readme.md

The latter will enable [another link](dup/readme.md)
to this readme itself, and the same content will be shown
via [another relative link](dup/).

If this were seen **formatted** without extra characters,
then symbolic link with some markup file extension works
like actual file!

Although, this seems limited to readme on web repository and
*might not* work with other files. Is it? Self-answer.

Hint: Path to the symbolic link is either ``sub/readme.md``
or ``sub/dup/readme.md``

Return to [higher directory](..)
