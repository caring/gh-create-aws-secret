# gh-create-aws-secret

## Description

This GitHub Action provisions an AWS Secret in Secret Manager. It checks if the secret already exists and creates a new one if it doesn't.

## Inputs

| Name                  | Description                                                  | Required |
| --------------------- | ------------------------------------------------------------ | -------- |
| `name`             | The name of the Secret.                | ✔        |

## Outputs

This action doesn't have any outputs.

## Example Usage

```yaml
jobs:
  provision-aws-secret:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Provision AWS Secret
        id: secret
        uses: caring/gh-create-aws-secret@v1.0.0
        with:
          name: some-secret
```

This action will provision a Secret

## License

This project is licensed under the [MIT License](LICENSE).

## Author

Written by the DevOps Team.
