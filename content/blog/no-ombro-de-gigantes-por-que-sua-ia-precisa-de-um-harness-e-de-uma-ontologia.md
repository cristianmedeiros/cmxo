---
title: "No ombro de gigantes: por que sua IA precisa de um harness (e de uma ontologia)"
date: 2026-06-16T10:15:43+03:00
format: "standard" # Full list post format you can find in documentation theme
image: images/blog/blog-1.jpg
draft: false
author: Cristian Medeiros
description: "Dar acesso ao ChatGPT ou Claude para o seu time sem criar regras de negócio claras é pedir para a IA errar. Descubra como o Harness e a Ontologia protegem sua operação."
tags: 
    - IA
    - Harness
    - Ontologia
    - Gestão de Conhecimento
    - Eficiência Operacional

categories:
- Harness
- IA
- Eficiência Operacional
---

Todo mundo conhece a famosa frase de Isaac Newton (é do Newton, pesquisei :p) sobre enxergar mais longe por estar sobre os ombros de gigantes. Ele sabia que não precisava reinventar a física do zero; bastava construir em cima do que já estava validado.

O problema é que a maioria das empresas hoje faz exatamente o oposto com a inteligência artificial. 

Tratam as ferramentas como se fossem gênios solitários. Entregam o acesso ao Claude, ao ChatGPT ou a ferramentas de código para o time e esperam que a máquina adivinhe como o negócio funciona por telepatia. Afinal, o treco é tão "inteligente", como não vai conseguir entender como a empresa funciona?

E nesse ponto as pessoas equecem que a IA não sabe como você precifica, qual é a margem mínima de lucro aceitável ou quais são as travas jurídicas dos seus contratos.

O resultado é previsível. A IA cria uma proposta comercial linda, muito bem escrita, mas financeiramente ruinosa para a empresa. Ou gera um código super rápido que ignora uma regra básica de segurança da sua infraestrutura.

A IA é excelente em sintaxe, mas cega em contexto. Se você quer que ela trabalhe direito, precisa fazê-la subir no ombro dos gigantes da sua empresa: seus playbooks, sua estratégia e seu histórico. Para chegar lá, vamos entender como o "Harness" e uma Ontologia podem ajudar.

Calma,tem um jeito de construir isso do zero, mesmo que esteja desorganizado.

## O que é um Harness?

Mesmo se olharmos apenas para a engenharia de software, o conceito de Harness mudou drasticamente. Ele deixou de ser apenas aquela bancada tradicional que roda testes unitários para ver se um componente quebra. 

Na era de agentes, sub-agentes, e agentes autônomos de desenvolvimento, o Harness é a infraestrutura que governa o ciclo de vida do contexto técnico. É o sistema que impede o "fork silencioso" da verdade — aquela situação perigosa onde duas partes do time (ou duas máquinas/agentes diferentes) começam a assumir premissas arquiteturais divergentes sem que ninguém perceba. O Harness garante que uma solução de debugging complexa encontrada em uma sessão isolada seja capturada, validada e promovida a fato institucional. A partir dali, a regra viaja acoplada com os agentes em qualquer máquina, automatizando a disciplina no momento da escrita. É o equivalente a ter um corretor ortográfico focado na estratégia. Se o seu funcionário ou a IA tentam aplicar um preço errado ou uma arquitetura capenga, o sistema sublinha em vermelho e impede o envio antes mesmo do commit ou da revisão humana.

Quando expandimos essa mesma lógica para a operação inteira de um negócio, o Harness vira o **Gandalf - YOU SHALL NOT PASS**, ou seja, vira a estrutura que impede a máquina de fazer besteira. É a esteira que garante que qualquer material gerado por IA — seja uma proposta comercial, um orçamento financeiro ou um código — respeite as diretrizes da companhia.

Uma operação madura divide essa estrutura em três camadas vivas:

