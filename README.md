## RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS 💊

Data: 03/12/2025
Empresa: **Abstergo Industries**
Responsável: **Willian Ferreira**

---

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, uma **farmácia fictícia**, realizado por Willian Ferreira. O objetivo do projeto foi elencar **3 serviços AWS** com foco na **diminuição imediata de custos** operacionais.

---

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma focada em um serviço AWS distinto para otimização de custos, conforme a necessidade da gestão financeira.

### Etapa 1: Otimização de Armazenamento
- **Nome da ferramenta:** **Amazon S3 Glacier Instant Retrieval**
- **Foco da ferramenta:** **Redução de custos de armazenamento** para dados acessados com pouca frequência, mas que precisam estar disponíveis rapidamente quando solicitados (e.g., registros de vendas antigos, histórico de pedidos de clientes, documentos fiscais anuais).
- **Descrição de caso de uso:**

  A Abstergo Industries armazena um grande volume de **dados históricos** (como registros de transações de mais de 6 meses) no **Amazon S3 Standard**. Apesar de raramente acessados, esses dados geram um custo de armazenamento elevado.

  A migração desses dados para o **S3 Glacier Instant Retrieval** permite uma redução significativa no custo de armazenamento por GB (aproximadamente 70-80% menos que o S3 Standard), mantendo a **latência de recuperação em milissegundos**, caso o gerente financeiro ou a área de compliance precise acessar rapidamente um registro antigo.

  * **Ganho de Custo:** Economia mensal substancial no custo de armazenamento, transferindo dados "frios" para uma classe de armazenamento mais barata, sem comprometer a disponibilidade para buscas rápidas.

---

### Etapa 2: Otimização de Infraestrutura de Servidores
- **Nome da ferramenta:** **Amazon EC2 Savings Plans**
- **Foco da ferramenta:** **Redução de custos de computação** por meio do compromisso de uso contínuo de recursos EC2.
- **Descrição de caso de uso:**

  A farmácia utiliza instâncias **Amazon EC2** para hospedar seu sistema de gestão de estoque, plataforma de vendas online e banco de dados. Foi identificado um **uso constante** (24/7) de instâncias básicas, mesmo que a carga de trabalho varie.

  A aquisição de um **EC2 Savings Plan** de 1 ano, comprometendo-se com um determinado gasto por hora em dólares (por exemplo, $5/hora de uso de computação), resulta em descontos significativos nas faturas do EC2 (até **66%** de desconto em comparação com o preço *On-Demand*). Este plano oferece flexibilidade de uso entre diferentes famílias, tamanhos, regiões e sistemas operacionais de EC2, maximizando a economia.

  * **Ganho de Custo:** Diminuição imediata da taxa horária de instâncias EC2 utilizadas de forma contínua, transformando despesas variáveis em despesas previsíveis e com desconto.



---

### Etapa 3: Otimização de Recursos Ociosos
- **Nome da ferramenta:** **AWS Compute Optimizer**
- **Foco da ferramenta:** **Identificação e redimensionamento** de recursos superdimensionados (provisionamento excessivo) e ociosos, gerando recomendações específicas de economia.
- **Descrição de caso de uso:**

  Muitas vezes, as instâncias EC2 e os volumes EBS são provisionados com mais CPU e memória do que o necessário, resultando em "desperdício" de recursos (o recurso está pago, mas não está sendo utilizado). O **Compute Optimizer** analisa as métricas históricas de utilização da Abstergo Industries e recomenda o **tamanho de instância EC2 ideal** (como mudar de uma `m5.large` para uma `t3.medium`) e o **tipo/tamanho de volume EBS** mais eficiente para a carga de trabalho real.

  A aplicação dessas recomendações de redimensionamento pode levar a uma redução de **10-30%** nos custos de computação e armazenamento sem afetar o desempenho.

  * **Ganho de Custo:** Redução dos custos de instâncias e volumes de armazenamento/IOPS, garantindo que a farmácia pague apenas pelo poder de processamento e armazenamento que realmente utiliza.

---

## Conclusão
A implementação de ferramentas na empresa **Abstergo Industries** tem como esperado **a obtenção de descontos significativos no custo de armazenamento de dados (S3 Glacier Instant Retrieval), uma redução substancial nas taxas horárias de computação EC2 por meio de compromissos de uso (Savings Plans) e a eliminação de desperdício financeiro através da identificação e redimensionamento de recursos ociosos (Compute Optimizer)**, o que aumentará a eficiência e a produtividade financeira da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa, com foco em migração para arquiteturas *serverless* no futuro.

---

## Anexos

* Planilha de análise de TCO (Custo Total de Propriedade) projetado com a aplicação dos Savings Plans.
* Relatório de recomendações de redimensionamento gerado pelo AWS Compute Optimizer.
* Guia de migração de dados do S3 Standard para o S3 Glacier Instant Retrieval.

Assinatura do Responsável pelo Projeto:

Willian Ferreira
