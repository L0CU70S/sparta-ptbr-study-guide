# SPARTA e Modelagem de Ameaças: um guia introdutório

[🇺🇸 English](../README.md) · [🇧🇷 Início em Português](../README.pt-BR.md) · [← O que é SPARTA?](01-o-que-e-sparta.md) · [← Como ler a matriz SPARTA](04-como-ler-a-matriz-sparta.md)

> **Material educacional independente e não oficial.**
>
> Este documento não é afiliado, endossado, mantido ou patrocinado pela The Aerospace Corporation, pelo projeto SPARTA, pelo NIST, pela CCSDS ou por qualquer agência espacial. Em caso de divergência, a fonte oficial em inglês prevalece.

## Objetivo

Este documento apresenta uma forma introdutória e defensiva de usar o **SPARTA — Space Attack Research and Tactic Analysis** como apoio à modelagem de ameaças (*threat modeling*) de um sistema espacial fictício.

A proposta não é transformar o SPARTA em uma checklist automática ou tentar mapear todas as técnicas de uma missão. O objetivo é aprender a conectar objetivo de missão, ativos, arquitetura, ameaças, riscos, contramedidas, controles e requisitos de segurança.

## O que é modelagem de ameaças?

Modelagem de ameaças é um processo estruturado para responder perguntas como:

- O que estamos protegendo?
- Por que esse ativo ou função importa para a missão?
- Quais eventos ou comportamentos adversários podem afetá-lo?
- Que condições permitiriam esse cenário?
- Qual seria o impacto em confidencialidade, integridade, disponibilidade e sucesso da missão?
- Quais contramedidas e controles podem reduzir o risco?
- Como validar, monitorar e responder caso algo dê errado?

Uma boa modelagem de ameaças não começa por uma ferramenta ou por uma técnica. Ela começa pelo entendimento do sistema e do objetivo da missão.

## Onde o SPARTA entra

O SPARTA pode ser usado como uma fonte de conhecimento para enriquecer a etapa de identificação de ameaças. Depois que você entende o cenário, consulta técnicas e subtécnicas que possam ser relevantes, registra hipóteses e relaciona essas hipóteses a contramedidas e controles.

A sequência recomendada é:

```text
Objetivo da missão
       ↓
Ativos e funções críticas
       ↓
Segmentos, interfaces e fluxos de dados
       ↓
Fronteiras de confiança e premissas
       ↓
Cenários de ameaça relevantes
       ↓
Técnicas SPARTA potencialmente aplicáveis
       ↓
Avaliação de risco
       ↓
Contramedidas, controles e requisitos
       ↓
Monitoramento, resposta e validação
```

O perfil de cibersegurança do segmento espacial da Aerospace descreve um raciocínio semelhante: técnicas e subtécnicas são usadas para representar ameaças, contramedidas servem de ponte para controles, e controles podem ser transformados em requisitos de segurança orientados por risco. [^1]

## Passo 1 — Defina o cenário e o objetivo

Comece com um cenário limitado, fictício e claro. Evite criar uma “missão completa” logo no primeiro exercício.

### Exemplo fictício

> Uma organização acadêmica opera um pequeno satélite de observação da Terra. A missão possui uma estação terrena, um ambiente de operação de missão, servidores de processamento de telemetria, repositório de dados científicos e contas privilegiadas para operadores autorizados.

### Perguntas orientadoras

- Qual é o objetivo principal da missão?
- Quais dados ou funções devem permanecer disponíveis?
- Quem são os usuários e operadores autorizados?
- Quais componentes estão no Ground Segment, Link Segment, Space Segment e User Segment?
- O que a missão considera um impacto inaceitável?

## Passo 2 — Identifique ativos e funções críticas

Liste ativos sem usar nomes reais, IPs, domínios ou detalhes internos.

