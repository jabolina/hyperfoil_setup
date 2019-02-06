Hyperfoil Setup
=========

Deploys Hyperfoil Controller and Agents

Requirements
------------

This role requires built [Hyperfoil](https://github.com/Hyperfoil/Hyperfoil).

Dependencies
------------

Depends on `hyperfoil-shutdown` role.

Role Variables
--------------

* `hyperfoil_distribution` (optional): location of Hyperfoil zip distribution (on local machine). When this is not set the distribution is downloaded from GitHub.
* `hyperfoil_version` (optional): requested version. Defaults to latest version from GitHub.
* `hyperfoil_role` (required): define if the role should setup `agent` or `controller`
* `hyperfoil_dir` (optional): remote directory for Hyperfoil (unpacked distribution, logs...)
* `hyperfoil_controller_group` (optional): Ansible group that hosts the controller. Default is `hyperofoil-controller`.
* `hyperfoil_controller_port` (optional): Port on which Hyperfoil should listen
* `hyperfoil_log_config` (optional): Log4j2 configuration file
* `hyperfoil_jfr` (optional): Set to `true` to collect Flight Recordings (requires Oracle JDK)
* `debug_port` (optional): If set, java will listen on this debug port
* `debug_suspend` (optional): Use `n` or `y`
* `libperfjava` (optional): location of libperfjava.so (for perf maps)

License
-------

Apache License, Version 2.0
