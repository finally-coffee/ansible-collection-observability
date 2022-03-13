# `finallycoffee.observability.matrix-alertmanager` ansible role

## Overview

Runs [matrix-alertmanager](https://github.com/jaywink/matrix-alertmanager)
in a docker container, and bridges alerts from alertmanager
into a configured matrix room (per configured receiver).

## Configuration

### Required configuration

The following variables need to be defined in order for `matrix-alertmanager` to
be able to work:

- `matrix_alertmanager_secret`: The secret configured in alertmanager for this receiver
- `matrix_alertmanager_homeserver_url`: URL to the homeserver to log in to, including scheme and port.
- `matrix_alertmanager_mxid`: The matrix ID in the form `@local:server.tld` to use
- `matrix_alertmanager_access_token`: The matrix access token for `matrix_alertmanager_mxid` (Note: this is not the password)
- `matrix_alertmanager_rooms`: A list of objects `{ name, room_id }` where `name` is the receiver name in alertmanager and `room_id` is a matrix room ID (not an alias)
