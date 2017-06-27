Role Name
=========

This role is used to build a development version of the [Messaging Performance Tool](https://github.com/orpiske/msg-perf-tool). Although functional, this role is still in development.

Build/Test Status
------------

Linux Build Status: [![Linux Build Status](https://api.travis-ci.org/msgqe/mpt-devel.svg?branch=master)](https://travis-ci.org/msgqe/mpt-devel)


Requirements
------------

The package libselinux-python is required for running the test.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `mpt_maestro_url` | http://localhost:1883 | The URL for the maestro broker |
| `mpt_log_dir` | /var/log/mpt | The log directory for the MPT |
| `mpt_receiver` | true | Whether to keep the mpt_receiver_daemon in a running state |
| `mpt_sender` | true | Whether to keep the mpt_sender_daemon in a running state |
| `mpt_inspector` | false | Whether to keep the mpt_inspector_daemon in a running state |
| `mpt_devel_skip_provisioning` | false | Whether to skip base system provisioning |


Dependencies
------------

This role depends on the [basic-server](https://github.com/msgqe/basic-server).

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

  - hosts: all
    remote_user: root
    roles:
      - basic-server
      - mpt-devel


License
-------

Apache

Author Information
------------------

Messaging team @ redhat.com
