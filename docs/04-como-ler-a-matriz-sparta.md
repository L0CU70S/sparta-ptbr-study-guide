# Como ler a matriz SPARTA

[🇺🇸 English](../README.md) · [🇧🇷 Início em Português](../README.pt-BR.md) · [← O que é SPARTA?](01-o-que-e-sparta.md) · [← SPARTA e MITRE ATT&CK](02-sparta-e-mitre-attack.md) · [← Glossário](03-glossario-space-cybersecurity-ptbr-en.md)

> **Material educacional independente e não oficial.**
>
> Este documento não é afiliado, endossado, mantido ou patrocinado pela The Aerospace Corporation, pelo projeto SPARTA, pelo NIST, pela CCSDS ou por qualquer agência espacial. Em caso de divergência, a fonte oficial em inglês prevalece.

## Objetivo

Este documento explica, em nível introdutório, como navegar e interpretar uma matriz de ameaças como o **SPARTA — Space Attack Research and Tactic Analysis**.

O objetivo não é reproduzir a matriz completa nem substituir os materiais oficiais. A proposta é ensinar um método de leitura que ajude estudantes e profissionais a usar a fonte oficial de forma mais consciente, defensiva e orientada ao contexto de missão.

- Fonte oficial: <https://sparta.aerospace.org/>
- Material introdutório: <https://sparta.aerospace.org/resources/getting-started>
- Perguntas frequentes: <https://sparta.aerospace.org/resources/faq>

## Antes de abrir a matriz

Não comece perguntando “quais técnicas devo usar?”. Comece pelo sistema ou cenário que deseja analisar.

Antes de consultar qualquer framework, registre ao menos:

- Qual é o objetivo da missão ou do serviço?
- Quais ativos são essenciais para a missão?
- Quais segmentos participam: Ground, Link, Space e User?
- Quais dados, comandos ou funções precisam de confidencialidade, integridade e disponibilidade?
- Quais interfaces existem entre redes, operadores, fornecedores, estações e sistemas?
- Qual seria o impacto de perda de disponibilidade, alteração indevida ou divulgação de dados?
- Quais premissas e limitações técnicas existem?

A matriz serve para enriquecer a análise de ameaças. Ela não substitui a compreensão da arquitetura, do objetivo operacional e do risco da missão.

## Elementos principais

### Tática (*Tactic*)

Uma tática representa o objetivo ou intenção geral de uma ação adversária — em termos simples, o “por quê”.

Exemplo conceitual: um adversário pode buscar acesso, persistência, execução, impacto ou obtenção de informações. O nome e a organização das táticas devem ser consultados diretamente na fonte oficial.

### Técnica (*Technique*)

Uma técnica representa um método geral que pode ser usado para alcançar uma tática — o “como” em nível amplo.

Ao estudar uma técnica, não conclua automaticamente que ela se aplica à sua missão. Pergunte:

- Essa técnica é tecnicamente possível naquela arquitetura?
- Existe uma interface, exposição ou fraqueza que viabilize o cenário?
- O adversário teria motivação e capacidade relevantes?
- Qual seria o impacto operacional se o cenário ocorresse?

### Subtécnica (*Sub-technique*)

Uma subtécnica descreve uma variação mais específica de uma técnica. Ela aumenta a precisão da análise, mas também exige cuidado para não transformar uma hipótese em certeza.

Em um estudo público, cite a subtécnica pelo identificador e nome oficial, fornecendo link para a fonte original. Evite reproduzir grandes blocos de conteúdo oficial quando um link e uma explicação própria forem suficientes.

### Procedimento (*Procedure*)

Um procedimento descreve a forma concreta como uma técnica pode ser executada em um contexto específico.

Para um repositório educacional público, não publique procedimentos ofensivos capazes de facilitar comprometimento, interrupção, interferência em RF, jamming, spoofing, intrusão ou controle não autorizado de sistemas reais. Mantenha o foco em análise defensiva, arquitetura, controles, monitoramento e resposta.

### Contramedida (*Countermeasure*)

Uma contramedida representa uma medida de defesa que pode prevenir, detectar, limitar, responder ou reduzir o impacto de uma técnica.

Uma contramedida não é, necessariamente, um produto. Ela pode incluir processos, arquitetura, gestão de identidade, segmentação, registro de eventos, validação de comandos, controles criptográficos, requisitos de engenharia, procedimentos operacionais e testes.

## Um fluxo de leitura seguro

Use este fluxo ao estudar uma técnica do SPARTA:

```text
Missão e objetivos
       ↓
Ativos e segmentos envolvidos
       ↓
Interfaces e fronteiras de confiança
       ↓
Cenários de ameaça relevantes
       ↓
Técnicas/subtécnicas SPARTA potencialmente aplicáveis
       ↓
Impacto + probabilidade + criticidade
       ↓
Contramedidas e controles proporcionais
       ↓
Requisitos, monitoramento, playbooks e testes
```

A ideia é iniciar no contexto e terminar em decisões de segurança verificáveis.

## Como interpretar uma técnica sem exagerar

Uma técnica em uma matriz deve ser entendida como uma hipótese estruturada, não como evidência de que um ataque aconteceu ou acontecerá.

Use uma ficha de leitura como esta:

