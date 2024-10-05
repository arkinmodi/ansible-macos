# Automated Personal Environment Setup

1. Install Xcode Command Line Tools
    ```sh
    xcode-select --install
    ```
1. Install [Homebrew](https://brew.sh/)
1. Setup
   [GitHub SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
1. Install [Ansible](https://www.ansible.com/) via Homebrew
    ```sh
    brew install ansible
    ```
1. Run setup playbook

    ```sh
    ansible-pull --ask-become-pass --url https://github.com/arkinmodi/ansible-macos

    # Or if cloned locally
    ansible-playbook --ask-become-pass local.yml

    # Shortcut for entering password
    ansible-playbook ~/code/ansible-macos/local.yml -e "ansible_become_pass=$(op read '...')"
    ```

## Notes

View Ansible facts

```sh
ansible localhost -m ansible.builtin.setup
```
