# `finallycoffee.observability.postgres_exporter` ansible role

## Overview

Ansible role to deploy [`postgres_exporter`](https://github.com/prometheus-community/postgres_exporter),
running in a docker container.

## Configuration

Set `postgres_exporter_db_[host|post|user|pass]` according to your
databases configuration, and scrape the container on it's port `9187`
(e.g.: `http://{container_ip}:9187/metrics`).

For more configuration options using environment variables, see the
[official README](https://github.com/prometheus-community/postgres_exporter)
and set the configuration in `postgres_exporter_container_env` to override
the defaults.

