ansible-desktop-playbooks
#########################

.. image:: https://travis-ci.org/adarnimrod/ansible-desktop-playbooks.svg?branch=master
    :target: https://travis-ci.org/adarnimrod/ansible-desktop-playbooks

Ansible playbooks for setting up new desktops.

Desktop
=======

Common tasks I do on my machine (like set Plymouth theme, make :code:`/tmp`
tmpfs).

.. code:: shell

    ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose desktop.yml

Packages
========

Installs packages with APT and different languages package managers.

.. code:: shell

    ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose pkgs.yml

Workstation
===========

Configures development tools (includes the desktop and packages playbooks).

.. code:: shell

    ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose workstation.yml

Skype
=====

Installs the Skype Debian package since there's no repository.

.. code:: shell

    ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose skype.yml

Can be added as a Cron job under root for updates.

.. code:: shell

    ansible-playbook --connection local --inventory-file localhost, --verbose skype.yml | logger

Or maybe even (always downloads the newest version from the Git repo).

.. code:: shell

    ansible-pull --url https://www.shore.co.il/git/ansible-desktop-playbooks --verbose skype.yml | logger

Dropbox
=======

Installs Dropbox headless.

.. code:: shell

    ansible-playbook --connection local --inventory-file localhost, --verbose dropbox.yml


VSCode
======

Installs `Visual Studio Code <https://code.visualstudio.com/>`_ from APT repo.

.. code:: shell

    ansible-playbook --connection local --inventory-file localhos, --verbose vscode.yml
