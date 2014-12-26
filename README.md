heroku-buildpack-octave-cedar14
======================================

Heroku buildpack for [Octave](https://www.gnu.org/software/octave/) that works on the new [Cedar 14](https://devcenter.heroku.com/articles/cedar) stack.

Note: the buildpack also installs the [GNU Compiler Collection](https://gcc.gnu.org/) because the default version that comes on a Heroku dyno does not include a Fortran compiler (which Octave requires).

## How to use
This buildpack can be used in conjunction with other supported language stacks on Heroku by using the [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) buildpack.
```
$ heroku config:add BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi.git
$ cat .buildpacks
https://github.com/heroku/heroku-buildpack-nodejs.git
https://github.com/wclark3/heroku-buildpack-octave-cedar14.git
```

## Octave Console
You can also run Octave in the console as follows:
```
$ heroku run octave
```

## License
MIT License. Copyright (c) 2014 Will Clark. See LICENSE for details.