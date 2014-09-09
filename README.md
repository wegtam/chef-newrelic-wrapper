# Newrelic wrapper Cookbook

[![Apache License 2.0](http://img.shields.io/badge/license-apache%202.0-green.svg)](http://opensource.org/licenses/Apache-2.0)

This cookbook simply loads your [New Relic](https://newrelic.com/) license key from an encrypted data bag and stores it into the appropriate node values.

## Requirements

1. The [newrelic cookbook](https://github.com/escapestudios-cookbooks/newrelic).
2. An encrypted data bag named `api-data` that stores your license in an item named `newrelic` and a field named `license_key`.
3. Copy your data bag secret to the node. Either manually or via knife and the `--secret-file` option on bootstrap.

## Attributes

No attributes are used currently.

## Usage

### newrelic-wrapper::default

Just include the default recipe **before** the newrelic cookbook in your runlist.

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[newrelic-wrapper]",
    "recipe[newrelic]"
  ]
}
```

## Contributing

1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests, ensuring they all pass
6. Submit a Pull Request using Github

## License and Authors

* Freely distributable and licensed under the [Apache 2.0 license](LICENSE).
* Copyright 2014 [Wegtam UG](http://www.wegtam.org)

### Authors:

* [@jan0sch](https://github.com/jan0sch)

