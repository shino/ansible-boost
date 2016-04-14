# ansible-boost

This ansible role installs the (Boost C++ Libararies)[http://www.boost.org/] from source.

## Requirements

This role requires Ansible 1.4 higher and platforms listed in the metadata file.

## Role Variables

The variables that can be passed to this role and a brief description about them are as follows

    # Version of Boost (optional, default is 1.55.0)
    boost_version: 1.55.0

    # install prefix (optional, default is None)
    boost_prefix: /usr/local/boost

    # Work Directory, tarball is downloaded and it is expanded (optional, default is /tmp/install )
    boost_work_dir: /tmp/install

    # Options for bootstrap.sh (optional, default is empty)
    boost_bootstrap_opt: --with-libraries=log

    # Options for b2 (optional, default is empty)
    boost_make_opt: -j 8

## Examples

1) No options

    ---
    - hosts: all
      roles:
        - boost

2) With options

    ---
    - hosts: all
      roles:
        - role: boost
          boost_version: 1.49.0
          boost_prefix: /usr/local/boost
          boost_work_dir: /tmp

## Dependencies

None

## Licence

BSD

## Contribution

Fork and make pull request!

[kawasakitoshiya / ansible-boost](https://github.com/kawasakitoshiya/ansible-boost)

## Author Information

Toshiya Kawasaki
