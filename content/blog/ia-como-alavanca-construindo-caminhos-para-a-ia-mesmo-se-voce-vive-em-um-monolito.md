---
title: "IA como Alavanca (Parte 3 de 7): Construindo \"Golden Paths\" para a IA (Mesmo se você vive em um Monolito)"
date: 2025-11-24T08:56:41+03:00
format: "standard" # Full list post format you can find in documentation theme
image: images/blog/blog-1.jpg
draft: false
author: Cristian Medeiros
description: Acha que precisa de microsserviços para ter uma Plataforma? Errado. O DORA 2025 mostra que a Plataforma é a chave para escalar a IA no seu legado. Veja como criar uma TVP (Plataforma Mínima Viável).
tags:
- Liderança Técnica
- IA
- DORA
- CTO as a Service
- Engenharia de Plataforma
- Monolito
- Legado
- Developer Experience
- Golden Path


categories:
- Liderança Técnica
- IA
- Plataforma
---

## O Mito da "Arquitetura Perfeita"

Se você lidera uma startup em crescimento, provavelmente vive uma realidade distante dos *cases* de sucesso do Vale do Silício, ou até das terras tupiniquins. Você não tem uma arquitetura de microsserviços imaculada rodando em Kubernetes perfeitamente orquestrados.

Você tem um "Monolito Heroico" — talvez em Rails, Django ou Node — que cresceu rápido demais. Ele funciona e paga as contas, mas é difícil de configurar, lento para fazer *deploy* e assustador para novos desenvolvedores.

Quando se fala em **Engenharia de Plataforma** e **IA**, seu primeiro instinto talvez seja o medo: *"Não posso pensar nisso agora. Tenho que refatorar tudo primeiro."*

O Relatório DORA 2025 traz uma verdade libertadora: **Você não precisa reescrever tudo para ter uma plataforma.** Pelo contrário: é o seu monolito "bagunçado" que mais precisa de uma **Plataforma Interna de Qualidade** agora.

Sem uma plataforma que abstraia a complexidade do seu legado, a IA não gera impacto no negócio. <cite>Ela apenas gera código mais rápido que vai travar na hora de rodar </cite>.

## Por que a Plataforma é o "Motor da Eficiência" para a IA?

O conceito central aqui são os **"Golden Paths"**. Uma plataforma não serve para reescrever o código da empresa; ela serve para criar uma estrada pavimentada onde os desenvolvedores (e agora a IA) possam trabalhar sem bater, de nada serve ter velocidade sem direção.

<cite>O DORA 2025 descobriu que plataformas de alta qualidade **amplificam drasticamente** o impacto positivo da IA na performance organizacional </cite>.

* **O cenário SEM plataforma:** O desenvolvedor pede para a IA criar uma nova *feature*. A IA gera o código em segundos. O desenvolvedor leva 2 dias tentando configurar o ambiente local do monolito para testar esse código, lutando com dependências quebradas e versões de banco de dados. **Ganho da IA = Zero.**
* **O cenário COM plataforma:** O desenvolvedor usa um comando simples (CLI) para subir um ambiente efêmero do monolito. A IA cria a *feature* e a própria plataforma roda os testes automaticamente nesse ambiente. **Ganho da IA = Real e Escalável.**

## Plataforma no Monolito: Abstração, não Refatoração

O maior erro que vejo como CTO as a Service é confundir Plataforma com "Infraestrutura Complexa". Plataforma não é instalar o Backstage ou migrar para Kubernetes se você não precisa.

<cite>**Plataforma é Experiência do Desenvolvedor (DX).** </cite>

Se você tem estruturas desorganizadas ou um monolito legado, não tente "arrumar a casa" inteira de uma vez. O segredo é construir um **"andaime" (scaffolding)** seguro ao redor do monolito.

Isso pode ser tão simples quanto scripts de automação robustos, ambientes de *preview* por Pull Request ou dados de teste sanitizados que funcionam sempre. <cite>A plataforma é a camada que diz à IA (e ao Dev): *"Não se preocupe com a bagunça, apenas use esta interface que vai dar tudo certo."* </cite>

## Como um CTO as a Service Implementa a "TVP" (Thinnest Viable Platform)

