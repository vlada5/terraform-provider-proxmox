---
layout: page
title: proxmox_virtual_environment_acme_plugins
parent: Data Sources
subcategory: Virtual Environment
description: |-
  Retrieves the list of ACME plugins.
---

# Data Source: proxmox_virtual_environment_acme_plugins

Retrieves the list of ACME plugins.

## Example Usage

```terraform
data "proxmox_virtual_environment_acme_plugins" "example" {}

output "data_proxmox_virtual_environment_acme_plugins" {
  value = data.proxmox_virtual_environment_acme_plugins.example.plugins
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Read-Only

- `plugins` (Attributes List) List of ACME plugins (see [below for nested schema](#nestedatt--plugins))

<a id="nestedatt--plugins"></a>
### Nested Schema for `plugins`

Read-Only:

- `api` (String) API plugin name.
- `data` (Map of String) DNS plugin data.
- `digest` (String) Prevent changes if current configuration file has a different digest. This can be used to prevent concurrent modifications.
- `plugin` (String) ACME Plugin ID name.
- `type` (String) ACME challenge type (dns, standalone).
- `validation_delay` (Number) Extra delay in seconds to wait before requesting validation. Allows to cope with a long TTL of DNS records (0 - 172800).