dotfiles
========

[![Build Status](https://travis-ci.org/dirn/ansible-dotfiles.svg?branch=master)](https://travis-ci.org/dirn/ansible-dotfiles)

An Ansible role to install dotfiles.

Requirements
------------

None.

Role Variables
--------------

Several variables are available to configure the role.

To set the source repository:

    dotfiles_github_repo: https://github.com/dirn/dotfiles.git

> While the name implies a GitHub repository is required, any Git URL can be
> used.

To control where the repository will be cloned:

    dotfiles_dest: ~/.dotfiles

To control if the repository is kept up-to-date:

    dotfiles_keep_updated: false

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: dirn.dotfiles
           dotfiles_github_repo: git@github.com:dirn/dotfiles.git
           dotfiles_keep_updated: true

License
-------

MIT

Author Information
------------------

This role was created by [Andy Dirnberger](https://github.com/dirn).
