CloudFormation Templates
========================

This repo contains AWS CloudFormation Stack Templates. Each stack is stored as
one or more YAML files. Those files are converted to a single JSON file before
uploading to CloudFormation. YAML is used primarily because it allows
comments.

A top-level resource, PreProcess, can be used for YAML anchors. This resource
will not be present in the final JSON file.

To generate the combined JSON file (as of 2014-06-17):

```
./bin/convert_yaml_to_json -s directory/of/yaml -o path/to/combined.json
```

The `path/to/combined.json` can then be uploaded in CloudFormation.
