# Projeto Azure WebApp com MySQL e Keyvaults

## 2 Semestre 2 Checkpoint

### Passo 1 - Clonar o repositório (Valor 0.0)

- Abrir a Console da Nuvem Azure.
- Acessar o Cloud Shell
- Fazer a cópia deste repositório para a máquina da nuvem azure, conforme realizdo anteriormente nas aulas de laboratório.

`git clone https://github.com/rksakai/webapp-azure-2tsc.git`

(evidência: nenhuma)

### Passo 2 - Modificar o nome das variáveis (Valor 1.0)

- Alterar as variáveis babaixo da seguinte forma.
- -- "vault_name" = "kv_ckpt02_rmxxxxxx"
- -- "mysql_name" = "mysql-webapp-ckpt02-rmxxxxxx"
- -- "mysql_database" = "mysql-db-rmxxxxxx"
- -- "webapp_name" = "WebApp-ckpt02-rmxxxxxx"

(evidência: nenhuma)

### Passo 3 - Executar o Terraform para implantar a infraestrutura (Valor 2.0)

- Iniciar o diretório como Terraform
`terraform init`

- Criar o plano de execução
`terraform plan -out webapp.plan`
  
- Aplicar as alterações e criações
`terraform apply`

(evidência: Print da tela com a execução do terraform apply e print da tela com os recursos criados na nuvem Azure)

### Passo 4 - Alterar os scripts para criar mais um banco de dados MySQL (Valor 2.0)

- Alterar o script mysq.tf para adicionar mais um banco de dados na infraestrutura.
- Alterar o script variables.tf para adicionar uma variável com o nome desse novo banco de dados.

(evidência: nenhuma)

### Passo 5 - Executar novamente o Terraform para adicionar o novo banco de dados na infraestrutura (Valor 2.0)

- Criar o plano de execução
`terraform plan -out webapp.plan`
  
- Aplicar as alterações e criações
`terraform apply`

(evidência: Print da tela com a execução do terraform apply e print da tela com os recursos criados na nuvem Azure)

### Passo 6 - Explicar para que serve e onde o trecho de código app_settings do arquivo webapp.tf é aplicado. Pode ser com um simples Print Screen da tela (Valor 2.0)

(evidência: Print da tela onde o trecho de código é usado e explicação da utilização)

### Passo 7 - Efetuar o destroy de toda infraestrutura criada (Valor 1.0)

`terraform destroy`

(evidência: Print da tela com a execução do terraform destroy)
