# `finallycoffee.observability.cadvisor` ansible role

## Overview

Deploys [cadvisor](https://github.com/google/cadvisor/), a daemon
for collecting and exporting information about running (docker)
containers in a docker container.

## Configuration

In order to scrape `/metrics` of running containers, it is recommended
to expose the default port of cadvisor to the host using
```yaml
cadvisor_container_ports:
  - "127.0.0.1:8080:8080`
```
so that cadvisor metrics are exposed at `http://127.0.0.1:8080/metrics`.

### Enabling/Disabling collection of metrics

By setting `cadvisor_disabled_metrics`, the collection of metrics
can be disabled. The default list of disabled metrics is quite extensive,
so when enabling a disabled-by-default metric, it is recommended to
use `cadvisor_force_enable_metrics` instead, as it's empty by default.
