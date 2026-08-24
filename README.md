# Pipeline CI/CD com Python e GitHub Actions

## Sobre o projeto

Este projeto demonstra a utilização de Continuous Integration (CI) e Continuous Delivery (CD) utilizando Python, pytest e GitHub Actions.

A aplicação possui uma calculadora simples com operações de:

- Soma
- Subtração
- Multiplicação
- Divisão

Também existem testes automatizados para verificar o funcionamento das operações.

## 1. O que representa a etapa de CI neste projeto?

A etapa de Continuous Integration representa a integração e validação automática do código.

Sempre que ocorre um push na branch main ou um pull request para a branch main, o GitHub Actions configura o ambiente Python, instala as dependências e executa os testes automatizados.

O objetivo é identificar defeitos antes que o código seja disponibilizado para entrega.

## 2. O que impede a execução do Continuous Delivery quando existe um defeito?

O job Continuous Delivery possui a configuração:

needs: ci

Isso significa que o job de Continuous Delivery depende da conclusão bem-sucedida do job Continuous Integration.

Se algum teste falhar, o job CI falha e o Continuous Delivery não é executado.

## 3. Qual seria a próxima etapa necessária para transformar este pipeline em Continuous Deployment?

Seria necessário adicionar uma etapa responsável por realizar automaticamente a implantação do artefato em um ambiente de destino, como um servidor ou serviço de hospedagem.

Dessa forma, após os testes serem aprovados e o artefato ser gerado, o pipeline poderia realizar o deploy automaticamente.
