# gridmix2 data generation for hadoop 2.x

This repository contains just data generation script from hadoop 1.2.1 gridmix2
benchmark, updated to work with hadoop 2.x.

Why? I needed this to be able to reproduce a bug. It's likely not usefull for
any other purpose.

## origin

Original source files resides in `src/benchmarks/gridmix2` directory, I reused
just two files:

 * `gridmix-env-2`
 * `generateGridmix2data.sh`

And incorporate changes for this script to work with hadoop 2.x releases.

## details

Since the data generation script uses `randomtextwriter` from hadoop examples
jar file, it's possible to run it on hadoop 2.x as well with minor
modifications (rename of properties and output class names - see git log for
the details).

The gridmix2 test itself depends on hadoop 1.x source, so it's not compatible
with new releases. It's already declared as deprecated and so removed from
hadoop 2.x source tree. Moreover I didn't need to run it to reproduce bug, so 
I didn't bother to look at it.
