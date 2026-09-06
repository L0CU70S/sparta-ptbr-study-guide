# O que é o SPARTA?

[🇺🇸 English](../README.md) · [🇧🇷 Início em Português](../README.pt-BR.md)

> **Material educacional independente e não oficial.**
>
> Este documento não é afiliado, endossado, mantido ou patrocinado pela The Aerospace Corporation, pelo SPARTA, pelo NIST, pela CCSDS ou por qualquer agência espacial. Em caso de divergência, a fonte oficial em inglês prevalece.

## Resumo

**SPARTA** significa **Space Attack Research and Tactic Analysis**. É um framework público de cibersegurança espacial criado pela **The Aerospace Corporation** para apoiar a identificação, organização e análise de ameaças cibernéticas associadas a sistemas e missões espaciais.

Este guia apresenta uma explicação introdutória em português brasileiro. Ele não substitui o conteúdo oficial do SPARTA nem representa uma tradução oficial.

- Fonte oficial: <https://sparta.aerospace.org/>
- Perguntas frequentes: <https://sparta.aerospace.org/resources/faq>
- Termos de serviço: <https://sparta.aerospace.org/terms-of-service>

## Por que o SPARTA importa?

Sistemas espaciais dependem de componentes em terra, enlaces de comunicação, sistemas embarcados e aplicações de usuários. Cada segmento possui ativos, interfaces, restrições operacionais e riscos próprios.

O SPARTA oferece uma taxonomia para estruturar a discussão sobre comportamentos adversários nesse contexto. Ele pode apoiar, entre outras atividades:

- Modelagem de ameaças (*threat modeling*).
- Avaliação e priorização de riscos.
- Identificação de contramedidas defensivas.
- Seleção e adaptação de controles de segurança.
- Definição de requisitos de segurança verificáveis.
- Planejamento de monitoramento, detecção e resposta a incidentes.

A relação não é automática: uma técnica potencialmente aplicável deve ser analisada de acordo com a arquitetura, a missão, a criticidade, as ameaças relevantes e a tolerância a risco do sistema em questão.

## Conceitos fundamentais

| Termo em inglês | Tradução sugerida em PT-BR | Explicação introdutória |
|---|---|---|
| Tactic | Tática | Objetivo ou propósito de uma ação adversária: o “por quê”. |
| Technique | Técnica | Método geral utilizado para alcançar uma tática: o “como”. |
| Sub-technique | Subtécnica | Forma mais específica de executar uma técnica. |
| Procedure | Procedimento | Implementação concreta de uma técnica em determinado contexto. |
| Countermeasure | Contramedida | Medida defensiva que ajuda a prevenir, detectar, limitar ou responder a um risco. |
| Threat Modeling | Modelagem de ameaças | Processo de identificar ativos, fluxos, fronteiras de confiança, cenários de ameaça e controles. |
| Control Tailoring | Adaptação de controles | Ajuste de controles de segurança à missão, arquitetura, impacto e risco. |

## Segmentos de um sistema espacial

Para estudar o SPARTA, é útil reconhecer os principais segmentos de uma missão:

| Segmento | Papel geral | Exemplos de elementos |
|---|---|---|
| Space Segment | Parte espacial/em órbita | Plataforma espacial, payload, computador de bordo e software de voo. |
| Link Segment | Comunicação entre espaço, terra e usuários | Antenas, transceptores, transmissão, componentes de criptografia e dados em trânsito. |
| Ground Segment | Operação e suporte em terra | Estação terrena, comando e controle, processamento de dados, rede de ground e operações de segurança. |
| User Segment | Consumo e uso dos serviços de missão | Dispositivos de usuários, gateways e aplicações que recebem ou utilizam dados de missão. |

A documentação da Aerospace destaca que os segmentos não devem ser protegidos de forma isolada: há responsabilidades específicas e controles compartilhados entre componentes de uma missão.

## Como o SPARTA pode ser usado de forma defensiva

Um fluxo de estudo seguro e aplicável é:

1. Definir um cenário fictício de missão e seu objetivo.
2. Identificar ativos, dados, interfaces e fronteiras de confiança.
3. Selecionar ameaças relevantes com base em informações públicas e no contexto da missão.
4. Consultar técnicas e subtécnicas SPARTA potencialmente aplicáveis.
5. Avaliar impacto, probabilidade, criticidade e risco residual.
6. Identificar contramedidas e controles defensivos proporcionais ao risco.
7. Transformar decisões em requisitos, casos de monitoramento, playbooks e testes.

Esse uso é mais útil do que simplesmente listar técnicas. O objetivo é conectar ameaças a decisões de segurança que favoreçam resiliência e sucesso da missão.

## Relação com MITRE ATT&CK

A comparação entre SPARTA e MITRE ATT&CK pode ajudar como introdução: ambos estruturam conhecimento sobre comportamento adversário usando conceitos como táticas e técnicas.

Entretanto, eles não são equivalentes. O SPARTA tem escopo próprio em sistemas e missões espaciais e deve ser lido dentro das particularidades de Ground Segment, Link Segment, Space Segment, operações de missão e restrições de engenharia espacial.

Leia a comparação introdutória planejada em: [`02-sparta-e-mitre-attack.md`](02-sparta-e-mitre-attack.md).

## O que o SPARTA não é

- Não é um produto de segurança.
- Não é uma ferramenta automática de pentest.
- Não é uma lista universal de controles pronta para copiar e colar.
- Não substitui inteligência de ameaças validada ou análise específica da missão.
- Não elimina a necessidade de avaliação de risco, engenharia de segurança e validação de controles.

## Referências

- The Aerospace Corporation. [SPARTA — Space Attack Research and Tactic Analysis](https://sparta.aerospace.org/).
- The Aerospace Corporation. [SPARTA FAQ](https://sparta.aerospace.org/resources/faq).
- Scholl, M.; Suloway, T. [NIST IR 8270 — Introduction to Cybersecurity for Commercial Satellite Operations](https://csrc.nist.gov/pubs/ir/8270/final), 2023.
- The Aerospace Corporation. *Space Segment Cybersecurity Profile for National Security Systems*, TOR-2023-02161 Rev A, 2024.

---

> **Nota de responsabilidade:** este documento utiliza apenas fontes públicas e conteúdo educacional independente. Não contém informações de clientes, empregadores, sistemas reais, credenciais, topologias operacionais ou instruções para interferir, comprometer ou interromper sistemas espaciais ou de comunicação.