| Ativo ou função fictícia | Segmento | Por que é importante? | Impacto de comprometimento |
|---|---|---|---|
| Estação terrena | Ground Segment | Mantém comunicação operacional com o ativo espacial | Perda ou degradação de capacidade de comunicação |
| MOC | Ground Segment | Coordena operação, planejamento e acompanhamento de missão | Impacto sobre operações e tomada de decisão |
| Serviço de telemetria | Ground Segment | Recebe, processa e disponibiliza dados operacionais | Dados incompletos, atrasados ou potencialmente alterados |
| Contas privilegiadas de operadores | Ground Segment | Permitem atividades administrativas e operacionais autorizadas | Acesso indevido a funções sensíveis |
| Enlace de comunicação | Link Segment | Transporta dados e comandos entre componentes | Risco à disponibilidade, integridade e confidencialidade conforme a arquitetura |
| Computador de bordo | Space Segment | Executa funções embarcadas e software de voo | Impacto potencial em funções essenciais de missão |

## Passo 3 — Desenhe arquitetura, fluxos e fronteiras de confiança

Crie um diagrama simples antes de discutir técnicas. O diagrama deve mostrar:

- Segmentos de missão.
- Ativos principais.
- Fluxos de telemetria e telecomando em alto nível.
- Conexões entre ambiente corporativo, engenharia, operação e estação terrena.
- Contas e caminhos de acesso privilegiado.
- Sistemas que registram logs e eventos.
- Fronteiras de confiança, como redes segregadas, DMZs, bastions ou gateways.

Exemplo conceitual:

```text
[Usuários e aplicações]
          |
     User Segment
          |
[Ambiente corporativo] --- [Ambiente de engenharia]
          |                         |
          +------[MOC / Operações]--+
                        |
                [Estação terrena]
                        |
                  Link Segment
                        |
                [Ativo espacial]
                  Space Segment
```

Esse diagrama deve permanecer conceitual. Não use informações de ambientes reais, clientes ou empregadores.

## Passo 4 — Registre cenários de ameaça

Antes de consultar uma técnica específica, descreva eventos de alto nível que poderiam afetar a missão.

Exemplos defensivos:

- Uso indevido ou comprometimento de uma conta privilegiada de operador.
- Alteração não autorizada de configuração em um sistema de operação.
- Indisponibilidade de serviço que processa telemetria.
- Falha de segmentação entre ambiente corporativo e ambiente operacional.
- Acesso remoto de fornecedor sem controles adequados.
- Ausência de logs suficientes para investigar uma atividade anômala.
- Dependência de um único componente operacional sem plano de recuperação.

Esses cenários não são alegações sobre sistemas reais. São hipóteses usadas para orientar decisões defensivas.

## Passo 5 — Consulte SPARTA de forma contextual

Agora consulte a fonte oficial do SPARTA e selecione apenas técnicas ou subtécnicas que pareçam relevantes ao cenário.

Para cada item, registre:

| Campo | Como preencher |
|---|---|
| Referência SPARTA | ID, nome oficial em inglês e link para a fonte oficial |
| Cenário analisado | Descrição fictícia e defensiva do risco |
| Segmento(s) envolvido(s) | Ground, Link, Space, User ou combinação aplicável |
| Ativos afetados | Ativos e funções críticas previamente identificados |
| Pré-condições | Acessos, interfaces, falhas ou exposições necessárias |
| Impacto potencial | Efeito em confidencialidade, integridade, disponibilidade e missão |
| Contramedidas | Medidas defensivas relevantes em alto nível |
| Evidências possíveis | Logs, auditorias, testes, revisões ou indicadores úteis |
| Premissas e limitações | O que não é conhecido ou precisa ser validado |

A técnica é uma referência de análise; não é prova de incidente, vulnerabilidade confirmada ou aplicabilidade automática.

## Passo 6 — Avalie o risco

Uma avaliação simples pode usar impacto e probabilidade como ponto de partida:

\[
Risco = Impacto x Probabilidade
\]

A fórmula é apenas uma simplificação. Uma análise real também pode considerar criticidade da missão, capacidade e motivação do agente de ameaça, exposição, vulnerabilidades, controles existentes, detectabilidade e tolerância a risco.

Use uma escala qualitativa inicial:

| Critério | Baixo | Médio | Alto |
|---|---|---|---|
| Impacto | Afeta função não crítica e possui recuperação simples | Afeta operação relevante, com recuperação planejada | Afeta função essencial, segurança operacional ou sucesso da missão |
| Probabilidade | Exige condições improváveis ou controles fortes já existentes | Possível em condições específicas | Exposição relevante, controles insuficientes ou cenário plausível |
| Prioridade | Monitorar e revisar | Tratar com plano definido | Mitigar com prioridade e validar controles |

