# Development environment for Cognite Data Fusion Spark DataSource


## Requeriments

- Container engine like docker or podman
- Visual studio code with Dev Containers extension


## How to use

- Clone this repo
- Setup your environment variables en `.devcontainer/devcontainer.json`
  - Default values are from [Cognite Spark data source learning](https://learn.cognite.com/path/data-engineer-basics-integrations/cognite-spark-data-source/).
  - For testing you can create a CLIENT_SECRET from [generate client secret](https://learn.cognite.com/path/data-engineer-basics-integrations/cognite-spark-data-source/1371418) in Cognite Spark data source learning.
- Open it with Visual Studio Code
- Command palette > `Dev Containers: Rebuid and Reopen in Container`.
- Use the [example notebook](example_oauth.ipynb) as a start point.