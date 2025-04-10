## About

GitHub Action to connect a runner to a Headscale server using the Tailscale CLI. This action installs and configures the necessary tools to establish a secure connection to a Headscale server.

## Usage

### Quick start

```yaml
name: Connect to Headscale

on:
  push:

jobs:
  connect:
    runs-on: ubuntu-latest
    steps:
      - name: Connect to Headscale
        uses: candidco/headscale-connect-action@v1
        with:
          headscale-cli-address: 'your-headscale-server-address'
          headscale-cli-api-key: 'your-api-key'
```

## Customizing

### inputs

The following inputs can be used as `step.with` keys:

| Name                           | Type   | Default             | Description                                                                                   |
|--------------------------------|--------|---------------------|-----------------------------------------------------------------------------------------------|
| `headscale-cli-address`        | String |                     | The address of the Headscale CLI.                                                             |
| `headscale-cli-api-key`        | String |                     | The API key for the Headscale CLI.                                                            |
| `headscale-user`               | String | `github-actions`    | The user to create or use in Headscale.                                                       |
| `headscale-preauthkey-expiration` | String | `30m`               | The expiration time for the preauth key.                                                      |
| `headscale-version`            | String | `0.25.1`            | The version of Headscale to install.                                                          |
| `headscale-os-arch`            | String | `linux_amd64`       | The OS and architecture for the Headscale binary.                                             |

## Outputs

This action does not produce any outputs.

## Contributing

Want to contribute? Awesome! Contributions are welcome. Please check the [CONTRIBUTING.md](/.github/CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the Apache-2.0 License. See the [LICENSE](LICENSE) file for more details.
