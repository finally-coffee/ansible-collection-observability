# `finallycoffee.observability` ansible collection

## Overview

Ansible roles for running monitoring infrastructure, regardless of logs,
metrics or alerting.

## Roles

- [`alertmanager`](roles/alertmanager/README.md): Runs prometheus'
  alertmanager for receiving alerts from prometheus and routing them
  to the correct configured receivers.

- [`matrix-alertmanager`](roles/matrix-alertmanager/README.md): An alert-
  manager receiver which posts alerts to a configured matrix channel
  using alertmanagers' webhooks.

- [`vmtsdb`](roles/vmtsdb/README.md): VictoriaMetrics time series database.

- [`vmalert`](roles/vmalert/README.md): VictoriaMetrics alerting and
  ruling engine.

- [`postgres_exporter`](roles/postgres_exporter/README.md): Prometheus
  exporter for postgres databases, in a docker container.

## License

[CNPLv7+](LICENSE.md): Cooperative Nonviolent Public License