| Campo | Pergunta orientadora |
|---|---|
| Técnica SPARTA | Qual é o identificador e nome oficial? |
| Segmento | Ela parece mais relevante para Ground, Link, Space, User ou mais de um segmento? |
| Ativos afetados | Quais ativos ou funções da missão poderiam ser impactados? |
| Pré-condições | Que interfaces, acessos, exposições ou falhas seriam necessários? |
| Impacto | O que poderia ocorrer com confidencialidade, integridade, disponibilidade e sucesso da missão? |
| Probabilidade | O cenário é plausível para esta arquitetura e adversário considerado? |
| Contramedidas | Quais medidas defensivas podem reduzir o risco? |
| Evidência | O que poderia ser monitorado, auditado, testado ou revisado? |
| Risco residual | O que ainda permanece após os controles? |

## Exemplo defensivo e fictício

Considere um cenário fictício de Ground Segment com:

- Rede corporativa.
- Ambiente de engenharia.
- MOC.
- Servidor de processamento de telemetria.
- Acesso privilegiado de operadores.
- Conectividade com uma estação terrena.

Em vez de buscar diretamente uma técnica, comece com a pergunta:

> “Quais falhas de identidade, acesso remoto, segmentação, monitoramento ou mudança de configuração poderiam afetar a integridade e a disponibilidade de operações de missão?”

A partir daí, um estudo defensivo pode:

1. Identificar ativos críticos e fluxos de dados.
2. Desenhar fronteiras de confiança entre ambiente corporativo, engenharia e operação.
3. Consultar referências SPARTA para selecionar hipóteses relevantes.
4. Propor controles como MFA, PAM, segregação de redes, gestão de mudanças, logs centralizados e revisão de acessos.
5. Criar casos de detecção e um playbook de resposta a incidente.

Esse exemplo não pressupõe uma arquitetura real e não apresenta instruções ofensivas.

## Da matriz para controles e requisitos

O valor de uma técnica aumenta quando ela ajuda a orientar uma decisão. Uma sequência possível é:

| Etapa | Pergunta | Produto de trabalho |
|---|---|---|
| Ameaça | O que pode afetar a missão? | Cenário de ameaça |
| Técnica | Como o cenário poderia ocorrer em alto nível? | Referência SPARTA aplicável |
| Risco | Qual é o impacto e a probabilidade? | Registro de risco |
| Contramedida | Como reduzir a probabilidade ou impacto? | Estratégia de mitigação |
| Controle | Qual salvaguarda concreta será adotada? | Matriz de controles |
| Requisito | Como tornar a decisão verificável? | Requisito de segurança |
| Validação | Como demonstrar que o requisito funciona? | Caso de teste, log, evidência ou tabletop |

A Aerospace descreve o uso de técnicas SPARTA como parte de uma análise orientada por ameaças que pode levar a contramedidas, controles e requisitos de aquisição/engenharia. A seleção deve considerar risco, criticidade e contexto de missão. [^1]

## Boas práticas de documentação

Ao escrever uma nota sobre uma técnica ou grupo de técnicas:

- Mantenha o identificador e o nome oficial em inglês.
- Inclua um link para a página oficial correspondente.
- Escreva a explicação em suas próprias palavras.
- Diferencie fatos da fonte, premissas do cenário e sua interpretação.
- Use cenários fictícios e orientados à defesa.
- Registre limitações e incertezas.
- Evite prometer mitigação total: controles reduzem risco, mas raramente o eliminam.

## Erros comuns

| Erro | Por que é um problema | Alternativa melhor |
|---|---|---|
| Começar pela técnica | Ignora objetivo, arquitetura e risco | Começar pela missão, ativos e interfaces |
| Copiar a matriz inteira | Cria esforço de manutenção e risco de desatualização | Citar fonte oficial e publicar interpretação original |
| Aplicar todos os controles | Pode gerar custos e complexidade sem tratar risco real | Adaptar controles ao risco e à missão |
| Tratar técnica como incidente confirmado | Uma técnica é uma hipótese ou referência, não prova | Validar com logs, evidências e contexto |
| Focar apenas em tecnologia | Segurança depende também de processos, pessoas e engenharia | Considerar governança, procedimentos, arquitetura e operação |
| Misturar estudo com ambiente real | Pode expor dados ou induzir conclusões sem autorização | Usar laboratórios e cenários fictícios |

## Próximos passos

Depois de compreender como ler a matriz, o próximo passo é aplicar o raciocínio em um processo de modelagem de ameaças:

- [`05-sparta-e-threat-modeling.md`](05-sparta-e-threat-modeling.md)

## Referências

[^1]: The Aerospace Corporation. *Space Segment Cybersecurity Profile for National Security Systems*, TOR-2023-02161 Rev A, 2024.

- The Aerospace Corporation. [SPARTA — Space Attack Research and Tactic Analysis](https://sparta.aerospace.org/).
- The Aerospace Corporation. [Getting Started — SPARTA](https://sparta.aerospace.org/resources/getting-started).
- The Aerospace Corporation. [SPARTA FAQ](https://sparta.aerospace.org/resources/faq).
- Scholl, M.; Suloway, T. [NIST IR 8270 — Introduction to Cybersecurity for Commercial Satellite Operations](https://csrc.nist.gov/pubs/ir/8270/final), 2023.

---

> **Nota de responsabilidade:** este documento contém apenas conteúdo educacional independente baseado em fontes públicas. Não contém dados de clientes, informações do empregador, credenciais, topologias reais, detalhes operacionais sensíveis ou instruções para comprometer, interferir ou interromper sistemas espaciais ou de comunicação.
