# Document [Heading link](https://docs.airbyte.com/deploying-airbyte/on-kubernetes-via-helm/ "Heading link")

### Creater workspace (services-workspace)
 - đăng nhập kubesphere/services-workspace/app management/app repositories/add
### Creater file values
 - Chọn servicer-workspace/projects/create(new project)/chọn projects/application workloads/app/create/from app template/airbyte/chart files (coppy thành file values)

## Helm install

    helm install airbyte -f (file values) airbyte/airbyte