Aqui na CM-XO, aplicamos o conceito de **TVP (Thinnest Viable Platform)** — a Plataforma Mínima Viável. Não construímos a "NASA", construímos o "trilho" que seu time precisa hoje. O conceito de TVP foi criado à muitos anos, vem do Team Topologies de Mathew Skelton e Manuel Pais, o livro entra em vários detalhes interessantes. 

**O Cenário (Exemplo Prático):**
Imagine a startup "LegacyScale". Eles têm um monolito em PHP/Laravel de 8 anos. Ninguém sabe como rodar o ambiente local direito. A IA está gerando código, mas ele quebra em produção porque o ambiente de desenvolvimento é diferente do de produção.

**Minha Abordagem como CTO as a Service (O Plano de Ação):**

### Passo 1 – Identificar a Fricção Máxima (Onde a IA trava?)
Não começamos instalando portais (sabe o tal do IDP - Internal Developer Portal - pois é, pulamos ele por enquanto). Começamos com diagnóstico. Onde os devs (e a IA) perdem mais tempo?
*No "Faz de Conta":* Descobrimos que configurar o banco de dados local com dados úteis leva 4 horas. A IA não consegue resolver "configuração de ambiente". A Plataforma *precisa* resolver isso.

### Passo 2 – Construir o Primeiro "Golden Path" (O "Happy Path")
Em vez de refatorar o PHP, criamos uma abstração.
*Ação:* Criamos um `Docker Compose` robusto e um `Makefile` padronizado.
*Resultado:* Agora, qualquer dev (ou agente de IA) roda `make start` e o ambiente sobe completo em 5 minutos, com banco populado. Isso é uma Plataforma Interna de Qualidade para este estágio.

### Passo 3 – A Plataforma como "Cérebro" da IA (Contexto faz toda diferença)
Aqui está o pulo do gato. Uma IA genérica não conhece as peculiaridades (AKA "gambiarras") do seu monolito de 8 anos. Se você pedir para ela criar uma *query*, ela vai criar algo padrão que provavelmente quebra o seu banco legado.
* **O Problema:** A IA gera código "correto" em teoria, mas "errado" para o seu legado porque lhe falta contexto.
* <cite>**A Solução da Plataforma:** O DORA 2025 destaca a capacidade de **"Dados Internos Acessíveis à IA"** </cite>. Usamos a plataforma para automatizar a extração desse contexto.
* **Ação no "Faz de Conta":** Configuramos um *job* na plataforma que varre o banco de dados de homologação e gera, automaticamente, um arquivo atualizado com o esquema do banco e a documentação das APIs internas. Esse contexto é indexado e disponibilizado para a ferramenta de IA (via RAG ou contexto do GitHub Copilot).
* **O Ganho Real:** Agora, quando o dev pede: "Crie uma rota de usuário", a IA **sabe** que a tabela se chama `tbl_usr_2018` e não `users`. A plataforma garantiu que a IA "aprendesse" o legado, economizando horas de depuração.

---

## Conclusão: A Plataforma é a "API" do seu Monolito

Você não precisa matar seu monolito para usar IA. <cite>Você precisa **encapsulá-lo** com uma plataforma que torne o trabalho nele cognitivamente barato </cite>.

Uma plataforma interna transforma um "legado assustador" em um "produto interno consumível". É isso que permite que a IA atue como acelerador, e não como gerador de caos.

Construir essa camada de abstração exige visão de produto e técnica. Como [CTO as a Service](https://cmxo.tech/servicos), eu ajudo a definir qual é a "Plataforma Mínima" que sua empresa precisa para desbloquear a IA hoje, sem esperar a refatoração do ano que vem.

**No próximo artigo desta série:** Vamos falar sobre **Foco Centrado no Usuário** — e por que a IA pode ser perigosa se você estiver construindo a coisa errada muito rápido.

---
### Recursos Adicionais
* **Relatório DORA 2025 (State of AI-assisted Software Development):** [https://dora.dev/research/2025/dora-report/](https://dora.dev/research/2025/dora-report/)
* **Relatório DORA 2024 (Accelerate State of DevOps):** [https://dora.dev/research/2024/dora-report/](https://dora.dev/research/2024/dora-report/)
* **Backstage:** [https://backstage.io/](https://backstage.io/)