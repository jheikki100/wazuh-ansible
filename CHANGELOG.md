# Change Log
All notable changes to this project will be documented in this file.

## [v3.9.3_7.2.0]

### Added 
- Update to Wazuh v3.9.3 ([rshad](https://github.com/rshad) [PR#206](https://github.com/wazuh/wazuh-ansible/pull/206#))
- Added Versioning Control for Wazuh stack's components installation, so now it's possible to specify which package to install for wazuh-manager, wazuh-agent, Filebeat, Elasticsearch and Kibana. ([rshad](https://github.com/rshad) [PR#206](https://github.com/wazuh/wazuh-ansible/pull/206#))
- Fixes for Molecule testing issues. Issues such as Ansible-Lint and None-Idempotent tasks. ([rshad](https://github.com/rshad) [PR#206](https://github.com/wazuh/wazuh-ansible/pull/206#))
- Fixes for Wazuh components installations' related issues. Such issues were related to determined OS distributions such as `Ubuntu Trusty` and `CetOS 6`. ([rshad](https://github.com/rshad) [PR#206](https://github.com/wazuh/wazuh-ansible/pull/206#))
-  Created Ansible playbook and role in order to automate the uninstallation of already installed Wazuh components. ([rshad](https://github.com/rshad) [PR#206](https://github.com/wazuh/wazuh-ansible/pull/206#))


## [v3.9.2_7.1.1]

### Added 

- Update to Wazuh v3.9.2
- Support for Elastic 7
- Ability to deploy an Elasticsearch cluster [#6b95e3](https://github.com/wazuh/wazuh-ansible/commit/6b95e304b6ac4dfec08df5cd0fe29be9cc7dc22c)

## [v3.9.2_6.8.0]

### Added 

- Update to Wazuh v3.9.2

## [v3.9.1]

### Added 

- Update to Wazuh v3.9.1
- Support for ELK v6.8.0

## [v3.9.0]

### Added

- Update to Wazuh Wazuh v3.9.0 ([manuasir](https://github.com/manuasir) [#177](https://github.com/wazuh/wazuh-ansible/pull/177)).
- Support for Elasticsearch v6.7.1 ([LuisGi91](https://github.com/LuisGi91) [#168](https://github.com/wazuh/wazuh-ansible/pull/168)).
- Added Molecule testing suit ([JJediny](https://github.com/JJediny) [#151](https://github.com/wazuh/wazuh-ansible/pull/151)).
- Added Molecule tests for Wazuh Manager ([dj-wasabi](https://github.com/dj-wasabi) [#169](https://github.com/wazuh/wazuh-ansible/pull/169)).
- Added Molecule tests for Wazuh Agent ([dj-wasabi](https://github.com/dj-wasabi) [#174](https://github.com/wazuh/wazuh-ansible/pull/174)).

### Changed

- Updated network commands ([kravietz](https://github.com/kravietz) [#159](https://github.com/wazuh/wazuh-ansible/pull/159)).
- Enable active response section ([kravietz](https://github.com/kravietz) [#155](https://github.com/wazuh/wazuh-ansible/pull/155)).

### Fixed

- Fix default active response ([LuisGi93](https://github.com/LuisGi93) [#164](https://github.com/wazuh/wazuh-ansible/pull/164)).
- Changing from Oracle Java to OpenJDK ([LuisGi93](https://github.com/LuisGi93) [#173](https://github.com/wazuh/wazuh-ansible/pull/173)).
- Adding alias to agent config file template ([LuisGi93](https://github.com/LuisGi93) [#163](https://github.com/wazuh/wazuh-ansible/pull/163)).

## [v3.8.2]

### Changed 

- Update to Wazuh version v3.8.2. ([#150](https://github.com/wazuh/wazuh-ansible/pull/150))

## [v3.8.1]

### Changed
- Update to Wazuh version v3.8.1. ([#148](https://github.com/wazuh/wazuh-ansible/pull/148))


## [v3.8.0]

### Added

- Added custom name for single agent registration ([#117](https://github.com/wazuh/wazuh-ansible/pull/117))
- Adapt ossec.conf file for windows agents ([#118](https://github.com/wazuh/wazuh-ansible/pull/118))
- Added labels to ossec.conf ([#135](https://github.com/wazuh/wazuh-ansible/pull/135))

### Changed

- Changed Windows installation directory ([#116](https://github.com/wazuh/wazuh-ansible/pull/116))
- move redundant tags to the outer block ([#133](https://github.com/wazuh/wazuh-ansible/pull/133))
- Adapt new version (3.8.0-6.5.4) ([#144](https://github.com/wazuh/wazuh-ansible/pull/144))

### Fixed

- Fixed a couple linting issues with yamllint and ansible-review ([#111](https://github.com/wazuh/wazuh-ansible/pull/111))
- Fixes typos: The word credentials doesn't have two consecutive e's ([#130](https://github.com/wazuh/wazuh-ansible/pull/130))
- Fixed multiple remote connection ([#120](https://github.com/wazuh/wazuh-ansible/pull/120))
- Fixed null value for wazuh_manager_fqdn ([#132](https://github.com/wazuh/wazuh-ansible/pull/132))
- Erasing extra spaces in playbooks ([#131](https://github.com/wazuh/wazuh-ansible/pull/131))
- Fixed oracle java cookies ([#143](https://github.com/wazuh/wazuh-ansible/pull/143))

### Removed

- delete useless files from wazuh-manager role ([#137](https://github.com/wazuh/wazuh-ansible/pull/137))

## [v3.7.2]

### Changed

- Adapt configuration to current release ([#106](https://github.com/wazuh/wazuh-ansible/pull/106))

## [v3.7.1]

### Added

 - include template local_internal_options.conf. ([#87](https://github.com/wazuh/wazuh-ansible/pull/87))
 - Add multiple Elasticsearch IPs for Logstash reports. ([#92](https://github.com/wazuh/wazuh-ansible/pull/92))

### Changed

 - Changed windows agent version. ([#89](https://github.com/wazuh/wazuh-ansible/pull/89))
 - Updating to Elastic Stack to 6.5.3 and Wazuh 3.7.1. ([#108](https://github.com/wazuh/wazuh-ansible/pull/108))

### Fixed

- Solve the conflict betwwen tha agent configuration and the shared master configuration. Also include monitoring for `/var/log/auth.log`. ([#90](https://github.com/wazuh/wazuh-ansible/pull/90))
- Moved custom_ruleset files. ([#98](https://github.com/wazuh/wazuh-ansible/pull/98))
- Add authlog fix to localfile. ([#99](https://github.com/wazuh/wazuh-ansible/pull/99))
- Exceptions reload systemd. ([#114](https://github.com/wazuh/wazuh-ansible/pull/114))

### Removed

- clean old code for windows agent. ([#86](https://github.com/wazuh/wazuh-ansible/pull/86))

## v3.7.0-3701

### Added

- Amazon Linux deployments are now supported ([#71](https://github.com/wazuh/wazuh-ansible/pull/71)) and for the old repository structure ([#67](https://github.com/wazuh/wazuh-ansible/pull/67))
- Added the option to add rule files and decoders directly over the local rule and decoder directories in /var/ossec/etc ([#81](https://github.com/wazuh/wazuh-ansible/pull/81)).
- Added the necessary variables to configure a new configuration template for the Wazuh API ([#80](https://github.com/wazuh/wazuh-ansible/pull/80)).
- Added the option to verify the shared configuration for agents set in the manager ([#76](https://github.com/wazuh/wazuh-ansible/pull/76)).
- Added the option to configure the active response ([#75](https://github.com/wazuh/wazuh-ansible/pull/75)).

### Changed

- Repository restructure.
- Extended conditions to register a Wazuh agent. Now will register the agent in cases where there is no client.keys or the file exists but this empty ([#79](https://github.com/wazuh/wazuh-ansible/pull/79)).
- Grouping of tasks in a block under the same condition to improve the efficiency of the code ([#74](https://github.com/wazuh/wazuh-ansible/pull/74)).
- Improved efficiency of the Java repository ([#73](https://github.com/wazuh/wazuh-ansible/pull/73)).

### Fixed

- Fix oracle java cookie ([#71](https://github.com/wazuh/wazuh-ansible/pull/71)).
- include the logall_json label in ossec.conf template. This was causing an error when recreating the cdb_lists ([#84](https://github.com/wazuh/wazuh-ansible/pull/84)).

## v3.6.0

Ansible starting point.

Roles:
 - Elastic Stack:
   - ansible-elasticsearch: This role is prepared to install elasticsearch on the host that runs it.
   - ansible-kibana: Using this role we will install Kibana on the host that runs it.
 - Wazuh:
   - ansible-filebeat: This role is prepared to install filebeat on the host that runs it.
   - ansible-wazuh-manager: With this role we will install Wazuh manager and Wazuh API on the host that runs it.
   - ansible-wazuh-agent: Using this role we will install Wazuh agent on the host that runs it and is able to register it.

