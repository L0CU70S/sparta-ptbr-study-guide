# Glossário de Cibersegurança Espacial — PT-BR / EN

[🇺🇸 English](../README.md) · [🇧🇷 Início em Português](../README.pt-BR.md) · [← O que é SPARTA?](01-o-que-e-sparta.md) · [SPARTA e MITRE ATT&CK →](02-sparta-e-mitre-attack.md)

> **Material educacional independente e não oficial.**
>
> Este glossário não é afiliado, endossado, mantido ou patrocinado pela The Aerospace Corporation, pelo projeto SPARTA, pelo NIST, pela CCSDS ou por qualquer agência espacial. Os termos originais e fontes oficiais em inglês prevalecem em caso de divergência.

## Objetivo

Este glossário reúne termos iniciais usados em sistemas espaciais, operações de missão e cibersegurança espacial. Ele foi criado para apoiar o estudo de referências em inglês, como SPARTA, NIST IR 8270 e materiais da CCSDS.

Não é uma tradução oficial de qualquer framework ou padrão. As traduções são sugestões educacionais em português brasileiro e devem ser interpretadas no contexto técnico da fonte original.

## Como usar

- Mantenha o termo em inglês ao pesquisar documentação, vagas e padrões internacionais.
- Use a tradução em PT-BR para explicar o conceito a públicos brasileiros.
- Em documentos técnicos, apresente o termo em português e o original em inglês na primeira ocorrência.
- Quando um termo não tiver equivalente consolidado em português, prefira manter o original e incluir uma explicação curta.

Exemplo de uso recomendado:

> O **Segmento Terrestre (Ground Segment)** inclui os componentes em terra usados para operação, comando, controle, processamento e segurança de uma missão.

---

## 1. Segmentos e arquitetura de missão

| Termo em inglês | Tradução sugerida em PT-BR | Explicação introdutória |
|---|---|---|
| Space Cybersecurity | Cibersegurança Espacial | Disciplina de proteção de sistemas, dados, operações e missões espaciais contra riscos cibernéticos. |
| Space System | Sistema Espacial | Conjunto completo de componentes espaciais, terrestres, enlaces, usuários e processos que entregam uma missão ou serviço. |
| Space Segment | Segmento Espacial | Parte em órbita, incluindo plataforma espacial, carga útil, computador de bordo e sistemas embarcados. |
| Ground Segment | Segmento Terrestre | Componentes em terra que apoiam operação, comando, controle, processamento de dados, rede e cibersegurança. |
| Link Segment | Segmento de Enlace | Componentes e comunicações que conectam espaço, terra e, dependendo da arquitetura, usuários. |
| User Segment | Segmento do Usuário | Dispositivos, gateways, aplicações e usuários que consomem ou utilizam serviços e dados da missão. |
| Spacecraft | Espaçonave | Veículo ou plataforma espacial; conforme a missão, pode incluir um satélite, veículo espacial ou outro ativo em órbita. |
| Satellite | Satélite | Objeto artificial colocado em órbita para cumprir funções como comunicação, observação, navegação ou ciência. |
| Payload | Carga útil | Parte da espaçonave dedicada à função principal da missão, como imageamento, comunicação ou coleta científica. |
| Bus | Plataforma da espaçonave | Subsistema que fornece funções de suporte à carga útil, como energia, estrutura, controle térmico e processamento. |
| On-Board Computer (OBC) | Computador de Bordo | Computador embarcado responsável por executar funções de controle, processamento e software de voo. |
| Flight Software | Software de Voo | Software executado no ativo espacial para apoiar controle, operação, processamento ou funções de missão. |
| Mission Architecture | Arquitetura de Missão | Organização de componentes, interfaces, fluxos de dados e responsabilidades que tornam a missão possível. |
| Mission Lifecycle | Ciclo de Vida da Missão | Fases pelas quais uma missão passa, da concepção e desenvolvimento à operação, descarte ou descomissionamento. |

