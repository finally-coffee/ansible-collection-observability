# `finallycoffee.observability.grafana` ansible role

Ansible role to install and configure grafana, currently only supports docker. For docker, the python library `docker` must be installed on the target host.

## Usage

Ensure the following variables are populated:
- `grafana_config_security_secret_key`
- `grafana_config_security_admin_password`

### Authentication via OAuth2

Set `grafna_config_auth_generic_oauth_enabled` to `true` and populate variables according to the grafana docs, all generic oauth configuration values are available prefixed with `grafana_config_auth_generic_oauth_`.
