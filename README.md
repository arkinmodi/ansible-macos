# Automated Personal Environment Setup

1. Install Xcode Command Line Tools
    ```sh
    xcode-select --install
    ```
1. Install [Homebrew](https://brew.sh/)
1. Install [Ansible](https://www.ansible.com/) via Homebrew
    ```sh
    brew install ansible
    ```
1. Run setup playbook
    ```sh
    ansible-pull -U https://github.com/arkinmodi/ansible-macos

    # Or if cloned locally
    ansible-playbook local.yml
    ```
