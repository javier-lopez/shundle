## About

[Shundle](https://github.com/javier-lopez/shundle/) is short for _sh bundle_ and is a [sh](http://en.wikipedia.org/wiki/Unix_shell) plugin manager.

<p align="center">
<img src="http://javier.io/assets/img/shundle-2.gif" alt="shundle"/>
</p>

## Quick start

1. Set up [Shundle](https://github.com/javier-lopez/shundle/):

   ```
   $ git clone --depth=1 https://github.com/javier-lopez/shundle ~/.shundle/bundle/shundle
   ```

2. Configure bundles:

   Sample `.bashrc` (if not using bash use your shell init profile):

   ```sh
   if [ -f ~/.shundle/bundle/shundle/shundle ]; then
       .  ~/.shundle/bundle/shundle/shundle
       #let shundle manage shundle, required!
       Bundle='javier-lopez/shundle'
           #options
           SHUNDLE_ENV_COLOR=1

       #from GitHub
       Bundle='gh:javier-lopez/shundle-plugins/eternalize'
       Bundle='github:javier-lopez/shundle-plugins/colorize:master'
       Bundle='github:javier-lopez/shundle-plugins/autocd:f7916'
       Bundle='https://github.com/javier-lopez/shundle-plugins/aliazator.git'
           ALIAZATOR_PLUGINS="installed"

       #from non GitHub
       #Bundle='git://git.domain.com/rep.git'

       #from the web
       #Bundle='http://domain.com/awesome-script'

       #from the file system
       #Bundle='file://path/to/script'
   fi

   # Brief help
   # shundle list         - list installed bundles
   # shundle install      - install configured bundles
   # shundle search       - search for foo in github (experimental)
   # shundle clean        - confirm (or auto-approve) removal of unused bundles
   #
   # run shundle without parameters for more details or see the wiki for FAQ
   #
   ```

3. Install configured bundles:

   ```
   $ . ~/.bashrc
   $ shundle install
   $ . ~/.bashrc
   ```

   Installation requires [Git](http://git-scm.com/) and triggers [`git clone`](http://gitref.org/creating/#clone) for each configured repo to `~/.shundle/bundle/`.

## Uninstalling

If by any reason you dislike [Shundle](https://github.com/javier-lopez/shundle) you can uninstall it by removing the top shundle directory:

   ```
   $ rm -rf ~/.shundle
   ```

Please drop me an [email](mailto:m@javier.io) with your suggestions or open [an issue](https://github.com/javier-lopez/shundle/issues) describing the problems you faced.

## Contributors

See [Shundle contributors](https://github.com/javier-lopez/shundle/graphs/contributors)

*Thank you!*

## Inspiration and ideas from

* [vundle](https://github.com/gmarik/vundle)
* [bash-it](https://github.com/revans/bash-it)
* [alias.sh](http://alias.sh/)

## Also

* Shundle was developed and tested with [Bash](http://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) 4.2 on Linux
* Shundle will try to run in as many platforms & shells as possible
* Shundle tries to be as [KISS](http://en.wikipedia.org/wiki/KISS_principle) as possible

## TODO:
[Shundle](https://github.com/javier-lopez/shundle/) is a work in progress, so any ideas and patches are appreciated.

* write documentation
* improve install|update visualization
* tests
* improve error handling
* make it rock!
