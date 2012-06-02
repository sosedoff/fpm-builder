# FPM Builder

A set of bash scripts to build and convert software into deb packages.

## Usage

Formulas have been tested on Ubuntu Natty (11.04). 

Requires ruby (tested on 1.9.2)

### Setup system

If you're running a clean system (Amazon EC2 / Rackspace Cloud / Vagrant), first 
thing you have to install all required packages and build tools.

```bash
apt-get -y update && apt-get -y upgrade
apt-get install -y build-essential autoconf libssl-dev curl libcurl4-gnutls-dev zlib1g zlib1g-dev libxml2 libxml2-dev libxslt-dev libreadline5-dev libyaml-dev
```

Install ruby and fpm:

```bash
apt-get install -y ruby1.9.2
ln -s /usr/bin/ruby1.9.1 /usr/bin/ruby # Symlink to proper binary name
gem update --system # Update rubygems
gem install --no-ri --no-rdoc fpm
```

Your system is ready for building packages.

## Formulas

- node.js v0.6.18
- redis v2.4.14