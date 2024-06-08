# `finallycoffee.observability.vmalert` ansible role

## Description

This role configures `vmalert` and runs it in the officially distributed docker container.

The default configuration file for recording rules is `vmalert_recording_config` and the default file for alerts is `vmalert_alert_config`. To set rules in a prometheus-like syntax, supply them to the role using `vmalert_alerts` or `vmalert_records`.

It is also possible to pass extra rule-files to load using `vmalert_rule_files`, though care must be taken to also mount them to the location in the container by populating `vmalert_container_volumes`.

VM alert runs with the `envflag.enable` flag by default, so configuration to vmalert can be passed using `vmalert_container_env` with the syntax found on the official victoriametrics documentation.
