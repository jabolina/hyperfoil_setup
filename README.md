Hyperfoil Setup
=========

Deploys Hyperfoil Controller

Requirements
------------

If you want to use unreleased version (from local machine) [Hyperfoil](https://github.com/Hyperfoil/Hyperfoil) must be already built.

Dependencies
------------

Depends on `hyperfoil-shutdown` role.

Role Variables
--------------

* `hyperfoil_distribution` (optional): location of Hyperfoil distribution zip or directory (on local machine). When this is not set the distribution is downloaded from GitHub.
* `hyperfoil_version` (optional): requested version. Defaults to latest version from GitHub.
* `hyperfoil_dir` (optional): remote directory for Hyperfoil (unpacked distribution, logs...)
* `hyperfoil_controller_group` (optional): Ansible group that hosts the controller. Default is `hyperofoil-controller`.
* `hyperfoil_controller_port` (optional): Port on which Hyperfoil should listen
* `hyperfoil_controller_start_timeout` (optional): How long to wait for Hyperfoil to start, in seconds (default: 15).
* `hyperfoil_controller_args` (optional): Extra arguments to pass to the controller JVM.
* `hyperfoil_trigger_url` (optional): Configure controller to start runs from CI; this URL will be returned to CLI (with `BENCHMARK=my-benchmark&RUN_ID=xxxx` suffix) and CLI will perform a GET to that URL.
* `hyperfoil_log_config` (optional): Log4j2 configuration file
* `hyperfoil_jfr` (optional): Set to `true` to collect Flight Recordings (requires Oracle JDK)
* `hyperfoil_controller_debug_port` (optional): If set, java will listen on this debug port.
* `hyperfoil_controller_debug_suspend` (optional): Use `n` or `y`. Default is `n`.
* `hyperfoil_agent_debug_port` (optional): If set, agent java process will listen on this port.
* `libperfjava` (optional): location of libperfjava.so (for perf maps)

License
-------

Apache License, Version 2.0
