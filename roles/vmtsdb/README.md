# `finallycoffee.observability.vmtsdb` ansible role

## Description

This role configures `vmtsdb`, the time-series database part of victoria metrics, run in a docker container.

Per default `enableTCP6` and `envflag.enable` flags are passed to victoriametrics, enabling configuration using `vmtsdb_container_env`, using the syntax found on the official victoriametrics documentation.
