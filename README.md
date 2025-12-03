## RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS (MIGRAÇÃO) 🚀

Data: 03/12/2025
Empresa: **Abstergo Industries**
Responsável: **Willian Ferreira**

---

## Introdução
Este relatório apresenta a proposta de implementação inicial e migração para a AWS da empresa **Abstergo Industries**, uma farmácia que atualmente opera com infraestrutura **on-premises**. O objetivo é elencar **3 serviços AWS** que promovam a **eliminação de custos fixos de hardware**, aumentem a **segurança** e garantam a **continuidade do negócio**, representando uma redução de custos a longo prazo.

---

## Descrição do Projeto
O projeto de migração para a nuvem será dividido em 3 etapas, focadas em mover a farmácia de um modelo *on-premises* (baseado em hardware próprio) para um modelo *cloud-native*.

### Etapa 1: Migração do Servidor de Aplicação
- **Nome da ferramenta:** **Amazon Lightsail**
- **Foco da ferramenta:** **Migração rápida e barata** de servidores de aplicação e *websites* simples (e.g., sistema de gestão e vendas básico) para a nuvem, com **custos fixos e previsíveis**.
- **Descrição de caso de uso:**

  A Abstergo Industries hoje opera seu sistema de gestão de estoque e vendas em um servidor físico local. A migração desse servidor para o **Amazon Lightsail** permite que a farmácia obtenha um Servidor Privado Virtual (VPS) pronto para uso, com preço mensal fixo e baixo (começando em $3.50/mês). Isso elimina imediatamente a necessidade de manutenção, energia e refrigeração do servidor físico local. O Lightsail simplifica a transição de um ambiente local para a nuvem.

  * **Ganho de Custo:** **Eliminação imediata do Capex** (compra de hardware) e redução de custos operacionais (energia, manutenção local, *downtime* não planejado) com um custo mensal de nuvem baixo e transparente.

---

### Etapa 2: Backup e Recuperação de Desastres
- **Nome da ferramenta:** **AWS Backup** e **Amazon S3**
- **Foco da ferramenta:** **Segurança e continuidade do negócio** através de *backups* automatizados e **Recuperação de Desastres (DR)** fora do local físico da farmácia.
- **Descrição de caso de uso:**

  A farmácia armazena dados críticos (como registros de pacientes e transações financeiras) em discos locais, o que os torna vulneráveis a incêndios, falhas de hardware ou *ransomware*. O **AWS Backup** permite a criação de cópias seguras e automatizadas desses dados diretamente no **Amazon S3** (armazenamento durável e barato). Isso resolve o problema de **Recuperação de Desastres**, garantindo que, em caso de falha total do servidor local, o negócio possa ser restaurado rapidamente, atendendo a requisitos regulatórios.

  * **Ganho de Custo:** **Redução do risco financeiro** devido a perda de dados e multas regulatórias. O custo de armazenamento no S3 é exponencialmente menor do que o custo de adquirir e manter um segundo *datacenter* para DR.



---

### Etapa 3: Modernização de Banco de Dados
- **Nome da ferramenta:** **Amazon Relational Database Service (RDS) - PostgreSQL/MySQL**
- **Foco da ferramenta:** **Performance, escalabilidade e gerenciamento de banco de dados**, eliminando a necessidade de um DBA (Administrador de Banco de Dados) interno.
- **Descrição de caso de uso:**

  O banco de dados local da farmácia (que armazena todo o catálogo, preços e histórico de vendas) exige manutenção constante e *patches* de segurança. Migrar esse banco de dados para o **Amazon RDS** significa que a AWS passa a gerenciar tarefas tediosas e caras, como *patching*, *backups* automáticos, monitoramento de falhas e *failovers*. Isso **libera tempo** da equipe de TI (ou do responsável técnico) para focar em tarefas de maior valor para o negócio.

  * **Ganho de Custo:** **Redução de custos com pessoal** (funções de DBA são caras) e eliminação do custo de **licenciamento de *softwares*** de banco de dados (se migrado para opções de código aberto como PostgreSQL ou MySQL).

---

## Conclusão
A implementação inicial dos serviços AWS na empresa **Abstergo Industries** tem como esperado **a eliminação da dependência de hardware físico local (Capex), a obtenção de uma infraestrutura de TI mais segura e resiliente, e a redução drástica dos custos de manutenção e administração de sistemas (Opex)**. O caminho da migração proporciona à farmácia escalabilidade futura e agilidade para lançar novos serviços online. Recomenda-se a imediata formalização das etapas de migração, começando pela avaliação de *backups* e DR.

---

## Anexos

* Planilha de Custo Total de Propriedade (TCO) comparando *on-premises* vs. AWS (Lightsail/RDS).
* Guia de *sizing* para instâncias do Amazon Lightsail.
* Políticas de Backup e Retenção de Dados no AWS Backup.

Assinatura do Responsável pelo Projeto:

Willian Ferreira
