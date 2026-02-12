Plano de DevSecOps

VittaHub – Portal Seguro de Boletins Médicos

1. Objetivo do Plano de DevSecOps

Este Plano de DevSecOps tem como objetivo integrar segurança da informação, automação e governança ao ciclo completo de desenvolvimento e operação do VittaHub, garantindo que requisitos de confidencialidade, integridade, disponibilidade e conformidade regulatória sejam atendidos desde a concepção até a operação do sistema.

A abordagem DevSecOps adotada busca eliminar o modelo tradicional no qual a segurança é tratada apenas ao final do desenvolvimento, promovendo uma cultura de segurança contínua, preventiva e automatizada.

2. Controles de Segurança no Pipeline (CI/CD)

O pipeline de Integração Contínua e Entrega Contínua (CI/CD) incorpora controles de segurança automatizados em todas as etapas:

2.1 Controles no Commit e Build

Versionamento obrigatório em repositório Git

Pull Requests com revisão técnica obrigatória

Bloqueio de merge sem aprovação

Execução automática de:

Build do backend e frontend

Testes unitários

Testes de integração

2.2 Controles de Segurança Automatizados

Análise estática de código (SAST)

Verificação de vulnerabilidades em dependências

Avaliação de qualidade e cobertura de código

Interrupção automática do pipeline em caso de falhas críticas (fail-fast)

2.3 Controles no Deploy

Deploy automatizado e padronizado via containers

Separação de ambientes (Dev, Homologação e Produção)

Uso de variáveis seguras para segredos e credenciais

Registro de logs e trilhas de auditoria do processo de deploy

3. Ferramentas Utilizadas

As ferramentas foram selecionadas com base em maturidade, integração com pipelines modernos e aderência a ambientes regulados:

3.1 Pipeline e Automação

GitHub Actions – Orquestração de CI/CD

Docker – Empacotamento padronizado da aplicação

Infraestrutura em nuvem – Ambientes segregados e escaláveis

3.2 Segurança e Qualidade

SonarQube – Análise estática de código (SAST) e qualidade

Ferramentas de verificação de dependências (Dependency Check)

TLS/SSL – Criptografia de comunicação

Gestão segura de segredos (Secrets Manager)

3.3 Monitoramento e Observabilidade

Centralização de logs

Dashboards de métricas

Alertas automáticos de falhas e comportamentos anômalos

4. Papéis e Responsabilidades

A segurança é tratada como responsabilidade compartilhada, com papéis bem definidos:

Papel	Responsabilidades
Desenvolvedores	Código seguro, correção de vulnerabilidades, revisão de código
Tech Lead	Garantir padrões de segurança, arquitetura e qualidade
Security Officer / CISO	Definir políticas de segurança e controles
DevOps Engineer	Manutenção do pipeline, automação e infraestrutura
Product Owner	Priorizar requisitos de segurança no backlog
Governança / Compliance	Auditorias, conformidade regulatória e gestão de riscos
5. Integração com Governança e Compliance

O DevSecOps está integrado diretamente ao modelo de governança digital do projeto:

Alinhamento com LGPD (Art. 46 – Segurança)

Aderência às normas ISO 27001 e ISO 27002

Auditorias técnicas periódicas

Logs de acesso e alterações com rastreabilidade

Revisões regulares de riscos e controles

Integração com o Comitê de Governança e Change Control Board (CCB)

Essa integração garante que decisões técnicas estejam sempre alinhadas aos requisitos legais, éticos e estratégicos do produto.

6. Descrição das Práticas de Segurança Aplicadas
6.1 Segurança desde o Design (Security by Design)

Princípios de menor privilégio

Minimização de dados sensíveis

Separação clara de responsabilidades

Camada Anti-Corrupção para isolamento de sistemas legados

6.2 Segurança no Desenvolvimento

Revisões de código obrigatórias

Padrões OWASP Top 10

Testes automatizados de segurança

Definition of Done incluindo critérios de segurança

7. SAST, Controle de Dependências e Revisão de Código
7.1 SAST – Static Application Security Testing

Análise automática do código-fonte a cada commit

Identificação precoce de falhas como:

Injeção de código

Uso inseguro de bibliotecas

Exposição de dados sensíveis

7.2 Controle de Dependências

Verificação contínua de bibliotecas vulneráveis

Atualização controlada de dependências

Bloqueio de builds com dependências críticas vulneráveis

7.3 Revisão de Código

Pull Requests obrigatórios

Revisão técnica por pares

Validação de requisitos funcionais e não funcionais (segurança e privacidade)

8. Monitoramento, Auditoria e Resposta a Incidentes
8.1 Monitoramento Contínuo

Monitoramento de disponibilidade e performance

Detecção de comportamentos anômalos

Alertas automáticos para falhas críticas

8.2 Auditoria

Logs imutáveis de acesso e operações

Trilhas completas de auditoria

Conformidade com requisitos do Marco Civil da Internet e LGPD

8.3 Resposta a Incidentes

Processo formal de gestão de incidentes

Classificação por severidade

Comunicação rápida com stakeholders

Registro e análise pós-incidente (lições aprendidas)

9. Uso de Red Team, Blue Team e Purple Team
9.1 Red Team

Simulação de ataques reais

Testes de intrusão (pentest)

Avaliação de superfícies de ataque

Identificação de vulnerabilidades exploráveis

9.2 Blue Team

Monitoramento ativo de sistemas

Análise de logs e alertas

Resposta a incidentes

Correção e mitigação de vulnerabilidades

9.3 Purple Team

Integração entre Red e Blue Team

Compartilhamento de aprendizados

Ajustes contínuos nos controles de segurança

Evolução constante da postura defensiva

10. Conclusão

A adoção do DevSecOps no VittaHub garante que segurança, qualidade e conformidade sejam tratadas como pilares estratégicos do produto.
Essa abordagem reduz riscos técnicos e legais, aumenta a confiabilidade do sistema e sustenta a escalabilidade do produto em um ambiente hospitalar altamente regulado.