---

## 2. Operações de missão e segmento terrestre

| Termo em inglês | Tradução sugerida em PT-BR | Explicação introdutória |
|---|---|---|
| Ground Station | Estação Terrena | Instalação e conjunto de sistemas usados para se comunicar com ativos espaciais. |
| Mission Operations Center (MOC) | Centro de Operações de Missão | Ambiente que planeja, acompanha, coordena e executa atividades operacionais da missão. A sigla MOC costuma ser mantida. |
| Command and Control (C2) | Comando e Controle | Capacidade de emitir comandos, acompanhar estados e coordenar a operação de ativos e sistemas de missão. |
| Telemetry | Telemetria | Dados enviados pelo ativo espacial para informar estado, saúde, desempenho ou resultados de missão. |
| Telecommand | Telecomando | Comando transmitido para um ativo espacial a fim de solicitar uma ação ou alteração operacional. |
| Tracking | Rastreamento | Acompanhamento de posição, trajetória ou visibilidade do ativo espacial. |
| TT&C | Telemetria, Rastreamento e Telecomando | Conjunto de capacidades essenciais para acompanhar e operar uma missão; a sigla TT&C é amplamente utilizada. |
| Uplink | Enlace de subida | Comunicação no sentido terra para espaço. |
| Downlink | Enlace de descida | Comunicação no sentido espaço para terra. |
| Mission Operations | Operações de Missão | Atividades e processos usados para manter uma missão operando e atingir seus objetivos. |
| Mission Assurance | Garantia de Missão | Abordagem multidisciplinar voltada a reduzir riscos e aumentar a probabilidade de sucesso da missão. |
| Operational Technology (OT) | Tecnologia Operacional | Tecnologia que monitora ou controla processos, dispositivos ou eventos físicos; princípios OT podem ser relevantes para sistemas de missão. |

---

## 3. SPARTA, ameaças e modelagem de ameaças

| Termo em inglês | Tradução sugerida em PT-BR | Explicação introdutória |
|---|---|---|
| SPARTA | SPARTA | Sigla de *Space Attack Research and Tactic Analysis*, framework público voltado à análise de ameaças cibernéticas em sistemas espaciais. O nome deve ser mantido. |
| Tactic | Tática | Objetivo ou propósito de uma ação adversária: o “por quê”. |
| Technique | Técnica | Método geral utilizado para alcançar uma tática: o “como”. |
| Sub-technique | Subtécnica | Forma mais específica de executar uma técnica. |
| Procedure | Procedimento | Implementação concreta de uma técnica em determinado contexto. |
| Threat | Ameaça | Circunstância, evento ou agente com potencial de causar impacto adverso a um ativo, sistema ou operação. |
| Threat Actor | Agente de Ameaça | Pessoa, grupo, organização ou outro ator capaz de realizar uma ação adversária. |
| Threat Intelligence | Inteligência de Ameaças | Informação analisada sobre ameaças, capacidades, intenções, indicadores ou contexto de risco. |
| Threat Modeling | Modelagem de Ameaças | Processo de identificar ativos, fluxos, fronteiras de confiança, cenários de ameaça, riscos e controles. |
| Attack Surface | Superfície de Ataque | Conjunto de pontos, interfaces e caminhos que podem ser expostos a uma ação adversária. |
| Attack Chain | Cadeia de Ataque | Sequência de etapas ou comportamentos que pode levar a um impacto adverso. |
| Countermeasure | Contramedida | Medida defensiva que ajuda a prevenir, detectar, limitar, responder ou recuperar de um cenário de ameaça. |
| Mitigation | Mitigação | Ação destinada a reduzir probabilidade, impacto ou exposição a um risco. |
| Detection | Detecção | Capacidade de identificar eventos, comportamentos ou condições potencialmente adversas. |
| Security Control | Controle de Segurança | Salvaguarda administrativa, técnica ou física usada para reduzir riscos. |

---

