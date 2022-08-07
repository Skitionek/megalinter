<!-- markdownlint-disable MD013 -->
<!-- Generated by .automation/build.py, please do not update manually -->
<!-- plugins-section-start -->

# Plugins

For security reasons, we try to embed in MegaLinter only linters that are widely adopted by open-source community.

But any linter can be callable within MegaLinter thanks to the plugin mechanism !

## Use plugins

Add plugin URLs in `PLUGINS` property of `.mega-linter.yml`. URLs must either begin with "https://" or take the form of "file://\<path\>", where \<path\> points to a valid plugin descriptor file.

> Note: Both \<path\> and the default mount directory (/tmp/lint/\<path\>) will be checked for a valid descriptor.

### Example

```yaml
PLUGINS:
  - https://raw.githubusercontent.com/oxsecurity/megalinter/main/.automation/test/mega-linter-plugin-test/test.megalinter-descriptor.yml
  - https://raw.githubusercontent.com/cookiejar/mega-linter-plugin-cookietemple/main/cookietemple.megalinter-descriptor.yml
  - file://.automation/test/mega-linter-plugin-test/test.megalinter-descriptor.yml
```

## Plugins Catalog

* [jupyfmt](https://github.com/kpj/jupyfmt): The uncompromising Jupyter notebook formatter ([usage](https://github.com/kpj/jupyfmt#mega-linter-integration))
* [nitpick](https://github.com/andreoliwa/nitpick): Command-line tool and flake8 plugin to enforce the same settings across multiple language-independent projects. ([usage](https://github.com/andreoliwa/nitpick#run-as-a-megalinter-plugin))


Submit a PR if you want your plugin to appear here :)

## Create plugins

You can implement your own descriptors and load them as plugins during MegaLinter runtime

- Descriptor format is exactly the same than [MegaLinter embedded ones](https://github.com/oxsecurity/megalinter/tree/main/megalinter/descriptors) ([see json schema documentation](https://megalinter.github.io/json-schemas/descriptor.html))
- Plugins descriptor files must be named **\*\*.megalinter-descriptor.yml** and respect [MegaLinter Json Schema](https://github.com/oxsecurity/megalinter/blob/main/megalinter/descriptors/schemas/megalinter-descriptor.jsonschema.json)
- Plugins must be hosted in a url containing **\*\*/mega-linter-plugin-\*\*/**
- File URLs must conform to the same directory and file naming criteria as defined above.

### Limitations

- For now, the only `install` attributes managed are `dockerfile` instructions starting by `RUN`


<!-- plugins-section-end -->