## このリポジトリについて

このリポジトリは、[sinsoku/amazon-ecs-run-task-definition](https://github.com/sinsoku/amazon-ecs-run-task-definition) をforkしたものです。


## Amazon ECS "Run Task Definition" Action for GitHub Actions

Run an Amazon ECS task definition on the same configuration as the existing ECS service.

## Usage

Marketplaceに登録していないので、checkoutして利用してください。

```yaml
    - name: Checkout medpeer-dev/amazon-ecs-run-task-definition
      uses: actions/checkout@v4
      with:
        repository: medpeer-dev/amazon-ecs-run-task-definition
        path: amazon-ecs-run-task-definition
    - name: Run a task on Amazon ECS
      uses: ./amazon-ecs-run-task-definition
      with:
        task-definition: foo:1
        container: my-container
        command: |
          echo
          "Hello, World"
        service: my-service
        cluster: my-cluster
        wait-for-stopped: true
```

See [action.yml](action.yml) for the full documentation for this action's inputs and outputs.
