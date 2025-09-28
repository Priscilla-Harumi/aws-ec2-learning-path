# Jornada de Aprendizado AWS

Este repositório documenta minha jornada de estudos AWS (Amazon Web Services). Cada tópico contém o que aprendi de forma resumida e direta.

---

## Fundamentos

**Regiões da AWS**  
Aprendi que a AWS está dividida em regiões geográficas independentes. Cada região contém data centers físicos que oferecem redundância e menor latência.

**Zonas de Disponibilidade (AZs)**  
AZs são centros de dados dentro de uma região, separados para alta disponibilidade. Entendi que distribuir recursos entre AZs ajuda a evitar falhas.

**Serviços gerenciados**  
Serviços como RDS, S3 e Lambda permitem que a AWS cuide da infraestrutura, escalabilidade e manutenção, permitindo foco na aplicação.

**Criação de conta**  
Configurei minha conta AWS, incluindo informações de pagamento, verificação de identidade e habilitação de recursos básicos.

**Práticas de segurança**  
Aprendi sobre boas práticas como habilitar MFA, usar senhas fortes e limitar privilégios de usuários.

**IAM e políticas**  
IAM permite criar usuários, grupos e permissões. Compreendi como definir políticas que controlam acesso a recursos de forma granular.

**IAM Identity Center**  
Conheci o Identity Center (antigo AWS SSO) para gerenciar acesso centralizado a múltiplas contas AWS.

**SCPs (Service Control Policies)**  
SCPs são políticas aplicadas em nível de conta para restringir ações, mesmo para administradores.

**Controle de gastos e alertas**  
Aprendi a criar alertas no AWS Budgets e acompanhar o uso para não ter surpresas na fatura.

**Formas de acesso (Console, CloudShell, CLI)**  
Entendi as diferenças entre acessar a AWS via Console Web, CLI (linha de comando) e CloudShell, escolhendo a ferramenta certa para cada necessidade.

**Automatização: CLI + CSV (criação de usuários)**  
Aprendi a criar múltiplos usuários e configurar permissões usando scripts e arquivos CSV, economizando tempo.

---

## Computação

**EC2 - conceitos**  
EC2 é o serviço de máquinas virtuais da AWS. Compreendi a diferença entre instâncias, AMIs e tipos de armazenamento.

**Tipos de instância EC2**  
Existem instâncias otimizadas para computação, memória ou armazenamento. Aprendi a escolher a melhor opção conforme a necessidade.

**Otimização de recursos**  
Aprendi a monitorar uso de CPU, memória e rede para ajustar instâncias, economizando custos e aumentando desempenho.

**EBS (Elastic Block Store)**  
EBS fornece armazenamento persistente para EC2. Entendi como criar, anexar e redimensionar volumes.

**AMI (Amazon Machine Image)**  
AMIs permitem criar imagens de máquinas prontas para replicação ou backup rápido.

**Snapshots EBS**  
Aprendi a tirar snapshots de volumes para backup e restauração, garantindo segurança dos dados.

---

## Armazenamento

### S3 e classes de armazenamento
O Amazon S3 é um serviço de **armazenamento de objetos** escalável, seguro e altamente disponível, ideal para guardar arquivos, backups, logs ou qualquer dado que precise ser acessado de forma confiável. Cada objeto é armazenado dentro de **buckets**, que funcionam como pastas de alto nível.

Aprendi sobre as principais **classes de armazenamento**, que ajudam a equilibrar custo e desempenho:

- **Standard**: para dados acessados com frequência. Alta disponibilidade e tempo de acesso rápido, porém mais cara. Ideal para aplicativos ativos e arquivos que precisam ser lidos e gravados constantemente.  
- **Standard-Infrequent Access (IA)**: para dados acessados menos frequentemente, mas que ainda precisam de rápida recuperação. Mais barata que a Standard, mas há custo para acesso. Boa para backups ou arquivos antigos que podem ser consultados eventualmente.  
- **Glacier**: para **arquivamento de longo prazo**. Muito econômica, mas o tempo de recuperação pode levar minutos ou horas. Perfeita para históricos, logs antigos ou dados de compliance.  
- **Glacier Deep Archive**: ainda mais barata que Glacier, destinada a dados raramente acessados. A recuperação pode levar até 12 horas.

Também aprendi que é possível **mover objetos entre classes automaticamente** usando regras de ciclo de vida (lifecycle policies), permitindo otimizar custos sem perder dados importantes.


---

## Arquitetura

**Desenho de arquitetura com diagrams.net**  
Aprendi a criar diagramas de arquitetura claros, facilitando a visualização de fluxos, serviços e dependências.
