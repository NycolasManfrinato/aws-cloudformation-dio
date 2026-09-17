# AWS CloudFormation - Primeira Stack

Repositorio de documentacao do desafio de codigo "Implementando sua Primeira Stack com AWS CloudFormation", da formacao AWS Cloud Foundations (Digital Innovation One - DIO).

O objetivo deste projeto e reunir anotacoes, insights e boas praticas sobre a criacao de infraestrutura como codigo (IaC) usando o AWS CloudFormation, servindo como material de apoio para estudos e futuras implementacoes.

## Sobre o desafio

O laboratorio tem como proposta implementar a primeira stack com AWS CloudFormation, aplicando na pratica os conceitos vistos nas aulas e documentando a experiencia como material de apoio para estudos futuros.

## Topicos estudados

### 1. O que e o AWS CloudFormation

O AWS CloudFormation e um servico que permite modelar e provisionar recursos da AWS de forma automatizada, usando arquivos de template (JSON ou YAML) que descrevem a infraestrutura desejada como codigo (Infrastructure as Code - IaC).

- Elimina a necessidade de criar recursos manualmente pelo console, reduzindo erros humanos.
- Permite versionar a infraestrutura junto com o codigo da aplicacao, usando ferramentas como o Git.
- Os recursos definidos em um template sao provisionados, atualizados e removidos de forma conjunta, como uma unica unidade chamada Stack.
- Suporta rollback automatico em caso de falha durante a criacao ou atualizacao de uma stack.

### 2. Criando Stacks no AWS CloudFormation

- Uma Stack e criada a partir de um template que define os recursos (EC2, S3, VPC, IAM, entre outros) e seus parametros.
- O processo de criacao passa por etapas: upload do template, definicao de parametros, configuracao de opcoes (tags, permissoes) e revisao antes da execucao.
- Durante a criacao, o CloudFormation gerencia a ordem de criacao dos recursos, respeitando as dependencias declaradas entre eles.
- E possivel atualizar uma stack existente enviando uma nova versao do template; o CloudFormation calcula um changeset mostrando o que sera alterado antes de aplicar.
- Stacks podem ser excluidas de forma integrada, removendo todos os recursos associados automaticamente.

### 3. Criando Stacks de Firewall no CloudFormation

- E possivel usar o CloudFormation para provisionar recursos de seguranca de rede, como Security Groups e Network ACLs, definindo regras de entrada e saida como codigo.
- Essa abordagem garante que as regras de firewall sejam consistentes entre ambientes (desenvolvimento, homologacao, producao), pois seguem o mesmo template.
- Alteracoes nas regras de seguranca podem ser revisadas via changeset antes de serem aplicadas, reduzindo o risco de configuracoes incorretas expondo recursos indevidamente.
- Boas praticas incluem restringir o acesso pelo principio do menor privilegio e documentar o motivo de cada regra liberada no template.

## Principais aprendizados

- Entender o conceito de Infraestrutura como Codigo (IaC) e seus beneficios em relacao a criacao manual de recursos.
- Praticar a criacao, atualizacao e exclusao de uma stack no AWS CloudFormation.
- Compreender como o CloudFormation gerencia dependencias entre recursos e faz rollback em caso de erro.
- Aplicar boas praticas de seguranca ao definir regras de firewall (Security Groups) via template.

## Recursos utilizados

- [Documentacao oficial da AWS - AWS CloudFormation](https://docs.aws.amazon.com/pt_br/AWSCloudFormation/latest/UserGuide/Welcome.html)
- Material complementar do desafio: Implementando sua Primeira Stack com AWS CloudFormation.zip
- Trilha "Formacao AWS Cloud Foundations" - Digital Innovation One (DIO)

## Estrutura do repositorio

- README.md: documentacao e anotacoes do desafio
- templates/: arquivos de template CloudFormation (JSON/YAML) usados na pratica, quando aplicavel
- images/: capturas de tela do console AWS (quando aplicavel)

## Autor

Desafio realizado como parte da formacao AWS Cloud Foundations na DIO (https://www.dio.me/).