## 4. Risco, controles e engenharia de segurança

| Termo em inglês | Tradução sugerida em PT-BR | Explicação introdutória |
|---|---|---|
| Risk Assessment | Avaliação de Riscos | Processo de identificar, analisar e avaliar riscos considerando ameaças, vulnerabilidades, impacto e probabilidade. |
| Risk Tolerance | Tolerância a Risco | Nível de risco que uma organização ou missão está disposta a aceitar. |
| Risk Appetite | Apetite a Risco | Orientação de alto nível sobre a quantidade e o tipo de risco que uma organização pretende assumir. |
| Impact | Impacto | Magnitude do dano esperado caso confidencialidade, integridade ou disponibilidade seja comprometida. |
| Likelihood | Probabilidade | Chance de um evento de ameaça explorar uma vulnerabilidade ou ocorrer em determinado contexto. |
| Criticality | Criticidade | Grau de dependência da organização ou missão em relação a um ativo, função ou serviço. |
| Vulnerability | Vulnerabilidade | Fraqueza que pode ser explorada ou contribuir para um evento adverso. |
| Residual Risk | Risco Residual | Risco que permanece após a aplicação de controles e tratamentos. |
| Security Requirement | Requisito de Segurança | Declaração verificável que define uma necessidade de segurança para sistema, componente ou processo. |
| Control Tailoring | Adaptação de Controles | Ajuste de controles de segurança ao contexto técnico, risco, impacto e restrições da missão. |
| Security Architecture | Arquitetura de Segurança | Organização de componentes, controles, interfaces e princípios usados para proteger um sistema. |
| System Security Engineering (SSE) | Engenharia de Segurança de Sistemas | Aplicação de práticas de engenharia para incorporar segurança durante o ciclo de vida de um sistema. |
| Defense in Depth | Defesa em Profundidade | Uso de camadas complementares de proteção para reduzir dependência de um único controle. |
| Least Privilege | Menor Privilégio | Princípio de conceder apenas os acessos necessários para executar uma função autorizada. |
| Privileged Access Management (PAM) | Gestão de Acesso Privilegiado | Conjunto de processos e tecnologias para controlar, registrar e proteger acessos privilegiados. |

---

## 5. Comunicações, criptografia e segurança de enlace

| Termo em inglês | Tradução sugerida em PT-BR | Explicação introdutória |
|---|---|---|
| Satellite Communications (Satcom) | Comunicações por Satélite | Tecnologias e operações relacionadas à transmissão de dados usando satélites. |
| Radio Frequency (RF) | Radiofrequência | Faixa do espectro eletromagnético utilizada em comunicações sem fio, incluindo enlaces espaciais. |
| Antenna | Antena | Componente usado para transmitir ou receber sinais eletromagnéticos. |
| Transceiver | Transceptor | Equipamento capaz de transmitir e receber sinais. |
| Encryption | Cifragem | Transformação de dados para proteger confidencialidade contra acesso não autorizado. |
| Authentication | Autenticação | Processo de verificar identidade, origem ou legitimidade de uma entidade, mensagem ou comando. |
| Integrity | Integridade | Propriedade de que dados não foram alterados de forma não autorizada. |
| Anti-Replay | Proteção contra repetição | Mecanismos destinados a impedir que mensagens válidas sejam capturadas e reenviadas indevidamente. |
| Key Management | Gestão de Chaves | Processos de geração, proteção, distribuição, rotação, revogação e recuperação de chaves criptográficas. |
| Public Key Infrastructure (PKI) | Infraestrutura de Chaves Públicas | Pessoas, processos e tecnologias usados para gerenciar certificados e chaves públicas. |
| Jamming | Interferência intencional | Interferência deliberada que pode degradar ou impedir comunicações. Deve ser tratada apenas em contexto defensivo e de resiliência. |
| Spoofing | Falsificação | Simulação ou falsificação de uma identidade, sinal, mensagem ou fonte para induzir confiança indevida. |

