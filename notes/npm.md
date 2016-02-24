N.P.M. - Tricks and tips
(nope not node package manager... because it now manages more than just node packages.)

How to check what package to use:

  1. Check the number of downloads the package has had, lots is a good sign but not the be all and end all.
  2. Check when it was last updated, recent and regular is good.
  3. Check the version number, higher will be more developed and should have less bugs.
  (note: the version number, consisting of 3 digits, may also let you know about compatibility issues.)
  4. See if the test results are shown and if they pass.
  5. Click the link to the git repository and see how many stars, watches, forks and contributors are on there.

Go to the terminal and type:

  $ npm

this will give you a list of possible npm commands.

Installing packages

  $ npm install -h

will give you a list of options on how you can customize the install for the different packages.

The command for a standard install for one package will be something like:

  $ npm install <package name>

Some packages may depend on specific versions of other programs, rule of thumb, try installing and check the error message if it doesn't
work. The error messages are super useful.

An example of a package that may not install properly for you first time is 'bcrypt' as it uses python2 (if you have python installed but are still getting this error you might have the more recent python 3.. installed). On install you can specify what version you want it to use with:

  $ npm install bcrypt --python=python2

Global installs

To install a package globally, in other words to make it accessible to more projects use the flag -g

eg. $ npm install <package name> -g

You may get an error message if the folder permissions for npm are limited. These permissions can be adjusted using:

$ npm config get prefix
(to find the directory that you have the npm file stored in)

$sudo chown -R
$(whoami)
$(path from npm config get prefix)
