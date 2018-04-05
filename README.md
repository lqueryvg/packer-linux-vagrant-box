# Packer Virtualbox Centos7 7.2-7511

## Description

Creates a Virtualbox .box file suitable for use with Vagrant, with a very specific version of Centos with specific configuration.

- Virtualbox Guest Additions
- virtual DVD
- vagrant user *not* with uid 1000
- root pw and vagrant pw = "vagrant"
- verbose, non-graphical boot
- unnecessary drivers are removed and various basic tools are added
- en_US.UTF-8 & US keyboard
- firewall disabled
- selinux permissive
- timezone UTC

## Pre-requisites

- [Packer](http://www.packer.io/)
- [Vagrant](http://vagrantup.com/)
- [VirtualBox](https://www.virtualbox.org/) (if you want to build the VirtualBox box)

## Usage

    vi conf.json                      # check / edit config
    make clean
    make

## Directory Structure

    .
    ├── conf.json            # user configuration
    ├── Makefile
    ├── README.md
    ├── output/              # final .box file goes in here
    ├── packer_cache/        # downloaded artifacts (e.g. iso's)
    └── src/                 # source scripts and config

## Diagram

![Diagram](src/packer.png)

    Diagram source: https://drive.google.com/file/d/1eySy5xITxpMHR8rxNUjJzDktSZtpd637/view?usp=sharing