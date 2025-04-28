# fmake
A custom build utility, written in Python

# Setup

Firstly, this is *nix only, since compiling on Windows is...**rather difficult**

To make `fmake` executable, run\
`chmod +x fmake`\
If that doesn't work, uh...**sudo it**\
Then, to be able to run it, move it into your `/usr/local/bin` directory

# Config file

This repo comes with an example `make.fmake` file\
\
If you want to generate a new example config run `fmake example`.\
\
If you want to make a config file from scratch here's how to do that:\
\
`variable =/$ value(if applicable)`\
To set a variable to it's default value, write `variable $`.\
\
Here are the available variables
| Variable | Default | Possible values | about |
|----------|---------|-----------------|-------|
| cc | gcc | Any compiler | The compiler you want to use |
| src | main.c | Any .c file | The source C file |
| msg | true | true / false | Whether or not the "Done!" message is displayed after compilation |
| out | main | Any filename | The name of the executable file the compiler will produce |
| say | "Compiling done!" | Any string | The message that's printed after compilation |

# Making a project

If you want to set up a new C project you can run `fmake project` which creates an `src/` and a `build/` directory, alongside a preconfigured `make.fmake` file. The sourcetree should look something like this:

```
src/
src/main.c
build/
make.fmake
```

# Debugging

If you want to make sure all the variables in `make.fmake` are correctly declared you can run `fmake debug`. This should return something like this:\
```
CC:gcc
SRC:main.c
OUT:main
MSG:True
SAY:Compiling done!
```

# Version

Run `fmake --version`,`fmake -v`, or `fmake version` for the current version.

# Help

For more info run `fmake --help`, `fmake -?`, or `fmake -h`.
