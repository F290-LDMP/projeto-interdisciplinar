# Modelo de entrega — Projeto Interdisciplinar

[Voltar ao enunciado](../README.md)

Copie este modelo para o repositório da equipe e preencha os campos. Ele organiza as evidências; não cria requisitos adicionais ao enunciado. Caso o código esteja dividido em vários repositórios, mantenha um documento de entrega que conecte todos eles.

## 1. Identificação

- **Nome do projeto:** preencher.
- **Problema e público atendido:** preencher.
- **Versão final — tag ou commit:** preencher.
- **Data de entrega:** preencher. Prazo final: 28/11/2026.

| Integrante — até cinco | Usuário GitHub ou referência de contribuição | Responsabilidades |
|---|---|---|
| Preencher | Preencher | Preencher |

Não inclua CPF, documentos pessoais, endereço ou outros dados desnecessários à avaliação.

## 2. Origem e evolução

- **Projeto web do quarto semestre:** link.
- **Versão de origem:** commit ou tag.
- **O que existia antes:** descrever.
- **O que foi reaproveitado:** descrever.
- **O que foi alterado ou acrescentado:** descrever.
- **Limites do MVP entregue:** descrever.

## 3. Componentes e tecnologias

| Componente | Tecnologia | Repositório/caminho | Como executar/acessar |
|---|---|---|---|
| Aplicação web | Preencher | Link/caminho | Comando e endereço |
| Aplicativo Flutter | Flutter; destino móvel escolhido | Link/caminho | Comando/dispositivo de demonstração |
| API/backend | Preencher | Link/caminho | Comando e endereço |
| Backoffice | Web ou desktop; tecnologia | Link/caminho | Comando e endereço |
| Broker | Preencher | Configuração | Comando/endereço |
| Consumidor | Preencher | Link/caminho | Comando |
| Persistência | Preencher | Configuração | Comando |

Um mesmo projeto pode cumprir mais de uma responsabilidade. Identifique isso sem criar componentes artificiais.

## 4. Jornada integrada

Descreva um fluxo completo, indicando:

1. Ação do usuário ou administrador.
2. Chamada à API e validações relevantes.
3. Informação persistida.
4. Mensagem publicada e seu destino.
5. Consumidor responsável e efeito produzido.
6. Forma de observar o resultado no backoffice e/ou aplicativo.
7. Comportamento em caso de falha.

Acrescente um diagrama de componentes ou sequência, em Mermaid, imagem ou representação textual legível.

## 5. Contrato da API

Informe o link da documentação ou descreva aqui as operações utilizadas pelo MVP.

| Operação | Entrada | Resultado esperado | Erros relevantes |
|---|---|---|---|
| Preencher | Preencher | Preencher | Preencher |

Explique como os clientes acessam a API e como o acesso administrativo é controlado. Não versione credenciais reais.

## 6. Contrato de mensageria

- **Finalidade da funcionalidade assíncrona:** preencher.
- **Broker:** preencher.
- **Produtor:** preencher.
- **Fila/tópico/canal e regra de roteamento:** preencher conforme a tecnologia.
- **Consumidor:** preencher.
- **Relação com o backoffice:** preencher.
- **Exemplo de payload:** inserir mensagem fictícia do domínio.
- **Identificador para acompanhar a operação:** preencher.
- **Quando o processamento é considerado concluído:** preencher.
- **O que ocorre com o consumidor indisponível:** preencher.
- **Tratamento de falhas e possibilidade de duplicação:** preencher.
- **Como acompanhar ou recuperar o processamento:** preencher.

Declare as garantias efetivamente implementadas. Se não há retry, DLQ ou deduplicação, descreva a limitação sem apresentá-los como disponíveis.

## 7. Reprodução do ambiente

- Pré-requisitos e versões.
- Arquivo de exemplo das variáveis de ambiente, sem segredos reais.
- Preparação da persistência e dados iniciais.
- Comandos e ordem de inicialização de API, broker, consumidor e interfaces.
- Procedimento para acesso de demonstração, usando dados fictícios.
- Comandos para executar os testes ou verificações.

O avaliador deve conseguir seguir as instruções sem depender de configurações não documentadas na máquina da equipe.

## 8. Evidências de atendimento

| Requisito | Onde está implementado | Como demonstrar | Evidência |
|---|---|---|---|
| R01 — Evolução do projeto web | Preencher | Preencher | Link/captura/descrição |
| R02 — Aplicativo Flutter móvel | Preencher | Preencher | Link/captura/descrição |
| R03 — API funcional | Preencher | Preencher | Link/captura/descrição |
| R04 — Broker com consumo real | Preencher | Preencher | Log/mensagem/resultado |
| R05 — Backoffice integrado | Preencher | Preencher | Link/captura/descrição |

## 9. Verificações e resultados

| Cenário | Passos/comando | Resultado esperado | Resultado observado |
|---|---|---|---|
| Jornada principal | Preencher | Preencher | Preencher |
| Entrada inválida | Preencher | Preencher | Preencher |
| Falha na integração assíncrona | Preencher | Preencher | Preencher |

Informe quais verificações são automatizadas e quais foram executadas manualmente. Caso a equipe declare TDD, referencie a evidência do ciclo adotado.

## 10. Contribuições e portfólio

| Integrante | Contribuição | Evidência contextualizada |
|---|---|---|
| Preencher | Código, testes, revisão, documentação, design ou gestão | Commits, PRs, issues ou outros registros |

- **Organização das tarefas:** link do quadro/backlog ou descrição equivalente.
- **Registro no portfólio acadêmico:** link ou indicação de onde o resultado será incorporado.
- **Aprendizados e decisões relevantes:** preencher.

## 11. Limitações e próximos passos

Liste o que não foi implementado, os problemas conhecidos e as melhorias futuras. Diferencie claramente o que está funcionando do que permanece planejado.
