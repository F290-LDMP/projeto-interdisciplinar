# Projeto Interdisciplinar — Laboratório de Desenvolvimento Multiplataforma

Orientações para a entrega final da disciplina **Laboratório de Desenvolvimento Multiplataforma**, do curso de Desenvolvimento de Software Multiplataforma da Fatec Araras.

| Item | Definição |
|---|---|
| Organização da disciplina | [F290-LDMP](https://github.com/F290-LDMP) |
| Equipes | Até **5 integrantes** |
| Entrega final | **28 de novembro de 2026** — horário e canal de submissão a serem informados pelo docente |
| Ponto de partida | Projeto web desenvolvido no **quarto semestre** |
| Plataformas obrigatórias | Aplicação **web** e aplicativo **móvel em Flutter** |
| Administração | MVP de **backoffice web ou desktop**, com tecnologia livre |
| Integração | **API** e pelo menos uma funcionalidade com **consumo real de Message Broker** |
| Backend | Linguagem e framework livres; Spring Boot não é obrigatório |

Os requisitos de escopo deste enunciado foram definidos pelo docente. A [rubrica de avaliação](docs/CRITERIOS-DE-AVALIACAO.md) apresenta uma **proposta de critérios e pesos**, a ser ratificada pelo docente antes de sua aplicação. Não estabelece nota mínima, penalidades ou regras de aprovação adicionais às da disciplina.

## 1. Propósito do projeto

Evoluir um sistema web já desenvolvido para uma solução integrada, acessível por diferentes plataformas. O objetivo é demonstrar que uma mesma necessidade de negócio pode ser atendida por interfaces distintas, compartilhando dados e regras por uma API e incorporando comunicação assíncrona em uma funcionalidade relevante.

O MVP deve ser pequeno, mas funcional: uma pessoa deve conseguir concluir uma jornada real, e a equipe deve conseguir explicar e demonstrar o caminho dos dados entre as aplicações. Telas isoladas, chamadas simuladas e componentes apenas instalados não demonstram essa integração.

O trabalho não exige reproduzir a arquitetura do workshop. Microserviços com Java e Spring Boot são a referência prática da disciplina; a avaliação deve considerar os resultados e as evidências, respeitando a liberdade de linguagem e framework da equipe.

## 2. Fundamentação e alinhamento ao PPC

A referência institucional é o [PPC indicado pelo docente](https://bkpsitecpsnew.blob.core.windows.net/uploadsitecps/sites/19/2026/07/sl_PPC_DesenvolvimentoSoftwareMultiplataforma-6a469a7083e52.pdf#page=61), na seção **Laboratório de Desenvolvimento Multiplataforma**, página impressa **60** — página **61** do PDF. A capa identifica a edição de Franca, de 2021; este é o arquivo fornecido como referência para a atividade.

| Diretriz do PPC, em síntese | Evidência prevista nesta atividade |
|---|---|
| Integração de engenharia de software, programação e gestão | Escopo do MVP, decisões de arquitetura e organização das tarefas |
| Integração de interfaces e backend em diferentes plataformas | Web, aplicativo Flutter e backoffice conectados à API |
| Intercomunicação por mensageria e uso de brokers | Publicação, consumo e efeito observável em uma funcionalidade |
| Testes/TDD e versionamento | Evidências de verificação e histórico Git; registrar o ciclo TDD quando utilizado |
| Aprendizagem por projetos e gestão ágil | Evolução incremental e acompanhamento do trabalho da equipe |
| Apresentação de resultados e portfólio | Demonstração, documentação e referências do projeto no portfólio |
| Trabalho colaborativo | Responsabilidades e contribuições identificáveis |

**Recorte da entrega:** Desktop é opcional. IoT, armazenamento em grande escala e Data Streaming, também abordados no PPC, não foram definidos como requisitos mínimos desta entrega. O projeto evidencia o recorte estabelecido para esta atividade; não pretende comprovar, isoladamente, toda a ementa.

O PPC remete ao Manual de Projetos Interdisciplinares da CESU. Esse manual não foi fornecido nesta elaboração; portanto, este enunciado não atribui a ele tecnologias, quantidades de integrantes, datas ou pesos de avaliação. Eventuais disposições complementares deverão ser conferidas com o docente.

## 3. Requisitos obrigatórios e critérios de aceite

### R01 — Evoluir o projeto web do quarto semestre

A equipe deve utilizar o projeto web desenvolvido no quarto semestre como base, preservando seu problema de negócio e apresentando sua evolução.

**Critérios de aceite:**

- Identificar o projeto de origem e fornecer o link do repositório e uma referência da versão anterior, como commit ou tag.
- Explicar o que foi reaproveitado, adaptado e acrescentado nesta disciplina.
- Demonstrar uma aplicação web funcional vinculada ao mesmo domínio e aos dados da solução final.
- Mostrar sua integração com a API no recorte escolhido, sem depender apenas de dados fixos na interface.

O backoffice pode fazer parte do próprio site: não é obrigatório criar outro repositório ou outra aplicação web para a administração. Deve existir uma função administrativa distinguível da jornada do usuário do aplicativo.

### R02 — Criar um aplicativo cliente Flutter

A equipe deve entregar um aplicativo móvel em Flutter que consuma a API do projeto. É aceito um MVP, desde que contenha uma jornada de negócio completa.

**Critérios de aceite:**

- Executar em pelo menos um destino móvel, em dispositivo ou emulador/simulador compatível. Uma versão exclusivamente Flutter Web não substitui a entrega móvel.
- Realizar consultas e/ou operações pertinentes ao domínio por meio da API.
- Apresentar dados persistidos ou resultados reais do backend, incluindo ao menos um estado de carregamento, ausência de dados ou erro de comunicação demonstrável.
- Mostrar uma informação criada, alterada ou processada em outra parte da solução. A coerência deve ser verificável entre as plataformas.

Não é exigida publicação em loja de aplicativos nem suporte simultâneo a Android e iOS.

### R03 — Disponibilizar o backend como API

O backend deve oferecer uma API consumível pelo aplicativo e pelo backoffice. Pode ser uma adaptação do backend existente, um módulo acrescentado ao projeto ou uma reorganização justificada.

**Critérios de aceite:**

- Disponibilizar operações suficientes para a jornada do MVP, com dados e regras de negócio processados no backend.
- Persistir as informações necessárias e validar as entradas relevantes.
- Documentar operações, parâmetros, formatos de dados e respostas de sucesso e erro.
- Permitir demonstrar o compartilhamento dos dados entre as interfaces por meio da API.

REST/HTTP é uma opção recomendada, mas outra abordagem de API pode ser utilizada se estiver documentada. OpenAPI/Swagger, schema GraphQL ou documentação equivalente em Markdown são formas possíveis de descrever o contrato.

A linguagem, o framework e a tecnologia de persistência são livres. Não é obrigatório dividir o backend em microserviços. Uma organização modular é aceita se demonstrar a integração exigida.

### R04 — Incorporar Message Broker em uma funcionalidade real

Pelo menos uma funcionalidade deve publicar uma mensagem em um broker, consumi-la em um componente da solução e produzir um efeito de negócio observável.

**Critérios de aceite:**

- Identificar quem produz e quem consome a mensagem, o broker escolhido e a finalidade da comunicação assíncrona.
- Documentar fila, tópico ou canal e o formato da mensagem, conforme a tecnologia utilizada.
- Demonstrar o consumo real e a mudança de estado, processamento ou resultado produzido pelo consumidor.
- Apresentar evidência que conecte a ação de origem à mensagem e ao efeito: por exemplo, identificador da operação, logs e dados resultantes.
- Explicar o comportamento quando o consumidor ou outra dependência estiver indisponível e como verificar ou recuperar o processamento no MVP.

RabbitMQ é a referência das aulas, mas outro Message Broker pode ser utilizado. A equipe deve justificar sua escolha e demonstrar suas características sem prometer garantias que não implementou.

**Não atendem ao requisito:** apenas subir o container do broker, abrir seu painel, declarar uma fila sem consumidor ou registrar um texto de “mensagem enviada” sem publicação e consumo reais.

Retries, dead-letter queue, deduplicação e padrões como Outbox são possíveis evoluções. Não são todos obrigatórios; a solução deve declarar suas garantias e limitações e tratar as falhas compatíveis com o fluxo escolhido.

### R05 — Entregar um MVP de backoffice integrado

A solução deve possuir um portal ou módulo administrativo que permita gerenciar informações do domínio e que participe do fluxo integrado com a API e a mensageria.

**Critérios de aceite:**

- Disponibilizar ao menos uma operação administrativa relevante, como cadastrar conteúdo, gerenciar pedidos, aprovar solicitações ou acompanhar processamento.
- Consumir a API para consultar e/ou alterar informações do projeto.
- Demonstrar uma informação administrada que alimente o aplicativo ou um resultado de processamento assíncrono que possa ser acompanhado na administração.
- Identificar a funcionalidade da solução em que o broker é efetivamente consumido e sua relação com a operação administrativa.

O backoffice pode ser **web ou desktop**, em Flutter ou outra tecnologia. **Desktop é opcional.**

É aceito que o consumidor do broker seja um **serviço backend do backoffice ou da solução integrada**, e que a interface administrativa acesse seus resultados pela API. Não é necessário que a interface do navegador ou o aplicativo desktop se conecte diretamente ao broker.

Não é obrigatório criar uma segunda funcionalidade de mensageria para cumprir R05: o fluxo de R04 pode atender aos dois requisitos, desde que sua relação com o backoffice seja demonstrada.

## 4. Exemplo de integração aceitável

Considere um sistema de catálogo e solicitações:

1. Um administrador cadastra ou atualiza um item pelo backoffice, utilizando a API.
2. O aplicativo Flutter consulta os itens disponíveis na mesma API.
3. Um usuário registra uma solicitação no aplicativo.
4. O backend publica uma mensagem relacionada à solicitação.
5. Um consumidor processa a mensagem e registra o resultado.
6. O backoffice consulta pela API a situação processada; o aplicativo também pode acompanhar o resultado.

Este exemplo é ilustrativo. A equipe deve adaptar a jornada ao projeto que trouxe do quarto semestre; não é necessário transformar todo domínio em pedidos ou catálogo.

```text
Aplicação web ───────┐
                    │
Aplicativo Flutter ──┼── API / regras de negócio ── Persistência
                    │              │                   ▲
Backoffice ──────────┘          Publicador               │
                                   │                   │
                              Message Broker           │
                                   │                   │
                               Consumidor ──────────────┘

O consumidor pode pertencer ao backend do backoffice ou à solução integrada.
As interfaces acompanham os resultados pela API.
```

O diagrama representa responsabilidades, não uma quantidade obrigatória de processos, bancos ou repositórios.

## 5. Organização, qualidade e segurança

Para tornar a solução avaliável e reproduzível, a equipe deve:

- Manter o código sob controle de versão e informar as responsabilidades dos integrantes.
- Organizar um backlog ou registro equivalente com o que foi planejado, concluído e não entregue.
- Documentar arquitetura, tecnologias, configurações necessárias e a sequência de inicialização.
- Separar credenciais do código versionado e fornecer exemplos de configuração sem segredos reais.
- Demonstrar como o acesso administrativo é controlado e como entradas relevantes são validadas. O mecanismo é livre; Keycloak não é obrigatório.
- Utilizar dados fictícios ou autorizados na apresentação, evitando expor informações pessoais e credenciais nas evidências.
- Apresentar testes ou verificações reproduzíveis do caminho principal, de uma entrada inválida e de uma condição de falha da integração assíncrona. Testes automatizados são recomendados; somente possuir testes não comprova adoção de TDD.
- Registrar limitações conhecidas do MVP, especialmente em operações assíncronas, duplicação de mensagens e falhas parciais.

Não são exigidos provedor de nuvem pago, publicação em loja ou ferramentas comerciais. Execução local é aceita, desde que possa ser reproduzida a partir das instruções fornecidas.

## 6. Entregáveis

Até **28/11/2026**, a equipe deve disponibilizar:

1. **Código-fonte:** links dos repositórios do site, aplicativo, backend e backoffice, ou os caminhos correspondentes em um monorepo. Identificar a versão final avaliada por tag ou commit.
2. **Documento de entrega em Markdown:** integrantes, projeto de origem, problema, escopo do MVP, tecnologias, requisitos atendidos e limitações.
3. **Guia de execução:** pré-requisitos, configuração de ambiente, inicialização da API, persistência, broker, consumidor e interfaces; dados iniciais e acesso de demonstração, quando necessários.
4. **Arquitetura e contratos:** diagrama dos componentes, documentação da API, mensagem de exemplo e descrição do fluxo assíncrono.
5. **Evidências:** demonstração da jornada integrada e dos testes/verificações, com resultados observáveis. Capturas, logs e gravação podem complementar a demonstração; não substituem a entrega funcional.
6. **Contribuições e portfólio:** descrição objetiva da participação de cada integrante, com referências ao trabalho, e indicação de como o resultado será incorporado ao portfólio acadêmico.

Utilize o [modelo de entrega](docs/MODELO-DE-ENTREGA.md). Ele pode ser copiado para o repositório da equipe, sem necessidade de migrar o código para este repositório de orientações.

O docente informará o canal e o horário-limite da submissão, além da organização das apresentações. Não há horário de corte presumido neste documento.

## 7. Apresentação final

Sugestão de apresentação de **10 a 15 minutos por equipe**, sujeita à organização da turma pelo docente:

| Momento | Evidência esperada |
|---|---|
| Contexto | Problema atendido e evolução do projeto do quarto semestre |
| Visão da solução | Plataformas, API, persistência, broker e consumidor |
| Demonstração | Jornada completa, incluindo operação administrativa e aplicativo Flutter |
| Mensageria | Mensagem publicada, consumo e efeito observável |
| Verificação | Um cenário de erro ou indisponibilidade e a explicação do comportamento |
| Fechamento | Limitações do MVP e participação dos integrantes |

Todos os integrantes devem estar preparados para explicar suas contribuições e como elas se conectam à solução. A contagem de commits, isoladamente, não mede contribuição.

## 8. Acompanhamento sugerido até a entrega

Os marcos abaixo são **orientações de organização**, não novos prazos de submissão. A data final confirmada é 28/11/2026.

| Etapa | Resultado a buscar |
|---|---|
| Definição do MVP | Equipe, projeto de origem, jornada e arquitetura delimitados |
| Primeira integração | API e Flutter trocando dados reais; operação administrativa disponível |
| Fluxo assíncrono | Publicação, consumo e efeito de negócio conectados à jornada |
| Preparação da entrega | Verificações, documentação, roteiro e versão final identificada |

## 9. Avaliação

Consulte a [proposta de rubrica e pesos](docs/CRITERIOS-DE-AVALIACAO.md). Ela privilegia a integração funcional e a capacidade de demonstrar o resultado, sem pontuar uma equipe simplesmente por utilizar mais frameworks ou plataformas.

Funcionalidades opcionais não compensam a ausência dos requisitos obrigatórios. Isso significa que a evidência do requisito deve ser avaliada no critério correspondente; este documento não cria reprovação automática ou teto de nota.

## 10. Checklist final

- [ ] Equipe com até cinco integrantes identificada.
- [ ] Projeto web do quarto semestre e versão de origem referenciados.
- [ ] Evolução do site e escopo entregue explicados.
- [ ] Aplicativo Flutter funcionando em um destino móvel.
- [ ] API funcional e contrato documentado.
- [ ] Dados compartilhados de forma verificável entre as interfaces.
- [ ] Broker com publicação e consumo reais em uma funcionalidade.
- [ ] Efeito do consumidor observável e comportamento de falha explicado.
- [ ] Backoffice funcional, web ou desktop, integrado à API e ao fluxo escolhido.
- [ ] Guia de execução, configuração de exemplo e dados de demonstração disponíveis.
- [ ] Verificações e limitações do MVP registradas.
- [ ] Versão final do código identificada e contribuições dos integrantes descritas.
- [ ] Entrega preparada para 28 de novembro de 2026.

## 11. Referências e materiais de apoio

- [PPC indicado para a disciplina](https://bkpsitecpsnew.blob.core.windows.net/uploadsitecps/sites/19/2026/07/sl_PPC_DesenvolvimentoSoftwareMultiplataforma-6a469a7083e52.pdf#page=61): ementa da disciplina na página impressa 60, página 61 do arquivo.
- [Página institucional do curso na Fatec Araras](https://fatecararas.cps.sp.gov.br/tecnologia-em-desenvolvimento-de-softwares-multiplataforma/).
- [Workshop de microserviços](https://github.com/F290-LDMP/workshop-microservices): referência prática, sem obrigatoriedade de copiar sua stack.
- [Introdução a microserviços](https://github.com/F290-LDMP/IntroducaoMicroServicos).

**Versão do enunciado:** 1.0, elaborada em 25/10/2026. Ajustes posteriores devem ser comunicados pelo docente e registrados no histórico Git, especialmente quando afetarem requisitos, prazo ou avaliação.
