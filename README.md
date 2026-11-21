# kstone

Kubernetes operators need a clear way to manage etcd clusters, inspect their health, and protect their data. kstone brings these operational tasks into one platform for existing and newly created etcd clusters.

**kstone combines cluster management, monitoring, backup, inspection, and a web console in one project.**

## Features

- Register existing etcd clusters and create new clusters.
- Monitor etcd with Prometheus and view its Grafana panels.
- Back up data to object storage at minute-level intervals or use an etcd learner for real-time backup.
- Inspect data consistency, cluster health, hot write requests, and resource-object counts.
- View etcd data through the web console.
- Migrate data and run intelligent diagnosis where those capabilities are available in the project roadmap.

## Installation

Clone the repository and build its Go packages:

```sh
git clone https://github.com/kstone-io/kstone.git
cd kstone
go build ./...
make
```

For a Kubernetes installation, see the [Helm installation documents](charts). The repository also contains additional [documentation](docs).

## Usage

After building the project, inspect the available command-line options before starting a local instance:

```sh
./kstone --help
```

Deploy kstone in Kubernetes with the project Helm charts, then register an etcd cluster through the management interface. Configure Prometheus monitoring, backup settings, and inspection policies according to the deployment documentation.

## License

kstone is licensed under the Apache License 2.0. See [LICENSE](LICENSE) for the full license text.

This standalone project is based on [kstone-io/kstone](https://github.com/kstone-io/kstone), with attribution retained under the Apache-2.0 license.
