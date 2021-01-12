# firefox-box

| License | Versioning | Build |
| ------- | ---------- | ----- |
| [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) | [![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release) | [![Build status](https://ci.appveyor.com/api/projects/status/s03xyi6h5pmvwgrc/branch/master?svg=true)](https://ci.appveyor.com/project/nikAizuddin/firefox-box/branch/master) |

Developer box for [Firefox](https://www.mozilla.org/en-US/firefox/new/).


## Getting started

```
$ git clone --recursive https://github.com/extra2000/firefox-box.git
$ cd firefox-box
```


## Creating Vagrant Box

Create Salt pillar file for Firefox, based on the given example file. You can change the value in this pillar file:
```
$ cp -v salt/roots/pillar/firefox.sls.example salt/roots/pillar/firefox.sls
```

Copy vagrant file from `vagrant/examples/` and then create the vagrant box (you can change to `--provider=libvirt` if you want to use Libvirt provider):
```
$ cp -v vagrant/examples/Vagrantfile.firefox-box.fedora-33.x86_64.example vagrant/Vagrantfile.firefox-box
$ vagrant up --provider=virtualbox
```

Provision the vagrant box which disable swap memory and install Podman:
```
$ vagrant ssh firefox-box -- sudo salt-call state.highstate
```

To start firefox:
```
$ vagrant ssh firefox-box -- sudo salt-call state.sls firefox
```

To view Firefox using web-browser, use http://firefox-box:5800. To view Firefox using VNC, execute command `$ vncviewer firefox-box:5900`.

To stop Firefox:
```
$ vagrant ssh firefox-box -- sudo salt-call state.sls firefox.service.dead
```
