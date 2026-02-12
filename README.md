# [Ansible role types](#ansible-role-types)

Try variables for their type.

|GitHub|GitLab|Downloads|Version|
|------|------|---------|-------|
|[![github](https://github.com/buluma/ansible-role-types/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-types/actions)|[![gitlab](https://gitlab.com/shadowwalker/ansible-role-types/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-types)|[![downloads](https://img.shields.io/ansible/role/d/buluma/types)](https://galaxy.ansible.com/buluma/types)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-types.svg)](https://github.com/buluma/ansible-role-types/releases/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-types/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  roles:
    - role: buluma.types
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-types/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: true
  gather_facts: false

  roles:
    - role: buluma.bootstrap
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-types/blob/master/defaults/main.yml):

```yaml
---
# defaults file for types

# A list of strings.
types_strings:
  - "hello"
  - "1.2.3"

# A list of integers.
types_integers:
  - 0
  - 1
  - 2

# A list of booleans.
types_booleans:
  - yes  # yamllint disable-line rule:truthy
  - Yes  # yamllint disable-line rule:truthy
  - YES  # yamllint disable-line rule:truthy
  - true  # yamllint disable-line rule:truthy
  - True  # yamllint disable-line rule:truthy
  - TRUE  # yamllint disable-line rule:truthy
  - On  # yamllint disable-line rule:truthy
  - ON  # yamllint disable-line rule:truthy
  - on  # yamllint disable-line rule:truthy
  - no  # yamllint disable-line rule:truthy
  - No  # yamllint disable-line rule:truthy
  - NO  # yamllint disable-line rule:truthy
  - false  # yamllint disable-line rule:truthy
  - False  # yamllint disable-line rule:truthy
  - FALSE  # yamllint disable-line rule:truthy
  - Off  # yamllint disable-line rule:truthy
  - OFF  # yamllint disable-line rule:truthy
  - off  # yamllint disable-line rule:truthy

# A list of floats.
types_floats:
  - 0.0
  - 0.1

# A map.
types_map:
  value1: something
  value2: not-something

# A list of lists.
types_lists:
  - [one, two, three]
  - [aa, bb, cc]
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-types/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Build Status GitHub](https://github.com/buluma/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions)|[![Build Status GitLab](https://gitlab.com/shadowwalker/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/shadowwalker/ansible-role-bootstrap)|

## [Context](#context)

This role is part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-types/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Alpine](https://hub.docker.com/r/buluma/alpine)|all|
|[Amazon](https://hub.docker.com/r/buluma/amazonlinux)|all|
|[EL](https://hub.docker.com/r/buluma/enterpriselinux)|all|
|[Debian](https://hub.docker.com/r/buluma/debian)|all|
|[Fedora](https://hub.docker.com/r/buluma/fedora)|all|
|[opensuse](https://hub.docker.com/r/buluma/opensuse)|all|
|[Ubuntu](https://hub.docker.com/r/buluma/ubuntu)|all|

The minimum version of Ansible required is 2.12, tests have been done on:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them on [GitHub](https://github.com/buluma/ansible-role-types/issues).

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-types/blob/master/LICENSE).

## [Author Information](#author-information)

[buluma](https://buluma.github.io/)

