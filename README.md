![Logo](https://raw.githubusercontent.com/idealista/android-sdk_role/master/logo.gif)

[![Build Status](https://travis-ci.org/idealista/android-sdk_role.png)](https://travis-ci.org/idealista/android-sdk_role)

# Android SDK Ansible role

This Ansible role installs Android SDK in a Debian environment.

- [Getting Started](#getting-started)
	- [Prerequisities](#prerequisities)
	- [Installing](#installing)
- [Usage](#usage)
- [Testing](#testing)
- [Built With](#built-with)
- [Versioning](#versioning)
- [Authors](#authors)
- [License](#license)
- [Contributing](#contributing)

## Getting Started

These instructions will get you a copy of the role for your Ansible playbook. Once launched, it will set up [Android SDK](https://developer.android.com/studio) in a Debian system.

### Prerequisities

Ansible 2.7.9.0 version installed.
Inventory destination should be a Debian environment.

For testing purposes, [Molecule](https://molecule.readthedocs.io/) (version 2.20) with [Docker](https://www.docker.com/) as provider.

### Installing

Create or add to your roles dependency file (e.g requirements.yml):

``` yml
- src: idealista.android-sdk_role
  version: 1.0.0
  name: android-sdk
```

Install the role with ansible-galaxy command:

```
ansible-galaxy install -p roles -r requirements.yml -f
```

Use in a playbook:

``` yml
---
- hosts: someserver
  roles:
    - role: android-sdk
```

## Usage

Look to the [defaults](defaults/main.yml) properties file to see the possible configuration properties.

## Testing

### Using Docker as provider
```
pipenv install -r test-requirements.txt --python 2.7
pipenv run molecule test
```

See molecule.yml to check possible testing platforms.

## Built With

![Ansible](https://img.shields.io/badge/ansible-2.7.9.0-green.svg)
![Molecule](https://img.shields.io/badge/molecule-2.20.0-green.svg)

## Versioning

For the versions available, see the [tags on this repository](https://github.com/idealista/android-sdk_role/tags).

Additionaly you can see what change in each version in the [CHANGELOG.md](CHANGELOG.md) file.

## Authors

* **Idealista** - *Work with* - [idealista](https://github.com/idealista)

See also the list of [contributors](https://github.com/idealista/android-sdk_role/contributors) who participated in this project.

## License

![Apache 2.0 License](https://img.shields.io/hexpm/l/plug.svg)

This project is licensed under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) license - see the [LICENSE](LICENSE) file for details.

## Contributing

Please read [CONTRIBUTING.md](.github/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.
