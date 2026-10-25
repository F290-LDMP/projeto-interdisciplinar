# Proposta de critérios de avaliação

[Voltar ao enunciado](../README.md)

**Status: proposta docente para ratificação.** Os pesos abaixo são uma sugestão para esta atividade. Não são prescrições do CESU. O docente deve confirmar a rubrica com a turma antes de aplicá-la.

Os requisitos obrigatórios, a equipe de até cinco integrantes e o prazo de 28/11/2026 constam no [enunciado](../README.md). Esta rubrica não acrescenta regras de aprovação, penalidades por atraso, nota mínima ou obrigatoriedade de ferramentas específicas.

## 1. Distribuição sugerida — 100 pontos

| Critério | Natureza | Peso |
|---|---|---:|
| A. Solução multiplataforma e jornada integrada | Equipe | 30 |
| B. API, regras de negócio e persistência | Equipe | 20 |
| C. Mensageria aplicada a uma funcionalidade | Equipe | 20 |
| D. Qualidade, documentação e reprodução | Equipe | 15 |
| E. Participação individual e apresentação | Individual | 15 |
| **Total** | **85 pontos da equipe + 15 individuais** | **100** |

A avaliação ocorrerá em **apresentação formal e presencial perante banca**, com **até 30 minutos por equipe para pitch e demonstração**. A ficha resumida organiza a identificação e os links; os requisitos técnicos serão evidenciados na demonstração e nos repositórios de apoio. Não é exigido um relatório extenso no formato do modelo anterior.

Uma mesma evidência pode ajudar a compreender vários critérios, mas cada um avalia uma dimensão distinta: A observa a jornada entre interfaces; B, o backend; C, a integração assíncrona; D, a verificabilidade e manutenção; E, a contribuição e a compreensão de cada integrante.

## 2. Evidências por critério

### A. Solução multiplataforma e jornada integrada — 30 pontos

| Subcritério | Pontos | O que observar |
|---|---:|---|
| Evolução da aplicação web | 8 | Origem no quarto semestre, mudanças identificadas e site funcional no domínio do projeto |
| Aplicativo móvel Flutter | 10 | Jornada funcional, comunicação real com a API e tratamento de estados da interface |
| Backoffice | 7 | Operação administrativa relevante e integração com a API e o resultado da mensageria |
| Coerência entre plataformas | 5 | Uma ação ou dado pode ser acompanhado em outra interface, com resultado consistente |
| **Subtotal** | **30** | |

Desktop é opcional. Um backoffice web pode atingir a pontuação integral. Não é necessário entregar Android e iOS simultaneamente. Acabamento visual sofisticado não substitui funcionamento integrado.

### B. API, regras de negócio e persistência — 20 pontos

| Subcritério | Pontos | O que observar |
|---|---:|---|
| Operações e regras do MVP | 8 | API suficiente para a jornada; regras implementadas no backend |
| Persistência e dados compartilhados | 6 | Informações realmente armazenadas e utilizadas pelas aplicações |
| Contrato, validação e erros | 6 | Operações e respostas documentadas; entradas e falhas tratadas de forma compreensível |
| **Subtotal** | **20** | |

Não há vantagem de pontuação por escolher Java/Spring Boot ou por decompor o backend em mais serviços. Avalia-se o resultado e a adequação das decisões.

### C. Mensageria aplicada a uma funcionalidade — 20 pontos

| Subcritério | Pontos | O que observar |
|---|---:|---|
| Finalidade e contrato | 5 | Justificativa da comunicação assíncrona; produtor, consumidor, destino e payload identificados |
| Publicação, consumo e efeito | 10 | Mensagem real percorrendo o broker e produzindo efeito de negócio observável |
| Comportamento em falhas | 5 | Cenário de falha demonstrado, limitações declaradas e forma de acompanhamento ou recuperação explicada |
| **Subtotal** | **20** | |

Apenas instalar o broker ou produzir logs sem consumo não evidencia o fluxo completo. Um worker backend que alimenta o backoffice atende ao modelo admitido no enunciado. Não é exigida conexão direta da interface ao broker.

