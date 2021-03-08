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

Create Salt pillar file for Firefox and Zabbix agent, based on the given example file. You can change the value in this pillar file:
```
$ cp -v salt/roots/pillar/firefox.sls.example salt/roots/pillar/firefox.sls
$ cp -v salt/roots/pillar/zabbix-agent.sls.example salt/roots/pillar/zabbix-agent.sls
```

Copy vagrant file from `vagrant/examples/` and then create the vagrant box (you can change to `--provider=libvirt` if you want to use Libvirt provider):
```
$ cp -v vagrant/examples/Vagrantfile.firefox-box.fedora-33.x86_64.example vagrant/Vagrantfile.firefox-box
$ vagrant up --provider=virtualbox
```

Provision the vagrant box which disable swap memory, install Podman, and deploy Zabbix agent:
```
$ vagrant ssh firefox-box -- sudo salt-call state.highstate
```

To start firefox:
```
$ vagrant ssh firefox-box -- sudo salt-call state.sls firefox
```

If you set `firefox.lookup.ip: 0.0.0.0` in `salt/roots/pillar/firefox.sls`, you can use VNC via web-browser http://firefox-box:5800 and `firefox-box:5900` with VNC client. Otherwise, you need to SSH tunnel those ports to your `localhost` for example below. Then, use http://localhost:15800 and `localhost:15900`:
```
$ ssh -L 15900:127.0.0.1:15900 -L 15800:127.0.0.1:5800 -p 22 vagrant@firefox-box
```

To stop Firefox:
```
$ vagrant ssh firefox-box -- sudo salt-call state.sls firefox.service.dead
```
