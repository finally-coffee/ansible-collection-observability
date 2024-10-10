# `finallycoffee.observability.vmagent` ansible role

Install and configure the
[victoriametrics agent `vmagent`](https://docs.victoriametrics.com/vmagent/)
using the [supported deployment types (see `vars/main.yml#L5`)](vars/main.yml#L5).

## Configuration

Set scrape job configuration as complex data in `vmagent_config_scrape_configs`.
To tune the scrape interval, override `vmagent_config_global_scrape_interval`,
or modify / extend `vmagent_config` directly.

### Prometheus remote write api with basic auth

One of the more common methods of sending the collected metrics to a
central prometheus server. Set the following variables to archieve this:

```yaml
vmagent_flags:
  remoteWrite_url: https://my.prometheus.instance.example.com/api/v1/write
  remoteWrite_basicAuth_username: my_prom_user
  remoteWrite_basicAuth_passwordFile: /path/to/password/file.key
```

For the full set of options, see either the
[vmagents' "Advanced usage" documentation](https://docs.victoriametrics.com/vmagent/#advanced-usage)
or run `vmagent -help` for the same output.
