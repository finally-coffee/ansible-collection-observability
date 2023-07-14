# `finallycoffee.observability.alertmanager` ansible role

## Description

This role configures and runs prometheus alertmanager in a docker container.

The config file is templated on the host and persisted in `alertmanager_config_file`.

The alertmanager config can be passed by setting `alertmanager_config`, which expects the same yaml
format as the "normal" alertmanager config file (with top-level keys `global`, `route` and `receivers`).
