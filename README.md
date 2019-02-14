-------------------------------------------------------------------------------

This project is no longer maintained.

-------------------------------------------------------------------------------


_heroku-buildpack-submodule-example_
====================================

Example Heroku buildpack, showing how to reference _git_ submodules.


Usage
-----

```
$ mkdir fnord && cd fnord && git init
Initialized empty Git repository in /tmp/fnord/.git/

$ touch README && git add README && git commit -m "Fnord"
[master (root-commit) c9ac882] Fnord
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README

$ heroku create -b https://github.com/mietek/heroku-buildpack-submodule-example
Creating fnord-1975... done, stack is cedar-14
BUILDPACK_URL=https://github.com/mietek/heroku-buildpack-submodule-example
https://fnord-1975.herokuapp.com/ | git@heroku.com:fnord-1975.git
Git remote heroku added

$ git push heroku master
Initializing repository, done.
Counting objects: 3, done.
Writing objects: 100% (3/3), 215 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)

-----> Fetching custom git buildpack... done
-----> Example app detected
-----> Engaging submodule
Submodule 'heroku-buildpack-submodule-example-submodule' (https://github.com/mietek/heroku-buildpack-submodule-example-submodule.git) registered for path 'heroku-buildpack-submodule-example-submodule'
Cloning into 'heroku-buildpack-submodule-example-submodule'...
Submodule path 'heroku-buildpack-submodule-example-submodule': checked out 'e5b0b3cec18f7e991dec111c288f44cef4160f0c'
-----> Submodule engaged
-----> Discovering process types
       Procfile declares types -> (none)

-----> Compressing... done, 0K
-----> Launching... done, v4
       https://fnord-1975.herokuapp.com/ deployed to Heroku
```


About
-----

Made by [Miëtek Bak](https://mietek.io/).  Published under the BSD license.
