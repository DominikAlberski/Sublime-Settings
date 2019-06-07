# Sublime-Settings

Steps for new ST3 installation:

- remove the User folder of the fresh install
- clone your backup (only the User folder)
- install Package Control
- restart Sublime Text

Along with the Package Control files that are mentioned in the .gitignore file of that Git repo, you should also ignore oscrypto-ca-bundle.crt (if you use or will use Mac OS), as that’s the Mac version of the Package Control merged ca files. That’s less of an issue if you never use a Mac, but I’m just mentioning that here for completeness.

Also note that it doesn’t cover any packages that you manually installed yourself or any files in installed packages that you have expressly overridden, because such files would be stored outside of the User directory. So if you’re doing either of those two things, you have a bit more work to do. I would suggest not doing either of things if at all possible, though.

As a (vaguely contrived) example, if you were developing something for Python 3 using Sublime on a computer where the python interpreter is named python3 instead of python, you might override the default Python.sublime-build file to modify how it’s running the python interpreter.

Such an override would be stored in Python\Python.sublime-build and not User\Python.sublime-build, so it doesn’t get captured by this process.

versionning external package wich are on the Package manager is redondant.

It’s redundant, but another reason not to do it (if you use Sublime on multiple operating systems as I do) is that it’s possible for a package to have some os-specific file or content setup in it. When PackageControl installs such a package it installs the version for your current operating system, which would break that package under a different OS.