---

## 6. Sistemas embarcados e resiliência

| Termo em inglês | Tradução sugerida em PT-BR | Explicação introdutória |
|---|---|---|
| Embedded System | Sistema Embarcado | Sistema computacional dedicado incorporado a um equipamento ou ativo físico. |
| Firmware | Firmware | Software de baixo nível que opera próximo ao hardware de um dispositivo. |
| Secure Boot | Inicialização Segura | Mecanismo que verifica a autenticidade e integridade de componentes de inicialização antes da execução. |
| Firmware Signing | Assinatura de Firmware | Uso de mecanismos criptográficos para verificar autoria e integridade de atualizações de firmware. |
| Software Bill of Materials (SBOM) | Lista de Materiais de Software | Inventário de componentes, bibliotecas e dependências de software. |
| Supply Chain Security | Segurança da Cadeia de Suprimentos | Proteção contra riscos associados a fornecedores, componentes, software, hardware e integrações. |
| Safe Mode | Modo Seguro | Estado operacional predefinido destinado a proteger o ativo e preservar funções essenciais diante de anomalias. |
| Resilience | Resiliência | Capacidade de resistir, adaptar-se, recuperar-se e continuar funções essenciais diante de eventos adversos. |
| Availability | Disponibilidade | Propriedade de que sistemas e serviços ficam acessíveis e utilizáveis quando necessários. |
| Recovery | Recuperação | Retorno controlado de capacidades após falha, incidente ou degradação operacional. |

---

## Termos que merecem atenção

Alguns termos não devem ser traduzidos isoladamente sem contexto:

- **Bus:** em contexto espacial, costuma significar a plataforma que fornece subsistemas de suporte à carga útil; “barramento” pode ter outro sentido em computação ou redes.
- **Ground:** pode aparecer como parte de diversas expressões técnicas, como *ground station*, *ground network* e *ground segment*. Preserve o termo completo em inglês na primeira ocorrência.
- **Command:** pode significar telecomando de missão, comando de sistema operacional ou comando administrativo. O contexto define a melhor tradução.
- **Control:** pode se referir a controle de segurança, controle operacional ou comando e controle. Prefira usar expressões completas.
- **Security:** pode abranger cibersegurança, segurança física, segurança operacional e segurança de missão. Não trate todos os sentidos como sinônimos.

## Como contribuir de forma responsável

Ao sugerir um novo termo ou alteração:

1. Inclua o termo original em inglês.
2. Informe a fonte pública em que ele aparece.
3. Proponha uma tradução PT-BR e uma explicação curta.
4. Indique se o termo possui ambiguidade ou tradução não consolidada.
5. Evite reproduzir conteúdo protegido de fontes externas além do necessário para referência.

## Histórico de alterações

| Versão | Data | Alteração |
|---|---|---|
| 0.1 | 2026-09 | Versão inicial com termos de arquitetura de missão, operações, SPARTA, risco, enlace e sistemas embarcados. |

## Referências

- The Aerospace Corporation. [SPARTA — Space Attack Research and Tactic Analysis](https://sparta.aerospace.org/).
- The Aerospace Corporation. [SPARTA FAQ](https://sparta.aerospace.org/resources/faq).
- Scholl, M.; Suloway, T. [NIST IR 8270 — Introduction to Cybersecurity for Commercial Satellite Operations](https://csrc.nist.gov/pubs/ir/8270/final), 2023.
- The Aerospace Corporation. *Space Segment Cybersecurity Profile for National Security Systems*, TOR-2023-02161 Rev A, 2024.
- CCSDS. [Publications](https://public.ccsds.org/).

---

> **Nota de responsabilidade:** este glossário contém conteúdo educacional independente baseado em fontes públicas. Não contém dados de clientes, informações do empregador, credenciais, topologias reais, detalhes operacionais sensíveis ou instruções para comprometer, interferir ou interromper sistemas espaciais ou de comunicação.
