ansible-desktop-playbooks
#########################

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

Skype
=====

Installs the Skype Debian package since there's no repository.

.. code:: shell

    ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose skype.yml

Can be added as a Cron job under root for updates.

.. code:: shell

    ansible-playbook --connection local --inventory-file localhost, --verbose skype.yml | logger

Dropbox
=======

Installs Dropbox headless.

.. code:: shell

    ansible-playbook --connection local --inventory-file localhost, --verbose dropbox.yml
