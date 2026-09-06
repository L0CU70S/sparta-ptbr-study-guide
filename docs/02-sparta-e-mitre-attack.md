# SPARTA e MITRE ATT&CK: uma comparação introdutória

[🇺🇸 English](../README.md) · [🇧🇷 Início em Português](../README.pt-BR.md) · [← O que é SPARTA?](01-o-que-e-sparta.md)

> **Material educacional independente e não oficial.**
>
> Este documento não é afiliado, endossado, mantido ou patrocinado pela The Aerospace Corporation, pelo projeto SPARTA, pela MITRE, pelo NIST, pela CCSDS ou por qualquer agência espacial. Em caso de divergência, as fontes oficiais em inglês prevalecem.

## Resumo

Profissionais de cibersegurança frequentemente conhecem o **MITRE ATT&CK** como uma base de conhecimento para organizar comportamentos adversários. No contexto de sistemas e missões espaciais, o **SPARTA — Space Attack Research and Tactic Analysis** oferece uma referência pública voltada à identificação e análise de ameaças específicas desse domínio.

## Por que comparar?

A comparação ajuda profissionais de Blue Team, DFIR, SOC, infraestrutura, OT/ICS e segurança de redes a compreenderem mais rapidamente a função de uma matriz de ameaças aplicada ao domínio espacial.

Em ambos os casos, uma taxonomia de comportamento adversário pode apoiar:

- Uma linguagem comum para discutir riscos e cenários de ameaça.
- Modelagem de ameaças (*threat modeling*).
- Priorização de detecções, monitoramento e resposta a incidentes.
- Relacionamento entre ameaças, controles e requisitos de segurança.
- Comunicação entre times técnicos, engenharia, operações e gestão.

A comparação deve terminar aí: ela é um recurso didático, não uma afirmação de que SPARTA e ATT&CK possuem a mesma estrutura, cobertura, governança ou finalidade.

## Visão comparativa

