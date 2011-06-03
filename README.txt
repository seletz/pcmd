Introduction
============

This Script is mainly a shell command generator which executes the command in
the parent shell.

Configuration
-------------

You can configure your **p-commands** in **$HOME/.p.ini**.

Syntax::

    [<p-section>]
    <p-command> = <any arbitrary shell command>

Call::

    $ p <p-command> <p-section>

Example::

    [develop]
    goto = cd /Users/rbartl/develop
    mvim = mvim /Users/rbartl/develop

The p-command executes the shell command by default in the **Terminal.app**.
This can be overwritten with the Environment Variable **PTERM**, e.g.::

    $ vim .bashrc
    export PTERM="iTerm"


Usage
-----

After you configured some commands, you can execute them like this::

    $ p goto develop # executes -> cd /Users/rbartl/develop
    $ p mvim develop # executes -> mvim /Users/rbartl/develop