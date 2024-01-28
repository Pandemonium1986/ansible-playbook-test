# Ansible Playbook - test

[![GitHub Super Linter](https://github.com/Pandemonium1986/ansible-playbook-test/actions/workflows/linter.yml/badge.svg)](https://github.com/Pandemonium1986/ansible-playbook-test/actions/workflows/linter.yml)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
![Github license](https://img.shields.io/github/license/Pandemonium1986/ansible-playbook-test.svg?logo=github)

A simple playbook to test my ansible roles and collections.

## Getting Started

This playbook serves as a smoke test for all my roles and collections. It is, however, exhaustive and correctly configured, making it a template for use in a real functional context.


### Prerequisites

Go to the [Built With](#built-with) section

### Installing

Clone repository

```sh
mkdir -p ~/git/pandemonium1986/ && \
cd ~/git/pandemonium1986/ && \
git clone git@github.com:Pandemonium1986/ansible-playbook-test.git && \
cd ~/git/pandemonium1986/ansible-playbook-test
```


## Running the tests

To run the smokes tests, simply run the playbook.

```yaml
cd ~/git/pandemonium1986/ansible-playbook-test && \
ansible-galaxy install -r requirements.yml && \
ansible-playbook playbook.yml
```

## Built With

- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html) - Provisioning
- [Vagrant](https://www.vagrantup.com/downloads.html) - To build and manage the box.
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads) - The only provider available.


## Contributing

Please read [CONTRIBUTING.md](https://github.com/Pandemonium1986/.github/blob/main/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Pre Committing

This repository use [pre-commit](https://pre-commit.com) to manage commit-msg, pre-commit and pre-push hooks (if necessary).
Be sure to install them before any push.

```sh
cd MY_REPO && \
pre-commit install --hook-type commit-msg && \
pre-commit install --hook-type pre-push && \
pre-commit install
```

For more info see this [cheatsheet](https://github.com/Pandemonium1986/cheatsheet/blob/main/Commit.md)

Also every commit MUST follow the [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/).

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/Pandemonium1986/ansible-playbook-test/tags).

## Authors

- **Michael Maffait** - _Initial work_ - [Pandemonium1986](https://github.com/Pandemonium1986)

See also the list of [contributors](https://github.com/Pandemonium1986/ansible-playbook-test/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details
