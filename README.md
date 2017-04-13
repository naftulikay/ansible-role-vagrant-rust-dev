# vagrant-rust-dev [![Build Status][svg-travis]][travis]

An Ansible role for a Vagrant-based Rust development setup.

Simply gets the latest [`rustup`][rustup] shell installer, executes it, and removes it if `rustup` is not on the `PATH`.

## Requirements

A Vagrant machine which is an operating system/architecture supported by Rust, which should almost always apply.

## Role Variables

### `rustup_args`

An optional array of arguments to pass to the `rustup` installer. Defaults to empty, just executes the installer.

### `vagrant_user`

Defaults to `vagrant`. If you're doing something non-standard, use this.

### `vagrant_group`

Defaults to `vagrant`. If you're doing something non-standard, use this.

## Dependencies

None.

## Example Playbook

Do the thing:

```
---
- hosts: all
  roles:
    - role: vagrant-rust-dev
```

Do the thing with a specific argument to the installer:

```
- hosts: all
  roles:
    - role: vagrant-rust-dev
      rustup_args: ['--do-alternative-thing']
```

## LICENSE

MIT. If you need a different license, lemme know.

 [svg-travis]: https://travis-ci.org/naftulikay/ansible-role-vagrant-rust-dev.svg?branch=master

 [rustup]: https://www.rustup.rs/
 [travis]: https://travis-ci.org/naftulikay/ansible-role-vagrant-rust-dev
