# Custom Cloudflared Helm Chart

This is a simplified Helm chart for deploying a cloudflared agent.

## Why does this exist?

The official Cloudflare Helm chart was found to be outdated and not working as expected in our environment. This chart provides a more straightforward and reliable way to deploy cloudflared.

## Prerequisites

*   Kubernetes 1.12+
*   Helm 3.0+
*   A Cloudflare account
*   A cloudflared token

## Configuration

The following table lists the configurable parameters of the chart and their default values.

| Parameter | Description | Default |
| --- | --- | --- |
| `cloudflare.token` | Your cloudflared token. | `""` |
| `replicaCount` | The number of cloudflared replicas. | `2` |

## Usage

1.  Update the `values.yaml` file with your cloudflared token.
2.  Deploy the chart using Helm:

    ```bash
    helm install <release-name> . --namespace <your-namespace>
    ```

## Example

```bash
helm install cloudflared . --namespace cloudflare
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.