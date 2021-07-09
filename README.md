# Lockfile platforms problem

Different scenarios to think through https://github.com/pantsbuild/pants/issues/12222, and how to solve it with the 
new lockfiles design in Pants 2.7.

`ansicolors` has a bdist wheel so works on foreign platforms. `future` only has an `sdist` and cannot
be built for foreign platforms.
