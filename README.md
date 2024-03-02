Exercícios Práticos
Criação de uma infraestrutura simples usando Terraform.
Vou guiá-lo na criação de uma infraestrutura simples usando o Terraform.
Neste exemplo, vamos criar uma instância EC2 na AWS (Amazon Web
Services).
Certifique-se de ter uma conta AWS configurada e as credenciais de acesso
disponíveis. Vamos começar:
1. Instalação do Terraform:
Certifique-se de ter o Terraform instalado em sua máquina. Você pode baixar e
instalar a versão adequada para o seu sistema operacional no site oficial do
Terraform.
https://www.terraform.io/downloads.html

2. Configuração das Credenciais da AWS:
Configure suas credenciais da AWS. Você pode fazer isso definindo variáveis de
ambiente AWS_ACCESS_KEY_ID e AWS_SECRET_ACCESS_KEY, ou
configurando um perfil no arquivo ~/.aws/credentials.

3. Crie um Diretório de Trabalho:
Crie um novo diretório para o seu projeto Terraform e navegue até ele.

4. Crie Arquivos de Configuração:
Crie os seguintes arquivos de configuração no diretório do seu projeto:

provider "aws" {
    region = "us-east-1"
}

resource "aws_instance" "minha-instancia" {
    ami = "ami-0440d3b780d96b29d"
    instance_type = "t2.micro"
}

5. Inicialize o Diretório do Terraform:
Execute o comando terraform init para inicializar o diretório do Terraform. Isso
baixará os plugins necessários para o provedor AWS e configurará o ambiente.

6. Visualize o Plano:
Execute o comando terraform plan para visualizar o plano de execução. Isso
mostrará quais recursos serão criados, modificados ou removidos.

7. Aplique as Alterações:
Se o plano estiver correto, execute o comando terraform apply para aplicar as
alterações e criar a infraestrutura.

8. Verifique a Infraestrutura:
Após a conclusão, verifique se a instância EC2 foi criada na AWS.

9. Destrua a Infraestrutura (Opcional):
Quando não precisar mais da infraestrutura, você pode destrui-la executando o
comando terraform destroy. Isso removerá todos os recursos provisionados pelo
Terraform.
Este é apenas um exemplo simples de como criar uma infraestrutura usando o
Terraform. Você pode expandir e personalizar isso conforme necessário para
atender aos requisitos do seu projeto. Certifique-se sempre de entender o que o
seu código está fazendo e revise cuidadosamente antes de aplicar mudanças na
infraestrutura em produção.
Agora, teste o quanto quiser, valide conceitos e faça testes, mas não
esqueça de destruir tudo antes de sair!!!