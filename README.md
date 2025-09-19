# 📊 Análise de Dados Bancários - Marketing Direto

Este projeto realiza uma análise exploratória completa de dados bancários relacionados a campanhas de marketing direto. O objetivo é identificar padrões, correlações e fatores que influenciam na aquisição de produtos bancários pelos clientes.

# 🎯 Objetivos

- Analisar o perfil demográfico dos clientes (idade, profissão, estado civil)
- Investigar a relação entre variáveis financeiras (saldo bancário, empréstimos, inadimplência)
- Identificar correlações estatisticamente significativas
- Calcular taxas de conversão por diferentes segmentos
- Aplicar conceitos de probabilidade condicional

# Fonte dos Dados

Dataset original: https://archive.ics.uci.edu/dataset/222/bank+marketing

# 🔍 Principais Análises Realizadas

**1. Análise Descritiva**

**Distribuição de idade:** Análise da faixa etária dos clientes
**Profissões mais comuns:** Management (21%), Blue-collar (21%), Technician (17%)
**Métodos de contato:** Cellular (64%), Unknown (29%), Telephone (7%)

**2. Tratamento de Outliers**

- Após uma análise detalhada da correlação entre o saldo bancário e a idade dos clientes, não foi identificada uma correlação aparente.
- Identificação de outliers no saldo bancário usando método IQR
- 506 outliers removidos do dataset original
- Dataset filtrado: 4.015 registros
