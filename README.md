# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

- Data: 13/02/2025
- Empresa: Abstergo Industries
- Responsável: Marcos Vinicius Alves de Souza

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Marcos Vinicius Alves de Souza. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:

Etapa 1:
- Nome da ferramenta: AWS Compute Optimizer
- Foco da ferramenta: Rightsizing de recursos de compute (principalmente instâncias EC2, Auto Scaling Groups, volumes EBS e funções Lambda)
- Descrição de caso de uso: Identificação automática de instâncias EC2 superdimensionadas (over-provisioned) ou subutilizadas, recomendando tipos/tamanhos menores ou remoção de recursos ociosos. Na Abstergo Industries, foram identificadas diversas instâncias com utilização média de CPU abaixo de 20–30% durante semanas. Após aplicação das recomendações de downsizing e exclusão de recursos não utilizados (ex.: volumes EBS órfãos), obteve-se redução imediata de cerca de 25–35% nos custos de compute em menos de 30 dias, sem impacto perceptível na performance das aplicações críticas.

Etapa 2:
- Nome da ferramenta: AWS Savings Plans
- Foco da ferramenta: Descontos flexíveis em uso de compute (EC2, Lambda, Fargate)
- Descrição de caso de uso: Compromisso de gasto horário (ex.: Compute Savings Plans) em troca de descontos de até 66–72% comparado ao preço On-Demand, com grande flexibilidade de família de instâncias, região e serviços. Na Abstergo, analisou-se o histórico de uso via Cost Explorer e adquiriu-se um Savings Plan Compute de 1 ano (no modelo No Upfront). Isso cobriu grande parte do uso recorrente de EC2 e Lambda, gerando economia imediata de aproximadamente 40–55% sobre a parcela comprometida a partir do primeiro mês de vigência, sem necessidade de alterar a arquitetura existente.

Etapa 3:
- Nome da ferramenta: Amazon EC2 Spot Instances
- Foco da ferramenta: Uso de capacidade sobressalente da AWS com descontos de até 90%
- Descrição de caso de uso: Substituição de instâncias On-Demand por Spot em workloads tolerantes a interrupções, como processamento em batch, renderização, machine learning training, testes/CI/CD e ambientes de desenvolvimento/QA. Na Abstergo Industries, cerca de 35% das cargas de processamento não-crítico (análises de dados, jobs ETL noturnos e ambientes de staging) foram migradas para Spot Instances com estratégias de fallback para On-Demand. Resultado: redução média de 65–85% nesses workloads específicos, com economia material já observada na primeira fatura após a implementação.

## Conclusão
A implementação de ferramentas na empresa Abstergo Industries tem como esperado redução imediata de 30–50% nos custos de infraestrutura AWS (dependendo da proporção de cada workload), aumento da eficiência operacional por meio de recursos dimensionados corretamente e maior previsibilidade orçamentária. Isso permitirá realocar verba para iniciativas estratégicas, como expansão de novos produtos e adoção de tecnologias emergentes. Recomenda-se a continuidade da utilização das ferramentas implementadas, monitoramento contínuo via AWS Cost Optimization Hub e AWS Cost Explorer, além da busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

Assinatura do responsável pelo Projeto:


Marcos Vinicius Alves de Souza
