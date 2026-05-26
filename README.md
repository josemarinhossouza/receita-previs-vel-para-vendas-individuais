# Receita Previsível (Aaron Ross) — Simulador de Projeção B2B

Este repositório contém um protótipo de script voltado para a projeção de receita esperada com base na metodologia do livro **"Receita Previsível"**, de Aaron Ross.

---

### Como Funciona

* **Modelo B2B focado em Funil:** O processo de venda é estruturado em etapas de funil até que o lead seja classificado como comprador ideal e feche o negócio.
* **Escalabilidade Adaptável:** Atualmente, o indicador está adaptado para a realidade de um **único vendedor**, mas a lógica pode ser facilmente expandida para uma equipe inteira de vendas.
* **Venda Consultiva & Qualificação Real:** O vendedor trabalha os leads em um processo consultivo contínuo. O contato é cultivado até que o lead demonstre real intenção de fechar negócio. **Somente nesse momento ele é contado como Lead Qualificado Ativo (LQ).** Isso elimina leads frios do cálculo e torna a projeção significativamente mais confiável.
* **Valores Históricos vs. Operação Diária:**
    * Os **VALORES FIXOS** vêm do histórico de vendas e devem ser alterados apenas quando o histórico apresentar uma mudança significativa.
    * O **ÚNICO** valor que você altera no dia a dia operacional é o **LQ** (leads ativos agora).
* **Visões de Receita:** O código apresenta duas receitas previsíveis:
    * **R ciclo:** É a receita previsível no intervalo de uma venda para outra (seja em dias, semanas ou meses) para a venda de qualquer cliente.
    * **R 30 dias:** É a receita previsível estimada especificamente para o fechamento do mês.

---

### Fórmulas Utilizadas

| Indicador | Descrição | Fórmula |
| :--- | :--- | :--- |
| **E** | Eficiência | `Vendas realizadas / Leads históricos` |
| **TM** | Ticket Médio | `Total em R$ / Quantidade de vendas` |
| **PP** | Período Projetado | `30 dias / Ciclo médio` |
| **R ciclo** | Receita por Ciclo | `LQ × E × TM` |
| **R 30 dias** | Receita Mensal | `LQ × E × TM × PP` |