A Aerospace ressalta que risco deve considerar impacto e probabilidade, enquanto a criticidade e a tolerância a risco ajudam a orientar quais riscos exigem mitigação. [^1]

## Passo 7 — Transforme risco em defesa

A modelagem de ameaças precisa resultar em decisões práticas. Para cada risco priorizado, defina contramedidas, controles e evidências de implementação.

| Cenário fictício | Contramedidas defensivas de alto nível | Evidência esperada |
|---|---|---|
| Comprometimento de acesso privilegiado | MFA, PAM, menor privilégio, aprovação de acesso, auditoria de sessões e revisão periódica | Logs de autenticação, trilhas de auditoria, relatórios de acesso e procedimento aprovado |
| Alteração não autorizada de configuração | Gestão de mudanças, segregação de funções, controle de acesso, backup de configuração e alertas | Registro de mudança, logs de administração, baseline e evidências de revisão |
| Indisponibilidade de telemetria | Monitoramento de serviço, alertas, procedimentos de contingência, redundância conforme risco e testes de recuperação | Dashboard, alertas, resultados de teste e playbook |
| Falha de segmentação | Zonas, conduítes, firewall, regras revisadas, bastion e monitoramento de fluxos | Diagrama, regras aprovadas, logs e evidência de teste |

Essas medidas não garantem risco zero. Elas devem ser adaptadas à missão, aos ativos e às restrições técnicas e operacionais.

## Passo 8 — Planeje monitoramento, resposta e validação

Um controle só é mais confiável quando pode ser demonstrado e revisado.

Para cada cenário priorizado, defina:

- Que logs, métricas ou eventos podem indicar comportamento anômalo?
- Quem recebe o alerta e quem toma a decisão operacional?
- Como a investigação preserva evidências e evita piorar o impacto?
- Como a missão continua ou entra em modo de contingência, se necessário?
- Como o controle será testado: revisão, tabletop, teste de configuração ou simulação segura?
- Como as lições aprendidas serão incorporadas a requisitos, procedimentos e arquitetura?

Comece pequeno: um cenário, poucos ativos e uma única classe de risco. Um exercício limitado e bem justificado é mais valioso do que uma matriz extensa sem contexto.

## Checklist de qualidade

Antes de considerar um threat model concluído, verifique:

- [ ] O objetivo da missão está definido.
- [ ] Ativos e funções críticas foram identificados.
- [ ] Segmentos e fluxos principais foram representados.
- [ ] Fronteiras de confiança e premissas foram documentadas.
- [ ] Os cenários de ameaça são relevantes ao contexto.
- [ ] Referências SPARTA foram usadas como apoio, não como checklist automática.
- [ ] Impacto, probabilidade e prioridade foram justificados.
- [ ] Contramedidas e controles foram relacionados aos riscos.
- [ ] Existem ideias de monitoramento, resposta e validação.
- [ ] O material contém apenas dados fictícios ou publicamente disponíveis.
- [ ] O material não inclui instruções ofensivas ou de interferência em sistemas reais.

## Referências

[^1]: The Aerospace Corporation. *Space Segment Cybersecurity Profile for National Security Systems*, TOR-2023-02161 Rev A, 2024.

- The Aerospace Corporation. [SPARTA — Space Attack Research and Tactic Analysis](https://sparta.aerospace.org/).
- The Aerospace Corporation. [SPARTA FAQ](https://sparta.aerospace.org/resources/faq).
- Scholl, M.; Suloway, T. [NIST IR 8270 — Introduction to Cybersecurity for Commercial Satellite Operations](https://csrc.nist.gov/pubs/ir/8270/final), 2023.
- NIST. [SP 800-30 Rev. 1 — Guide for Conducting Risk Assessments](https://csrc.nist.gov/pubs/sp/800/30/r1/final).
- NIST. [SP 800-37 Rev. 2 — Risk Management Framework for Information Systems and Organizations](https://csrc.nist.gov/pubs/sp/800/37/r2/final).

---

> **Nota de responsabilidade:** este documento contém apenas conteúdo educacional independente baseado em fontes públicas. Não contém dados de clientes, informações do empregador, credenciais, topologias reais, detalhes operacionais sensíveis ou instruções para comprometer, interferir ou interromper sistemas espaciais ou de comunicação.
