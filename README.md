# Desafio Excel - Planilha de Investimento DIO

## ⚙️ BASE ESTRUTURAL

## 📖 — 1. Descrição

Este projeto foi desenvolvido como parte de um desafio voltado para a aplicação de fórmulas e formatação condicional no Excel. A ideia central é possibilitar a identificação do perfil de investidor, analisando o tempo de investimento informado dentro de uma tabela de cenários. Com essa abordagem, busca-se estabelecer critérios que permitam categorizar investidores com base no período que pretendem manter seus recursos aplicados, facilitando a tomada de decisão e aprimorando a visualização dos diferentes perfis financeiros.

## 💹 — 2. Qual a estrutura da planilha?

A planilha apresenta uma tabela estruturada com as seguintes informações:

- **Cenários de Projeção:** O usuário pode obter uma estimativa do montante esperado após um determinado período, formulando a pergunta: "Quanto em X meses?". No entanto, para uma visão mais estratégica e abrangente, são incluídas projeções anuais considerando horizontes temporais de 1, 2, 5, 15 e 20 anos;

- **Patrimônio Acumulado:** Refere-se à estimativa do valor total projetado ao final do período estipulado. Essa análise é realizada por meio do cálculo do "Valor projetado ao término do intervalo determinado", sendo apresentada em escalas anuais para permitir uma melhor compreensão da evolução patrimonial ao longo dos anos;

- **Rendimento Obtido:** Representa a soma dos ganhos acumulados ao longo do período em questão. Esse aspecto é avaliado por meio da análise do "Valor total do rendimento gerado", com foco nos cálculos anuais, proporcionando uma visão clara sobre os retornos brutos adquiridos ao longo do tempo.

### 2.1. Amostra de dados (Perfil Conservador):

| Cenários           | Patrimônio Acumulado | Rendimento  |
|--------------------|----------------------|-------------|
| Quanto em 1 ano?   | R$ 12.633,23         | R$ 117,49   |
| Quanto em 2 anos?  | R$ 26.750,73         | R$ 247,78   |
| Quanto em 5 anos?  | R$ 79.857,52         | R$ 742,67   |
| Quanto em 15 anos? | R$ 461.543,83        | R$ 4.292,36 |
| Quanto em 20 anos? | R$ 884.178,41        | R$ 8.222,86 |

### 2.2. Perfil de Investimento Mensal

O Investimento Mensal acima mostrado se refere a um valor fixo de R$ 1.000,00, ao qual anexei ao perfil **"Conservador"**. No entanto, existe na planilha valores que são alusivos a outros dois perfis que igualmente são analisados, sendo, o perfil **"Moderado"** com valor fixo de R$ 2.000,00 e, o perfil **"Agressivo"** com valor fixo de R$ 2.500,00.
Ambos os perfis refletem de forma interativa na tabela, refletindo os ganhos finais mensais e o acumulado, assim como no patrimônio e rendimentos anuais de cada valor que é investido.

---

## 💠 CONTEXTO FOCAL

## 👁️‍🗨️ — 3. Perfis de Investidor (nas células mescladas `D32` & `D33`):

- **Investidor Conservador** – faixa de valores entre R$ 1.000,00 e R$ 1.999,99, priorizando segurança e estabilidade;
- **Investidor Moderado** – valores variando de R$ 2.000,00 a R$ 2.499,99, equilibrando risco e retorno de forma estratégica;
- **Investidor Agressivo** – montantes a partir de R$ 2.500,00, focando em alto potencial de valorização e maior exposição ao risco.

### 3.1. Construção do Modelo:

As células `D32` e `D33` analisam a quantidade do valor investido com base no perfil do investidor, usando a fórmula:

```excel
==SE(D32="Conservador"; 1000;
 SE(D32="Moderado"; 2000;
 SE(D32="Agressivo"; 2500; 0)))
```

Esse retorno beneficia a transparência dos Tipos de FII, que são o ponto focal da análise, trazendo o percentual de maneira demonstrativa, representando a quantidade investida. 
No mais, o investimento mensal, anteriormente proposto, demonstra as informações de dividendos e patrimônio com base na taxa percentual do período, ao qual vinculei a 0,93% pelo período de 120 meses (10 anos).

---

## 📌 CONCLUSÃO

## 💱 — 4. Proposta da Planilha

- Permitir uma clareza de informações quanto a um salário X, precificado em análise a R$ 5.000,00, com a recomendação de perfis a se investir com seus devidos valores. De maneira conservadora a um valor de 20%, a valor moderado com 45% e, um valor agressivo a valor de 50% do salário;
- Demonstrar de maneira transparente, o patrimônio que se pode acumular durante 10 anos (120 meses) com uma taxa de 0,93% alusiva ao valor atual da análise, com dividendos mensais gerados a partir do patrimônio pela taxa em %;
- Oferecer uma carteira onde aquele que vá investir, entenda os perfis com base naquele que melhor se adequa a sua realidade, com os devidos investimentos que trazem maior rentabilidade;

## ➗ — 5. Construção

- Microsoft Excel;
- Fórmula SE;
- Fórmula PROCV;
- Validação de Dados em 2 niveis;

## 🔔 — 6. Agradecimento

Agradecimento ao Sérgio Sousa que disponibilizou no fórum seu link anexo no github, ao qual me inspirou a construir o meu README aqui. Link de Acesso:
https://github.com/SergioDevSousa/planilha-analise-exel/blob/main/README.md?plain=1

## 🗂️ — 7. Anexo do Arquivo
[Clique aqui para baixar](./investimento%20DIO.xlsx)