| Aspecto | MITRE ATT&CK | SPARTA |
|---|---|---|
| Organização responsável | MITRE | The Aerospace Corporation |
| Objetivo geral | Base de conhecimento sobre táticas e técnicas adversárias em domínios definidos do ATT&CK | Referência de ameaças e comportamentos adversários voltada a sistemas e missões espaciais |
| Contextos principais | Enterprise, Mobile, ICS e outros domínios ATT&CK | Sistemas espaciais e seus segmentos de missão |
| Uso comum | Threat intelligence, engenharia de detecção, Purple Team, investigação, hardening e resposta | Modelagem de ameaças espaciais, avaliação de riscos, contramedidas, controles e requisitos de missão |
| Escopo operacional | Pode envolver endpoints, identidade, redes, cloud, aplicações e sistemas industriais, conforme o domínio | Pode envolver Ground Segment, Link Segment, Space Segment, operações de missão e componentes relacionados |
| Fonte | [attack.mitre.org](https://attack.mitre.org/) | [sparta.aerospace.org](https://sparta.aerospace.org/) |

## O que eles têm em comum

Os dois frameworks ajudam a transformar uma pergunta ampla — “como um adversário poderia afetar este ambiente?” — em uma discussão mais estruturada.

Em nível conceitual, ambos podem ajudar a:

- Organizar comportamentos adversários por objetivos e métodos.
- Registrar hipóteses de ameaça de maneira consistente.
- Relacionar cenários de ameaça a medidas defensivas.
- Priorizar o que deve ser monitorado, analisado ou testado.
- Apoiar exercícios de resposta a incidentes e melhoria contínua.

Para profissionais que já conhecem ATT&CK, o SPARTA pode ser uma porta de entrada para aprender a pensar em ameaças dentro das particularidades de uma missão espacial.

## Diferenças que importam

### 1. O contexto de missão é central no SPARTA

Em sistemas espaciais, a segurança precisa considerar o objetivo da missão, a criticidade do ativo, as limitações de conectividade, o ciclo de vida do sistema, as responsabilidades entre segmentos e o impacto operacional.

Um controle adequado para um ambiente corporativo pode não ser suficiente, aplicável ou viável da mesma forma em um componente espacial. A seleção precisa considerar riscos reais, arquitetura e necessidades da missão.

### 2. O SPARTA se conecta a contramedidas e controles

O SPARTA pode apoiar uma sequência de análise que parte de ameaças e técnicas, passa por contramedidas e se relaciona a controles e requisitos de segurança. Isso ajuda a sair de uma lista genérica de boas práticas e chegar a decisões justificadas pelo risco.

### 3. Ground, link e space possuem responsabilidades diferentes

Uma missão pode ter controles implementados em mais de um segmento. Por exemplo, identidade, monitoramento, gestão de acesso e resposta a incidentes tendem a ter grande presença no Ground Segment; já componentes de integridade, modos seguros e restrições de hardware podem exigir decisões específicas do Space Segment.

Essa divisão não significa que os segmentos devam ser protegidos isoladamente. Uma arquitetura de segurança precisa considerar dependências e responsabilidades compartilhadas.

### 4. O conhecimento aplicável depende do domínio

Uma organização que opera uma estação terrena ou um MOC pode se beneficiar de ambos os tipos de referência:

- **MITRE ATT&CK**, para cenários comuns de identidade, endpoint, rede, e-mail, acesso remoto, cloud e ambiente corporativo.
- **SPARTA**, para estruturar riscos e ameaças que envolvem os elementos e impactos específicos de sistemas e missões espaciais.

O uso simultâneo não significa combinar matrizes sem critério. A arquitetura, os ativos, os objetivos de missão e o cenário de risco devem determinar quais referências são relevantes.

## Exemplo conceitual: ambiente fictício de operações de missão

Considere um ambiente fictício composto por uma rede corporativa, um ambiente de engenharia, um Mission Operations Center (MOC), sistemas de processamento de telemetria, controles de acesso privilegiado e conectividade com uma estação terrena.

Uma análise defensiva poderia usar:

| Necessidade | Pergunta de segurança | Referência que pode ajudar |
|---|---|---|
| Ambiente corporativo | Como identificar e investigar acesso indevido, abuso de credenciais ou movimentação lateral? | MITRE ATT&CK, além de logs, SIEM, EDR e procedimentos internos |
| Operação de missão | Como avaliar riscos que podem afetar comando, telemetria, disponibilidade operacional ou integridade da missão? | SPARTA, análise de risco de missão e contramedidas aplicáveis |
| Arquitetura | Onde estão os limites de confiança entre rede corporativa, engenharia e operações? | Threat modeling, segmentação e princípios de sistemas críticos |
| Resposta | Como conter, investigar e recuperar sem gerar impacto operacional adicional? | Playbooks, tabletop exercises, análise de impacto e procedimentos de missão |

O exemplo é fictício e não descreve uma arquitetura real nem procedimentos de ataque.

## Como estudar os dois de forma responsável

1. Comece pelos objetivos e ativos do ambiente, não pela matriz.
2. Use fontes oficiais e mantenha links para a fonte.
3. Para cada cenário, registre o contexto, impacto, suposições e limitações.
4. Não trate uma técnica como prova de que um ataque ocorrerá; trate-a como hipótese a ser avaliada.
5. Relacione cenários a controles proporcionais ao risco e à missão.
6. Produza apenas exemplos fictícios e defensivos em materiais públicos.
7. Diferencie estudo independente de experiência profissional em ambientes reais.

## Conclusão

Dizer que o SPARTA é “como um ATT&CK para o espaço” pode ser uma introdução didática útil, desde que venha acompanhada de uma ressalva: trata-se de uma analogia limitada.

O valor do SPARTA está em ajudar profissionais a organizar a análise de ameaças de acordo com as particularidades de sistemas espaciais, conectando ameaças, contramedidas, controles e requisitos de segurança orientados à missão.

## Referências

- MITRE. [MITRE ATT&CK](https://attack.mitre.org/).
- The Aerospace Corporation. [SPARTA — Space Attack Research and Tactic Analysis](https://sparta.aerospace.org/).
- The Aerospace Corporation. [SPARTA FAQ](https://sparta.aerospace.org/resources/faq).
- The Aerospace Corporation. *Space Segment Cybersecurity Profile for National Security Systems*, TOR-2023-02161 Rev A, 2024.
- Scholl, M.; Suloway, T. [NIST IR 8270 — Introduction to Cybersecurity for Commercial Satellite Operations](https://csrc.nist.gov/pubs/ir/8270/final), 2023.

---

> **Nota de responsabilidade:** este documento utiliza apenas fontes públicas e conteúdo educacional independente. Não contém informações de clientes, empregadores, sistemas reais, credenciais, topologias operacionais ou instruções para comprometer, interferir ou interromper sistemas espaciais ou de comunicação.
