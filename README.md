# Projeto Azure WebApp com MySQL e Keyvaults

## 2 Semestre 2 Checkpoint

### Passo 1 - Clonar o repositório

- Abrir a Console da Nuvem Azure.
- Acessar o Cloud Shell
- Fazer a cópia deste repositório para a máquina da nuvem azure, conforme realizdo anteriormente nas aulas de laboratório.

`git clone https://github.com/rksakai/webapp-azure-2tsc.git`


### Passo 2 - Modificar o nome das variáveis

- Alterar as variáveis babaixo da seguinte forma.
- -- "vault_name" = "kv_ckpt02_<rmxxxxxx>"
- -- "mysql_name" = "mysql-webapp-ckpt02-<rmxxxxxx>"
- -- "mysql_database" = "mysql-db-<rmxxxxxx>"
- -- "webapp_name" = "WebApp-ckpt02-<rmxxxxxx>"

### Passo 3 - Executar o Terraform para implantar a infraestrutura

- Iniciar o diretório como Terraform
`terraform init`

- Criar o plano de execução
`terraform plan -out webapp.plan`
  
- Aplicar as alterações e criações
`terraform apply`
