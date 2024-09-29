# Azure Resource Naming Standards

### Key Elements

| Element       | Description                       | Examples                                    |
|---------------|-----------------------------------|---------------------------------------------|
| Resource Type | Abbreviations for resource types  | `vm` (Virtual Machine), `rg` (Resource Group), `st` (Storage Account), `sql` (SQL Database), `app` (App Service), `func` (Function App), `kv` (Key Vault), `nsg` (Network Security Group), `vnet` (Virtual Network), `pip` (Public IP Address), `lb` (Load Balancer), `agw` (Application Gateway), `cosmos` (Cosmos DB), `redis` (Redis Cache), `log` (Log Analytics Workspace) |
| Environment   | Indicates the environment         | `prod` (Production), `dev` (Development), `test` (Testing), `stage` (Staging) |
| Region        | Azure region codes                | `eus` (East US), `wus` (West US), `neu` (North Europe), `weu` (West Europe), `sea` (Southeast Asia), `aue` (Australia East), `jpe` (Japan East) |
| Instance      | Unique identifier or instance number | Use a numeric value or a short identifier |

### Examples

| Resource Type       | Example Naming Convention       | Example Name         |
|---------------------|---------------------------------|----------------------|
| Virtual Machine     | `vm-[environment]-[region]-[instance]` | `vm-prod-eus-01`     |
| Resource Group      | `rg-[environment]-[region]-[instance]` | `rg-dev-weu-01`      |
| Storage Account     | `st-[environment]-[region]-[instance]` | `st-test-sea-01`     |
| SQL Database        | `sql-[environment]-[region]-[instance]` | `sql-stage-aue-01`   |
| App Service         | `app-[environment]-[region]-[instance]` | `app-prod-neu-01`    |
| Function App        | `func-[environment]-[region]-[instance]` | `func-dev-weu-01`    |
| Key Vault           | `kv-[environment]-[region]-[instance]` | `kv-prod-eus-01`     |
| Network Security Group | `nsg-[environment]-[region]-[instance]` | `nsg-dev-wus-01`     |
| Virtual Network     | `vnet-[environment]-[region]-[instance]` | `vnet-test-sea-01`   |
| Public IP Address   | `pip-[environment]-[region]-[instance]` | `pip-stage-aue-01`   |
| Load Balancer       | `lb-[environment]-[region]-[instance]` | `lb-prod-neu-01`     |
| Application Gateway | `agw-[environment]-[region]-[instance]` | `agw-dev-weu-01`     |
| Cosmos DB           | `cosmos-[environment]-[region]-[instance]` | `cosmos-prod-eus-01` |
| Redis Cache         | `redis-[environment]-[region]-[instance]` | `redis-dev-wus-01`   |
| Log Analytics Workspace | `log-[environment]-[region]-[instance]` | `log-test-sea-01`    |

## Conclusion
Following these naming standards will help ensure consistency and clarity across all Azure resources. Make sure to adhere to these guidelines for all new resources.