Retries, DLQ, idempotência e Outbox podem melhorar o resultado, mas não são uma lista cumulativa de recursos obrigatórios. Sua presença só contribui quando funciona, é pertinente e pode ser explicada.

### D. Qualidade, documentação e reprodução — 15 pontos

| Subcritério | Pontos | O que observar |
|---|---:|---|
| Execução reproduzível | 5 | Pré-requisitos, variáveis, ordem de inicialização e dados de demonstração suficientes |
| Verificações e qualidade | 5 | Casos reproduzíveis de sucesso, entrada inválida e falha assíncrona; testes e resultados descritos |
| Organização e segurança básica | 5 | Código versionado, decisões e limitações documentadas, segredos fora do Git e acesso administrativo explicado |
| **Subtotal** | **15** | |

Testes automatizados são recomendados. Quando a equipe declarar uso de TDD, deve apresentar evidência do ciclo de desenvolvimento; a simples existência de testes não comprova TDD.

### E. Participação individual e apresentação — 15 pontos por integrante

| Subcritério | Pontos | O que observar |
|---|---:|---|
| Compreensão técnica | 6 | Explica a parte em que atuou, suas decisões e a integração com o restante da solução |
| Contribuição verificável | 6 | Referências a código, testes, documentação, design, revisão ou organização do trabalho |
| Comunicação e colaboração | 3 | Comunica o produto com clareza no pitch e na demonstração perante a banca, organiza a exposição no tempo disponível e descreve o trabalho conjunto |
| **Subtotal** | **15** | |

A contribuição não deve ser medida apenas pela quantidade de commits. Issues, revisões, programação em pares, testes, documentação e outras evidências contextualizadas podem demonstrar participação. Avaliação em pares pode complementar a análise, com mediação do docente; não deve gerar penalidade automática por votação.

## 3. Escala sugerida para cada subcritério

| Nível | Fator | Descrição |
|---|---:|---|
| Não evidenciado | 0,00 | Não entregue ou sem evidência verificável |
| Inicial | 0,25 | Parcial ou majoritariamente simulado; não demonstra o resultado esperado |
| Parcialmente funcional | 0,50 | Funciona em parte, com limitações que interrompem cenários relevantes |
| Funcional | 0,75 | Atende à maior parte do esperado, com lacunas pontuais na implementação ou evidência |
| Consolidado | 1,00 | Atende ao esperado, pode ser reproduzido e é explicado com clareza |

Para cada subcritério, aplicar `pontos obtidos = pontos máximos × fator`. O nível deve ser justificado por evidências e aplicado de forma consistente entre as equipes.

A ausência de uma plataforma obrigatória ou do consumo do broker deve aparecer na avaliação dos subcritérios correspondentes e no checklist de requisitos. Não há, nesta proposta, regra adicional de reprovação automática ou teto geral de nota.

## 4. Composição individual sugerida

```text
Pontos da equipe = A + B + C + D       (máximo 85)
Pontos do integrante = pontos da equipe + E do integrante
                                         (máximo 100)
```

Se a disciplina utilizar escala de zero a dez, a conversão sugerida é `nota = pontos / 10`, observadas as regras acadêmicas de arredondamento e composição da disciplina.

Esta proposta se refere à avaliação do projeto. Não define seu percentual na média semestral da disciplina, que deve ser informado pelo docente.

## 5. Opcionais e equidade

Versão desktop adicional, nuvem, IoT, CI/CD, suporte a outro sistema móvel e outras extensões podem ser apresentados, mas não recebem bônus automático e não substituem o núcleo obrigatório. Não há exigência de serviços pagos ou publicação em lojas.

A complexidade deve ser proporcional ao MVP. Uma solução menor, bem integrada e verificável pode atingir a pontuação integral.

## 6. Registro de feedback

Sugestão de registro para o docente:

| Critério | Pontos | Evidências observadas e próximos passos |
|---|---:|---|
| A. Multiplataforma | /30 | |
| B. API | /20 | |
| C. Mensageria | /20 | |
| D. Qualidade e documentação | /15 | |
| E. Individual — preencher por integrante | /15 | |

Antes da apresentação final, o docente pode utilizar os mesmos critérios para devolutivas formativas, sem transformar os marcos sugeridos em novos prazos ou descontos não comunicados.
