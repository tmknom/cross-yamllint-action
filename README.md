# cross-yamllint-action

Run [yamllint][yamllint] with configuration shared across repositories.

<!-- actdocs start -->

## Description

This action runs [yamllint][yamllint], a tool designed to lint YAML files.

> [!NOTE]
> yamllint checks not only for syntax validity,
> but also detects potential bugs like key repetition,
> and style problems such as lines length, trailing spaces, indentation, etc.

## Usage

To set up the action, you need to create a YAML file that defines your configurations.
Refer to the detailed configuration syntax provided in the [yamllint documentation][yamllint_docs].

### Configuration URL

```yaml
  steps:
    - name: Cross Yamllint
      uses: tmknom/cross-yamllint-action@v0
      with:
        configuration-url: https://raw.githubusercontent.com/tmknom/cross-yamllint-action/main/configurations/reusable-workflows.yml
```

### Configuration Path

```yaml
  steps:
    - name: Cross Yamllint
      uses: tmknom/cross-yamllint-action@v0
      with:
        configuration-path: .yamllint.yml
```

## Inputs

| Name | Description | Default | Required |
| :--- | :---------- | :------ | :------: |
| configuration-path | The path for the yamllint configurations. | n/a | no |
| configuration-url | The url for the yamllint configurations. | n/a | no |

## Outputs

| Name | Description |
| :--- | :---------- |
| configuration-path | The path for the configuration file to passing yamllint. |

<!-- actdocs end -->

## Permissions

N/A

## FAQ

N/A

## Release notes

See [GitHub Releases][releases].

## License

Apache 2 Licensed. See [LICENSE](LICENSE) for full details.

[yamllint]: https://github.com/adrienverge/yamllint
[yamllint_docs]: https://yamllint.readthedocs.io/en/stable/rules.html
[releases]: https://github.com/tmknom/cross-yamllint-action/releases
