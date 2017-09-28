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

Install Skype flatpak from flathub..

.. code:: shell

    ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose skype.yml

Slack
=====

Install Slack desktop flatpak from flathub..

.. code:: shell

    ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose slack.yml

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
