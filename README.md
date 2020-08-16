# Headless Development Environment

## Introduction

This is a [Vagrant](https://www.vagrantup.com/) configuration to set up a complete, virtualized development environment for java and node users.

1. [Usage](#usage)
2. [Installation](#setup)
3. [Customize your virtual machine](#customize)
4. [Configure your new box and install new software](#configure)

## <a name="usage"></a> Usage

This requires to have [Vagrant](https://www.vagrantup.com/) installed on your machine.

It is fully based on Open Source software, and most importantly on:

- Ubuntu
- OpenJDK (Oracle JDK can't be used because of license issues)
- Node, NPM and Yarn
- Docker and Docker Compose

This "development box" also have all client applications useful for modern day development:

- MongoDB client

## <a name="setup"></a> Installation

The "Quick installation" provides a pre-build Virtual Machine, and the "Manual installation" let you build your Virtual Machine yourself. We recommend you use the "Quick installation" if you don't know which option to choose.

### Manual installation

This generates a new "development box" directly from this repository.

- Clone this repository
- Run `vagrant up`

## <a name="customize"></a> Customize your virtual machine

This is very important! Modify your system properties, depending on your host's hardware. We recommend, at least:

- 4 CPUs
- 8 Gb of RAM
- 128 Mb of video RAM

## <a name="configure"></a> Configure your new box and install new software

Start up the new box:

- Login using the `vagrant` user (not the 'Ubuntu' user which is selected by default)
  - Password is `vagrant` (please note that default keyboard layout is US!)
