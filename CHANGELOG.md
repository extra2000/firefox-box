# Changelog

## [1.2.0](https://github.com/extra2000/firefox-box/compare/v1.1.0...v1.2.0) (2021-03-08)


### Features

* **submodule:** Add [zabbix-agent-formula v2.0.0](https://github.com/extra2000/zabbix-agent-formula/releases/tag/v2.0.0) ([4cb2665](https://github.com/extra2000/firefox-box/commit/4cb26656bfa214a4252c9d051641f561b73d39b7))
* **submodule:** Update `firefox-formula` to [v1.1.0](https://github.com/extra2000/firefox-formula/releases/tag/v1.1.0) ([fb40e0e](https://github.com/extra2000/firefox-box/commit/fb40e0ea71cf6c10f10f28d6f7316e8db0295c7e))


### Continuous Integrations

* **AppVeyor:** Add instruction to create Zabbix agent pillar file ([31f8b30](https://github.com/extra2000/firefox-box/commit/31f8b3047b7417a89d5681c3c1c0d011b89ca6bf))
* **AppVeyor:** Ensure `git submodule` is recursive ([f2a4438](https://github.com/extra2000/firefox-box/commit/f2a4438980f121fb52d7dc6cabb1f48921bcd38d))


### Code Refactoring

* **submodule:** Remove `cockpit-formula` in favor of `zabbix-agent-formula` ([f5eed22](https://github.com/extra2000/firefox-box/commit/f5eed22df63f51f81e0bc77375146cb13c000d75))


### Documentations

* **README:** Update instructions and descriptions for Zabbix agent ([9b5c724](https://github.com/extra2000/firefox-box/commit/9b5c724e6d0e79598d823b363b97dfc3440547d5))

## [1.1.0](https://github.com/extra2000/firefox-box/compare/v1.0.1...v1.1.0) (2021-01-20)


### Features

* **submodule:** Update `cockpit-formula` to [v1.0.2](https://github.com/extra2000/cockpit-formula/releases/tag/v1.0.2) ([f059975](https://github.com/extra2000/firefox-box/commit/f059975da63d82d901f3c705bead2a7c55d03c06))
* **submodule:** Update `podman-formula` to [v2.2.1](https://github.com/extra2000/podman-formula/releases/tag/v2.2.1) ([ca099c9](https://github.com/extra2000/firefox-box/commit/ca099c953a70fbe4586aded0efb66ab7ab549b57))


### Continuous Integrations

* **AppVeyor:** Upgrade Ubuntu from `18.04` to `20.04` ([e23358b](https://github.com/extra2000/firefox-box/commit/e23358b6b19cb4642b0277ee317482d6ed7c90b0))

### [1.0.1](https://github.com/extra2000/firefox-box/compare/v1.0.0...v1.0.1) (2021-01-13)


### Documentations

* **README:** Update instructions for viewing VNC ([6ce7c35](https://github.com/extra2000/firefox-box/commit/6ce7c35d198e10db99c396c4a253c766e30206d9))


### Fixes

* **firefox-formula, pillar/firefox.sls.example:** Add IP address option for VNC ports binding and using default `127.0.0.1` as the IP for the VNC ports binding ([289e772](https://github.com/extra2000/firefox-box/commit/289e772ce5972867c36504c583e1f733a4cbd77a))

## 1.0.0 (2021-01-13)


### Features

* **salt:** Add implementations to `salt/` ([f577958](https://github.com/extra2000/firefox-box/commit/f5779581e054179382a499b37f35e4e35cc4c02d))
* **submodule:** Add Cockpit Formula ([f21e900](https://github.com/extra2000/firefox-box/commit/f21e900bbec8b8330e2c38540a7beb0f0c94f8fc))
* **submodule:** Add Firefox Formula ([cc45ae1](https://github.com/extra2000/firefox-box/commit/cc45ae13f828ae1b38250feaac4a2e62743222ac))
* **submodule:** Add Podman Formula ([d8cf5f0](https://github.com/extra2000/firefox-box/commit/d8cf5f0c351aa7b1d6c03042af9bf9005228635d))
* **vagrant:** Import Vagrant files from [extra2000/generic-box v1.4.0](https://github.com/extra2000/generic-box/releases/tag/v1.4.0) ([2f6b60a](https://github.com/extra2000/firefox-box/commit/2f6b60a945e61f0a1ba6b45325d4ca1c994b079d))


### Continuous Integrations

* Add AppVeyor with `semantic-release` bot ([5c281be](https://github.com/extra2000/firefox-box/commit/5c281be2ccb1ac3dcae76e86dc09b5926b693e32))


### Documentations

* **README:** Update `README.md` ([2c64347](https://github.com/extra2000/firefox-box/commit/2c643478851717a18e9b3afdcd994dcad3d360af))
