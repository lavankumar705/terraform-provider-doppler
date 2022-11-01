---
page_title: "doppler_service_token Resource - terraform-provider-doppler"
subcategory: ""
description: |-
	Manage a Doppler service_token.
---

# doppler_service_token (Resource)

Manage a Doppler service token.

## Example Usage

```terraform
resource "doppler_service_token" "backend_ci_token" {
  project = "backend"
  config = "ci"
  name = "Builder Token"
  access = "read"
}

# Service token key available as `doppler_service_token.backend_ci_token.key`
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **config** (String) The name of the Doppler config where the service token is located
- **name** (String) The name of the Doppler service token
- **project** (String) The name of the Doppler project where the service token is located

### Optional

- **access** (String) The access level (read or read/write)
- **id** (String) The ID of this resource.

### Read-Only

- **key** (String, Sensitive) The key for the Doppler service token