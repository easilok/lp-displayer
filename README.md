# Displayer - Display output manage

## Introduction

*Displayer* is a personal display output manager that, provided a configuration, can automatically select the preferred layout configuration of the outputs connected to a Linux system using X11.

It's written in common lisp, as part of my language learning journey.

The project born from a personal battle of automatically setting up may screen real estate in different layouts based on my location. What started as a set of bash scripts for calling *xrandr* with appropriate options (and even using current WiFi to guess my location), quickly fell as a new computer used dynamic output naming making my static configurations not working.

So, picking on my learning of the common lisp language, I decided to make a small tool that was smarter in selecting my preferred layout based on a set of conditions. Applied to a specific DSL for configuration, the possibilities for expanding its automatic selection are infinite.

This project is currently under heavy development. Refer to the [To-Do](./TODO.md) section to know what is being worked on at the moment.

## Running

### Development 

As this is a common lisp application, the following packages are required for it to work:

- [sbcl](https://www.sbcl.org) - the compiler;
- [quicklisp](https://www.quicklisp.org/beta/) - the common lisp library manager.

Having the proper setup, the application will install the required packages and run if used the following command:

```lisp
sbcl --load run.lisp
```

For easiness of development, a `nix development` shell is supplied with the proper development setup (quicklisp is still required to be installed manually).

### Production

The application can be run as a standalone binary. It first need to be built though which can be accomplished by running `make` in the root of the repository.
repository.

## Configuration

Refer to `config.example.disp` and make it yours as `config.disp`.
