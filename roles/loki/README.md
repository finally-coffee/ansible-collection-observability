# `finallycoffee.observability.loki` ansible role

## Overview

Runs [loki](https://github.com/grafana/loki) in a docker container.

## Configuration

Listens on `3100` per default, and can be changed using `loki_config_server_http_listen_port` / `loki_config_server_http_listen_addr`.

### Required configuration

Loki's storage config can be provided in `loki_config_storage_config`,
the schema configs can be provided in `loki_config_schema_config_configs`.
