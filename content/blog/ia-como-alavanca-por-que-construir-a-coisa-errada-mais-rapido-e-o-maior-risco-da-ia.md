---
title: "IA como Alavanca (Parte 4 de 7): Por que Construir a 'Coisa Errada' Mais Rápido é o Maior Risco da IA"
date: 2025-12-04T10:10:43+03:00
format: "standard" # Full list post format you can find in documentation theme
image: images/blog/blog-1.jpg
draft: false
author: Cristian Medeiros
description: "Sua equipe está entregando mais rápido com IA, mas o negócio não cresce? O DORA 2025 alerta: sem Foco no Usuário, a IA pode piorar a performance. Veja como corrigir a rota."
tags: 
    - UX
    - DORA 2025
    - IA
    - Product Engineering
    - Estratégia de Produto
    - CTO as a Service
    - Liderança Técnica

categories:
- Liderança Técnica
- IA
---


## A Armadilha da "Fábrica de Features" Turbinada

Com a chegada dos assistentes de código baseados em IA, a barreira para criar software caiu drasticamente. Hoje, é trivial gerar novas *features*, telas inteiras e APIs em tempo recorde. O sentimento imediato é de euforia: "Estamos entregando 50% mais rápido!"

Mas, se você olhar para os ponteiros do negócio — retenção, *churn*, receita — eles podem estar estagnados.

Este é o perigo da "Fábrica de Features" turbinada pela IA. A tecnologia é um motor potente, mas o **Foco no Usuário** é o volante. Se você der um motor de Fórmula 1 para um time que não sabe para onde está indo, eles não vão chegar ao pódio mais rápido; eles vão bater no muro mais rápido.

<cite>O Relatório DORA 2025 traz uma revelação contundente: em equipes que **não** têm um foco centrado no usuário, a adoção de IA tem um impacto **negativo** na performance da equipe.</cite> Apesar de não ser novidade, é interessante poder constatar isso com uma abordagem científica.

Isso mesmo. A IA pode atrapalhar. Sem a direção correta, ela acelera a produção de complexidade, débito técnico e funcionalidades que ninguém usa.

## Velocidade sem Direção é Desperdício (O Custo do *Output* vs. *Outcome*)

Na engenharia, é fácil confundir *Output* (código produzido, PRs mergeados, *story points*) com *Outcome* (valor gerado para o cliente). A IA é excelente em gerar *Output*. Ela não sabe nada sobre *Outcome* — a menos que você a direcione.

Antes, construir a funcionalidade errada levava duas semanas. Hoje, com IA, pode levar dois dias. O ciclo de desperdício (construir -> lançar -> falhar -> refazer) ficou mais rápido, consumindo recursos de nuvem e queimando a energia mental do time.

O DORA 2025 confirma que o foco no usuário não é apenas "coisa de designer". <cite>Equipes centradas no usuário têm maior produtividade, maior satisfação no trabalho e menos *burnout*</cite>. Sem isso, a IA vira apenas uma ferramenta de pressão por mais código.

## O Que Significa "Foco no Usuário" para a Engenharia?

Não basta o Product Manager (PM) falar com o cliente. A engenharia precisa entender o problema para usar a IA de forma eficaz. <cite>Segundo o DORA, o foco no usuário se manifesta quando o time</cite>:
1.  Usa o feedback do usuário para repriorizar o trabalho.
2.  Entende claramente o que o usuário quer alcançar.
3.  Vê a experiência do usuário como chave para o sucesso do negócio.

## Como um CTO as a Service Implementa Isso na Prática (O "Como Fazer")

Como **[CTO as a Service](https://cmxo.tech/servicos)**, meu papel muitas vezes é atuar como a **Ponte Estratégica**, impedindo que a engenharia se isole em uma bolha técnica.

**O Cenário (Exemplo Prático):**
Imagine a startup "SpeedShip". O time de engenharia está "voando" com o Copilot, entregando 10 tickets por semana. Mas o NPS está caindo e os desenvolvedores sentem que estão "enxugando gelo" (fazendo coisas que ninguém usa). O CTO está focado apenas em métricas de *throughput* (DORA metrics), ignorando o produto.

**Minha Abordagem como CTO as a Service (O Plano de Ação):**

### Passo 1 – Diagnóstico de Conexão (O Teste do "Porquê")
Vou a uma *daily* ou reunião de planejamento e faço uma pergunta simples para um desenvolvedor: *"Por que estamos construindo essa feature? Qual problema do usuário ela resolve?"*
*No "faz de conta":* O dev responde "Porque estava no Jira".
*Diagnóstico:* O time é uma fábrica de tickets. A IA só está acelerando a esteira de produção, sem conexão com o valor.

### Passo 2 – Quebrando o Silo (Engenharia encontra o Cliente)
Para conectar o time à realidade, instituímos ações táticas, como rotação de engenheiros no suporte. Mas usamos a IA para escalar essa empatia.
*Ação:* Configuramos uma ferramenta de IA para analisar tickets de suporte e transcrições de chamadas de vendas, gerando um "Resumo da dor do Cliente" semanal.
*Resultado:* A IA processa o volume de dados, mas o humano (o engenheiro) absorve a empatia ao ler os resumos. O time passa a entender *quem* está do outro lado da tela.

### Passo 3 – Redefinindo a "Definition of Done" (DoD)
Código "pronto" não é código *mergeado*. É código *usado* e *medido*.
*Ação:* Alteramos o processo para que nenhuma feature saia sem instrumentação (telemetria de uso, observabilidade). Se não podemos medir se o usuário usou, não construímos. A IA pode ajudar a escrever o código de telemetria rapidamente.

### Passo 4 – IA na Descoberta (Discovery), não só na Entrega
Mudamos o foco do uso da IA. Em vez de apenas usar o Copilot para "gerar código para essa função", ensinamos o time a usar a IA para "analisar esses 50 feedbacks de clientes e sugerir qual é a causa raiz do problema".
*Resultado:* Isso posiciona a engenharia como solucionadora de problemas, usando IA para entender o problema *antes* de gerar a solução.

---

## Conclusão: A IA precisa de um piloto

A IA não tem empatia. Ela não sabe se sua ideia de produto é ruim. Ela vai construí-la com a mesma eficiência e velocidade com que construiria uma ideia genial.

O **Foco no Usuário** é o "piloto" que garante que esse motor potente nos leve ao destino certo, em vez de apenas queimar combustível.

Alinhar Engenharia e Produto é um desafio cultural difícil, especialmente em empresas que crescem rápido. Como CTO as a Service, eu atuo como a ponte estratégica que garante que seu time técnico esteja construindo valor, e não apenas código.

**No próximo artigo desta série:** Vamos falar sobre **Ecossistemas de Dados Saudáveis** – o combustível de qualidade que sua IA precisa para funcionar além do básico.

---
### Recursos Adicionais
* **Relatório DORA 2025 (State of AI-assisted Software Development):** [https://dora.dev/research/2025/dora-report/](https://dora.dev/research/2025/dora-report/)
* **Relatório DORA 2024 (Accelerate State of DevOps):** [https://dora.dev/research/2024/dora-report/](https://dora.dev/research/2024/dora-report/)