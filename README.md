# Análise de Dados Bancários - Marketing Direto

Este projeto realiza uma análise exploratória completa de dados bancários relacionados a campanhas de marketing direto. O objetivo é identificar padrões, correlações e fatores que influenciam na aquisição de produtos bancários pelos clientes.

# Objetivos

- Analisar o perfil demográfico dos clientes (idade, profissão, estado civil);
- Investigar a relação entre variáveis financeiras (saldo bancário, empréstimos, inadimplência);
- Identificar correlações estatisticamente significativas;
- Calcular taxas de conversão por diferentes segmentos;
- Aplicar conceitos de probabilidade condicional.

# Fonte dos Dados

Dataset original: https://archive.ics.uci.edu/dataset/222/bank+marketing

# Metodologia

## Análise Exploratória (EDA)

- Estatísticas descritivas;
- Distribuição de frequências;
- Verificação de dados ausentes;
- Método IQR detalhado;
- Coeficiente de Pearson;
- Testes de significância;
- Probabilidade Condicional;

# Ferramentas Utilizadas

- Python (pandas, numby,matplotlib, seaborn);
- Google colaboratory;

# Resultados

**1. Análise Descritiva**

- **Distribuição de idade:** Nota-se a maior concentração de clientes está na faixa etária entre 30 e 40 anos.
  
<img width="1000" height="600" alt="Image" src="https://github.com/user-attachments/assets/39dcb23f-515d-4da5-99da-54066dc7a15d" />
  
- **Profissões mais comuns:** Management (21%), Blue-collar (21%), Technician (17%).
  
  <img width="1500" height="600" alt="Image" src="https://github.com/user-attachments/assets/f419ee04-ad5c-463e-a8f2-a3d1286f4317" />
  
- **Métodos de contato:** Cellular (64%), Unknown (29%), Telephone (7%).
  
<img width="1000" height="600" alt="Image" src="https://github.com/user-attachments/assets/948fe354-e3fc-49ce-9e71-27ddc6d2e204" />
  
- Após uma análise detalhada da correlação entre o saldo bancário e a idade dos clientes, não foi identificada uma correlação aparente. Para identificar e tratar os valores atípicos (outliers) na coluna de saldo bancário, foi empregado o método de Intervalo Interquartil (IQR). Foram **506** outliers removidos do dataset original e a nova base ficou com **4.015** registros.

<img width="1500" height="600" alt="Image" src="https://github.com/user-attachments/assets/cd77dc83-843b-4b75-83ab-1bef2a76fac5" />

- Gráfico com o tratamento de outliers.

  <img width="1500" height="600" alt="Image" src="https://github.com/user-attachments/assets/f88205f6-a390-4387-8528-82182f5ebbf4" />

- **Relação entre saldo e inadimplência, habitação e empréstimos:** Nota-se que clientes sem **inadimpência** (no) têm um saldo mediano mais alto e uma dispersão maior de saldo positivos, enquanto clientes com **inadimpência** (yes) tem uma mediana mais baixa. Um comportamento similar é observado em clientes com **casa** própria, aqueles que não têm um financiamento de habitação apresentam um saldo bancário maior em comparação com os que têm, o mesmo ocorre com clientes que tem algum tipo de **empréstimos**.

<img width="1800" height="600" alt="Image" src="https://github.com/user-attachments/assets/2c0f80fd-b8c0-4494-85e6-63e99e6c81aa" />

- Análise de aquisição do produto por clientes que tenham Inadimplência, Habitação e Empréstimos:
  - **Inadimplência:** Clientes inadimplentes têm uma taxa de aquisição de **12,2%**, 1 p.p. maior do que os que não são.
  - **Habitação:** Clientes sem empréstimo habitacional tem uma taxa de aquisição de **14,9%**. Tal informação sugere que clientes sem o comprometimento habitacional são mais propensos a adquirir o produto.
  - **Empréstimos:** Clientes sem empréstimos tem uma taxa de aquisição de **12,1%**, quase o dobro dos que possuem empréstimos. Isso demonstra que os clientes com sem o comprometimento de renda com empréstimos tem uma capacidade financeira maior.
 
 - **Correlação de Pearson**
  A correlação de Pearson é uma medida estatística que indica o grau de relaçai linear entre duas variáveis quantitativas. Quanto mais próximo de **1** demonstra que a variáveis tem uma relação positiva forte.
    - Valores próximos de +1: Correlação positiva forte;
    - Valores próximos de -1: Correlação negativa forte;
    - Valores próximos de 0: Correlação fraca ou inexistente.
  
  O mapa de calor mostra que idade e saldo têm uma correlação positiva muito fraca (r = 0.066). Embora estatisticamente significativa, essa relação indica que a idade tem influência mínima no saldo. Outros fatores provavelmente são muito mais determinantes para o saldo dos clientes.

<img width="800" height="600" alt="Image" src="https://github.com/user-attachments/assets/6ab66ee1-d3b6-43b2-934c-30399fb3cfdf" />

O heatmap abaixo demonstra que educação superior (tertiary) consistentemente produz as maiores taxas de conversão em ambos os grupos. Enquanto o cliente tem empréstimos reduz a capacidade de conversão do produto oferecido.

<img width="1200" height="800" alt="Image" src="https://github.com/user-attachments/assets/f9e08249-57e7-4023-a0cf-3748f302bb19" />

**Probabilidade Condicional:** A probabilidade condicional é a probabilidade de um evento ocorrer dado que outro evento já ocorreu. É escrita como P(A|B) e lida como "probabilidade de A dado B".

A análise da probabilidade condicional P(Conversão|Contato Anterior) revelou que **22%** dos clientes com pelo menos um contato prévio converteram no produto atual. Este resultado indica que contatos anteriores têm impacto positivo na conversão.

---
**Autor:** Rafael Sperança

**Ano:** 2025
