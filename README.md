# Ansible Role: Oh My Zsh

This Ansible role installs and configures Oh My Zsh for a specified user. It allows for modular customization of aliases and exports, making it easy to enable, disable, add, or remove configurations.

## Requirements

- Ansible 2.9 or higher
- Git installed on the target machine

## Role Variables

The following variables can be customized in the `vars/main.yml` file:

### User Configuration

- `omz_user`: The user for whom Oh My Zsh will be installed. Defaults to the current user.

### Aliases

A list of aliases to be added to the `.zshrc` file. Each alias should have a `name` and a `command`.

```yaml
aliases:
  - { name: 'll', command: 'ls -la' }
  - { name: 'gs', command: 'git status' }

Sure! Here is a `README.md` file for your Ansible role to install and configure Oh My Zsh.

### README.md

```markdown
# Ansible Role: Oh My Zsh

This Ansible role installs and configures Oh My Zsh for a specified user. It allows for modular customization of aliases and exports, making it easy to enable, disable, add, or remove configurations.

## Requirements

- Ansible 2.9 or higher
- Git installed on the target machine

## Role Variables

The following variables can be customized in the `vars/main.yml` file:

### User Configuration

- `omz_user`: The user for whom Oh My Zsh will be installed. Defaults to the current user.

### Aliases

A list of aliases to be added to the `.zshrc` file. Each alias should have a `name` and a `command`.

```yaml
aliases:
  - { name: 'll', command: 'ls -la' }
  - { name: 'gs', command: 'git status' }
```

### Exports

A list of environment variables to be exported in the `.zshrc` file. Each export should have a [`name`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fetc%2Fansible%2Froles%2FOhMyZShell%2Ftasks%2Fsetup-omz.yml%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A29%2C%22character%22%3A2%7D%7D%5D%2C%22ecf9d001-f168-448a-bd33-f314dac36546%22%5D "Go to definition") and a `value`.

```yaml
exports:
  - { name: 'PATH', value: '$PATH:/custom/path' }
  - { name: 'EDITOR', value: 'vim' }
```

## Example Playbook

Here is an example playbook that uses this role:

```yaml
---
- name: Install and configure Oh My Zsh
  hosts: localhost
  become: true
  vars_files:
    - vars/main.yml
  roles:
    - role: OhMyZShell
```

## Role Structure

The role follows the standard Ansible role directory structure:

```
OhMyZShell/
├── defaults
│   └── main.yml
├── files
├── handlers
│   └── main.yml
├── meta
│   └── main.yml
├── tasks
│   └── main.yml
│   └── setup-omz.yml
├── templates
├── tests
│   ├── inventory
│   └── test.yml
├── vars
│   └── main.yml
└── README.md
```

## Usage

1. **Clone the Role**: Clone this repository to your Ansible roles directory.

```sh
git clone https://github.com/fgrammatico/OhMyZShell.git roles/OhMyZShell
```

2. **Customize Variables**: Edit the `vars/main.yml` file to customize the user, aliases, and exports.

3. **Run the Playbook**: Run your playbook to install and configure Oh My Zsh.

```sh
ansible-playbook -i localhost, playbook.yml
```

## License

MIT

## Author Information

This role was created by [FmG](https://github.com/fgrammatico).
```

### Explanation

- **Requirements**: Lists the prerequisites for using the role.
- **Role Variables**: Describes the variables that can be customized.
- **Example Playbook**: Provides an example of how to use the role in a playbook.
- **Role Structure**: Shows the directory structure of the role.
- **Usage**: Explains how to clone the role, customize variables, and run the playbook.
- **License**: Specifies the license for the role.
- **Author Information**: Provides information about the author.

This `README.md` file should provide clear instructions on how to use and customize the role.