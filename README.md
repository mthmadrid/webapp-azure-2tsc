# Projeto Azure WebApp com MySQL e Keyvaults

## 2 Semestre 2 Checkpoint

### Passo 1 - Clonar o repositório (Valor 0.0)

- Abrir a Console da Nuvem Azure.
- Acessar o Cloud Shell
- Fazer a cópia deste repositório para a máquina da nuvem azure, conforme realizdo anteriormente nas aulas de laboratório.

`git clone https://github.com/rksakai/webapp-azure-2tsc.git`


### Passo 2 - Modificar o nome das variáveis (Valor 2.0)

- Alterar as variáveis babaixo da seguinte forma.
- -- "vault_name" = "kv_ckpt02_rmxxxxxx"
- -- "mysql_name" = "mysql-webapp-ckpt02-rmxxxxxx"
- -- "mysql_database" = "mysql-db-rmxxxxxx"
- -- "webapp_name" = "WebApp-ckpt02-rmxxxxxx"

### Passo 3 - Executar o Terraform para implantar a infraestrutura (Valor 3.0)

- Iniciar o diretório como Terraform
`terraform init`

- Criar o plano de execução
`terraform plan -out webapp.plan`
  
- Aplicar as alterações e criações
`terraform apply`

### Passo 4 - Alterar os scripts para criar mais um banco de dados MySQL (Valor 2.0)

- Alterar o script mysq.tf para adicionar mais um banco de dados na infraestrutura.
- Alterar o script variables.tf para adicionar uma variável com o nome desse novo banco de dados.

### Passo 5 - Executar novamente o Terraform para adicionar o novo banco de dados na infraestrutura

- Criar o plano de execução
`terraform plan -out webapp.plan`
  
- Aplicar as alterações e criações
`terraform apply`

### Passo 6 - Explicar onde o trecho de código é aplicado. Pode ser com um simples Print Screen da tela.

`# app_settings como argumento de nível superior
  app_settings = {
    KEY_VAULT_URL                 = azurerm_key_vault.vault.vault_uri
    DB_HOST                       = azurerm_mysql_flexible_server.mysql.fqdn
    DB_NAME                       = azurerm_mysql_flexible_database.mysql_database.name
    DB_USER                       = var.mysql_admin
    DB_PORT                       = "3306"
    SECRET_KEY                    = "@Microsoft.KeyVault(VaultName=${azurerm_key_vault.vault.name};SecretName=${azurerm_key_vault_secret.my_password.name})"
    SCM_DO_BUILD_DURING_DEPLOYMENT = "true"  # No Terraform sempre como string
    MYSQL_CHARSET                 = "utf8mb4"
    MYSQL_COLLATION               = "utf8mb4_unicode_ci"
  }`
