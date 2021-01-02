# ansible-desktop-playbooks

[![pipeline status](https://git.shore.co.il/ansible/ansible-desktop-playbooks/badges/master/pipeline.svg)](https://git.shore.co.il/ansible/ansible-desktop-playbooks/-/commits/master)

Ansible playbooks for setting up new desktops.

## Desktop

Common tasks I do on my machine (like set Plymouth theme, make
`/tmp`{.sourceCode} tmpfs).

```
ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose desktop.yml
```

## Packages

Installs packages with APT and different languages package managers.

```
ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose pkgs.yml
```

## Workstation

Configures development tools (includes the desktop and packages
playbooks).

```
ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose workstation.yml
```

## Skype

Install Skype flatpak from flathub..

```
ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose skype.yml
```

## Slack

Install Slack desktop flatpak from flathub..

```
ansible-playbook --ask-become-pass --connection local --inventory-file localhost, --verbose slack.yml
```

## Dropbox

Installs Dropbox headless.

```
ansible-playbook --connection local --inventory-file localhost, --verbose dropbox.yml
```

## VSCode

Installs [Visual Studio Code](https://code.visualstudio.com/) from APT
repo.

```
ansible-playbook --connection local --inventory-file localhos, --verbose vscode.yml
```

## License

This software is licensed under the MIT license (see `LICENSE.txt`).

## Author Information

Nimrod Adar, [contact me](mailto:nimrod@shore.co.il) or visit my
[website](https://www.shore.co.il/). Patches are welcome via
[`git send-email`](http://git-scm.com/book/en/v2/Git-Commands-Email). The repository
is located at: <https://git.shore.co.il/expore/>.
