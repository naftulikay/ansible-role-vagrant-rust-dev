# ansible-role-vagrant-rust-dev [![Build Status][travis.svg]][travis]

An Ansible role for a Vagrant-based Rust development setup.

Available on Ansible Galaxy at [`naftulikay.vagrant-rust-dev`][galaxy].

## Requirements

A Vagrant machine which is an operating system/architecture supported by Rust, which should almost always apply.

## Role Variables

<dl>
  <dt><code>vagrant_user</code></dt>
  <dd>The username of the Vagrant user, defaults to <code>vagrant</code></dd>
</dl>

> Please see the upstream [`naftulikay.vagrant-base`][vagrant-base] and [`naftulikay.rust-dev`][rust-dev] roles for
additional supported variables.

## Dependencies

 - [`naftulikay.vagrant-base`][vagrant-base]: Provides base Vagrant configuration.
 - [`naftulikay.rust-dev`][rust-dev]: Provides a basic Rust development environment.

## Example Playbook

Install a Rust development environment within the Vagrant machine:

```
---
- hosts: all
  roles:
    - role: vagrant-rust-dev
```

## LICENSE

MIT.

 [travis]: https://travis-ci.org/naftulikay/ansible-role-vagrant-rust-dev
 [travis.svg]: https://travis-ci.org/naftulikay/ansible-role-vagrant-rust-dev.svg?branch=master
 [galaxy]: https://galaxy.ansible.com/naftulikay/vagrant-rust-dev/
 [vagrant-base]: https://galaxy.ansible.com/naftulikay/vagrant-base/
 [rust-dev]: https://galaxy.ansible.com/naftulikay/rust-dev/
