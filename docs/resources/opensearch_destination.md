---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "elasticsearch_opensearch_destination Resource - terraform-provider-elasticsearch"
subcategory: "OpenSearch"
description: |-
  Provides an OpenSearch destination, a reusable communication channel for an action, such as email, Slack, or a webhook URL. Please refer to the OpenSearch destination documentation https://opendistro.github.io/for-elasticsearch-docs/docs/alerting/monitors/#create-destinations for details.
---

# elasticsearch_opensearch_destination (Resource)

Provides an OpenSearch destination, a reusable communication channel for an action, such as email, Slack, or a webhook URL. Please refer to the OpenSearch [destination documentation](https://opendistro.github.io/for-elasticsearch-docs/docs/alerting/monitors/#create-destinations) for details.

## Example Usage

```terraform
resource "elasticsearch_opensearch_destination" "test_destination" {
  body = <<EOF
{
  "name": "my-destination",
  "type": "slack",
  "slack": {
    "url": "http://www.example.com"
  }
}
EOF
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **body** (String) The JSON body of the destination.

### Read-Only

- **id** (String) The ID of this resource.

## Import

Import is supported using the following syntax:

```shell
# Import by name
terraform import elasticsearch_opensearch_destination.test_destination my-destination
```