---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "grafana_dashboard Resource - terraform-provider-grafana"
subcategory: ""
description: |-
  Official documentation https://grafana.com/docs/grafana/latest/dashboards/HTTP API https://grafana.com/docs/grafana/latest/http_api/dashboard/
---

# grafana_dashboard (Resource)

* [Official documentation](https://grafana.com/docs/grafana/latest/dashboards/)
* [HTTP API](https://grafana.com/docs/grafana/latest/http_api/dashboard/)

## Example Usage

```terraform
resource "grafana_dashboard" "metrics" {
  config_json = file("grafana-dashboard.json")
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **config_json** (String) The complete dashboard model JSON.

### Optional

- **folder** (Number) The id of the folder to save the dashboard in.
- **id** (String) The ID of this resource.

### Read-Only

- **dashboard_id** (Number) The numeric ID of the dashboard computed by Grafana.
- **slug** (String) URL friendly version of the dashboard title.

## Import

Import is supported using the following syntax:

```shell
terraform import grafana_dashboard.dashboard_name {{dashboard_slug}}
```