1. **Memória local:** É o contexto imediato e em voo da tarefa. O rascunho do e-mail que o comercial está editando, o checkpoint de um relatório ou o estado da branch local do dev. São informações temporárias, voláteis e descartáveis. Algumas são mais duráveis, e persistimos na memória local da ferramenta, no arquivos .md.
2. **Repositório compartilhado:** É o lar dos seus playbooks e regras de ouro. No nível básico, é um Shared Drive muito bem organizado por tipos de perguntas (e não por pastas de autores). No nível avançado, vira um Hub de Conhecimento Vetorial (Enterprise RAG) que atualiza o contexto dos seus agentes em tempo real via API.
3. **O Sistema de Registro:** Onde os dados oficiais residem de forma canônica. Para o desenvolvedor, é o Git. Para o vendedor, é o CRM (HubSpot/Salesforce). Para o financeiro, é o ERP. A IA pode ler essas fontes para buscar a verdade, mas nunca alterar os dados estruturados sem passar por uma barreira rígida de validação.

## E onde entra a Ontologia?

O Harness dá as camadas e as travas físicas do sistema. A Ontologia dá o dicionário e o modelo mental. Uma forma mais simples de explicar seria um glossário que explica os termos da empresa e do sistema.

Modelos de linguagem entendem palavras, mas não entendem o significado delas dentro do seu mercado. Sem uma ontologia clara, a IA vai confundir conceitos fundamentais. Ela não sabe, por exemplo, a diferença jurídica ou de margem entre um "Parceiro" e um "Cliente Enterprise". Para ela, no dicionário genérico da internet, são coisas parecidas. No seu caixa, não são.

A ontologia desenha as entidades do seu negócio e como elas se relacionam. Ela ensina à máquina: *"Nesta empresa, um Cliente Enterprise tem múltiplos CNPJs, e cada CNPJ tem um teto de faturamento diferente no ERP"*. 

Quando você junta o Harness (as travas e fluxos) com a Ontologia (o mapa mental), o seu sistema evolui para o que o mercado chama de Graph-RAG. A IA para de fazer buscas burras por palavras-chave em PDFs soltos (ou arquivos .md) e passa a entender o impacto de segunda ordem de qualquer proposta ou documento que ela gerar.

## Como começar sem tentar abraçar o mundo

Montar uma estrutura dessas parece um trabalho imenso, mas tentar documentar a empresa inteira de uma vez só serve para criar arquivos mortos que ninguém lê. O segredo é o crescimento incremental baseado na maturidade dos fatos.

Funciona assim:

* **O erro em voo:** O time comercial usa IA para fazer um orçamento complexo e aplica uma regra fiscal errada para um cliente de outro estado. O erro é descoberto e corrigido na revisão humana.
* **A promoção do fato:** Em vez de apenas corrigir o documento e seguir a vida, o líder pega essa regra tributária específica — esse fato validado — e o "promove" para a Camada 2 do Harness (o repositório compartilhado). Escreve um prompt assim: "Atualiza o repositório compartilhado com esse aprendizado"
* **O resultado:** A partir desse dia, qualquer IA ou funcionário que for gerar uma apresentação ou proposta comercial consultará a base, baterá na ontologia correta e nunca mais repetirá esse erro. O benefício escala com a frota inteira.

## O ativo que ninguém consegue copiar

Na era atual, gerar texto, código ou planilhas custa frações de centavos. A capacidade de execução bruta virou uma commodity que qualquer competidor compra com uma assinatura de ferramentas de mercado.

O verdadeiro diferencial competitivo de uma empresa mudou. Não é a ferramenta de IA que você usa, mas a qualidade e a governança do contexto que você entrega para ela. 

Empresas que gastam tempo desenhando um Harness forte e uma Ontologia clara não precisam dar briefings infinitos para novos funcionários ou gastar horas revisando o trabalho dos seus agentes automatizados. Elas simplesmente colocam a inteligência para trabalhar sobre o todo esse trabalho que foi construído com a IA. 

Para encerrar, tem mais um ponto que considero muito importante, tudo que é gerado acaba virando Harness (lembra do tema de qualidade de dados do DORA 2025?), pois bem, uma proposta recusada (ou aceita), um spec de nova feature, um teste que falhou, um deploy, uma reunião, etc, tudo que é gerado pode ser classificado e direcionado para a IA se aperfeiçoar, e fazer seu time trabalhar melhor, é extamente ai que mora a capacidade da IA de potencializar as pessoas. 