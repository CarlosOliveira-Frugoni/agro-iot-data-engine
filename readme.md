# 🌾 Agro IoT Data Engine

> Caderno temático criado com o [NotebookLM](https://notebooklm.google/) como parte de um Desafio Criativo da [DIO](https://dio.me), explorando como a Engenharia de Dados e a Internet das Coisas (IoT) estão transformando o agronegócio brasileiro.

![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-green)
![DIO](https://img.shields.io/badge/DIO-Desafio%20Criativo-blueviolet)
![Tema](https://img.shields.io/badge/tema-Agro%20%2B%20IoT%20%2B%20Dados-green)

---

## 📌 Contexto e Objetivos

**Tema escolhido:** Engenharia de Dados no Agronegócio — Como organizar dados de sensores e IoT para tomada de decisão.

**Por que esse tema?**
Minha trajetória profissional foi construída como Consultor e Executivo de Vendas Técnicas em setores de alta complexidade, como o agroindustrial, atuando na ponte entre o cliente final e a engenharia de aplicação. Com a transição de carreira para Engenharia de Dados e Inteligência Artificial, escolhi este tema para conectar minha bagagem prática do agronegócio às novas competências técnicas de modelagem de dados, sensores inteligentes e automação.

**Objetivos de estudo:**
- [x] Compreender como sensores IoT coletam dados no campo (umidade, temperatura, etc.)
- [x] Entender a arquitetura de um pipeline de dados agrícolas (do sensor à nuvem)
- [x] Identificar os principais desafios de conectividade e infraestrutura no agro brasileiro
- [x] Explorar como esses dados são usados para tomada de decisão pelo produtor rural

---

## 📚 Curadoria de Fontes

Foram selecionadas as seguintes fontes abertas para upload no NotebookLM:

| # | Título | Tipo | Link |
|---|--------|------|------|
| 1 | Tecnologia da Internet das Coisas na Agricultura 4.0: uma revisão sistemática | Artigo (PDF) | [Acessar](https://revistaadmpgc.weebly.com/uploads/1/3/9/5/13958983/artigo_6_v12_n2.pdf) |
| 2 | Adoção da Internet das Coisas (IoT) na agropecuária: uma revisão sistemática | Artigo (SciELO) | [Acessar](https://www.scielo.br/j/resr/a/R6rVdRLsZ5gLpQLZsbMvGcy/) |
| 3 | Utilizando sensores de IoT e Big Data para aprimorar a produção de culturas de precisão | Repositório (UFG) | [Acessar](http://repositorio.ufg.br/handle/123456789/22421) |
| 4 | Inteligência Artificial Aplicada na Agricultura de Precisão e Digital | Documento Técnico (Embrapa) | [Acessar](https://www.embrapa.br/busca-de-publicacoes) |

---

## 🧪 Engenharia de Prompts e "Cicatrizes"

### Prompt 1 — Extração de conceitos-chave

**Prompt utilizado:**
> *Com base nos documentos fornecidos, quais são os 5 termos ou siglas mais importantes relacionados a sensores e IoT no agronegócio, sua definição simples e importância para o produtor?*

**Resposta obtida (resumo):**
A IA identificou e explicou de forma simplificada os conceitos de **IoT**, **Sensores**, **Big Data**, **Agricultura de Precisão** e **M2M (Machine-to-Machine)**. Cada termo foi acompanhado de sua utilidade prática no campo, como a redução de desperdícios de adubo via Agricultura de Precisão e a automação de pivôs de irrigação por comunicação M2M.

---

### Prompt 2 — Conexão com regra de negócio (Ponto de vista do Engenheiro de Dados)

**Prompt utilizado:**
> *Agindo como um Engenheiro de Dados, explique como os dados coletados pelos sensores de umidade de solo descritos nos textos podem ajudar um gerente de fazenda a tomar decisões financeiras rápidas. Quais são os principais gargalos técnicos mencionados para que esses dados cheguem limpos até ele?*

**Resposta obtida (resumo):**
- **Impactos Financeiros:** Redução de até 30% em custos de energia elétrica por otimização da irrigação; aplicação exata de insumos (evitando perdas por lixiviação); geração de previsões de rendimento para fluxo de caixa; facilitação de acesso a créditos e seguros.
- **Gargalos Técnicos:** Conectividade precária no campo; falta de interoperabilidade entre equipamentos de fabricantes diferentes; danos físicos nos sensores (ex: pisoteio de animais); e desafios de conformidade com a LGPD e segurança de dados.

---

### Prompt 3 — Refinamento e "Cicatriz" (Troubleshooting)

**❌ Primeira tentativa (prompt genérico):**
> *Como a tecnologia ajuda a agricultura?*

**Problema encontrado:** A resposta foi extremamente superficial e ampla, citando que a tecnologia ajuda com tratores e previsão do tempo de maneira generalista, sem usar as informações específicas e os dados técnicos contidos nas fontes da curadoria.

**✅ Prompt refinado:**
> *Com base nos documentos fornecidos, quais são os 3 desafios de conectividade mais comuns na transmissão de dados de sensores de campo para a nuvem? As redes LPWAN resolvem a falta de conectividade?*

**Resultado após refinamento:**
A IA trouxe detalhes profundos sobre:
1. Localização remota e carência de sinal.
2. Barreiras físicas geográficas (necessidade de repetidores).
3. Incompatibilidade de protocolos entre marcas distintas.
Explicou que as redes **LPWAN (Low Power Wide Area Network)** são ótimas aliadas devido ao baixo consumo de energia e longo alcance, embora ainda dependam de gateways para saída de internet e de superação da resistência cultural dos produtores.

**💡 Lição aprendida ("Cicatriz"):**
Prompts genéricos geram respostas vagas. Para extrair valor técnico, é necessário instruir a IA a consultar apenas a base de documentos carregada e especificar restrições qualitativas (como pedir as limitações das redes LPWAN e soluções técnicas específicas).

---

## 📖 Miniguia de Estudo (Entrega Final)

### Resumos Estruturados

*   **IoT e Sensoriamento no Agro:** Consiste na implantação de dispositivos eletrônicos (sensores de solo, clima, umidade) capazes de monitorar continuamente a saúde da lavoura e transmitir esses registros sem interferência humana.
*   **Arquitetura do Fluxo de Dados:** Organizada em camadas: Coleta (sensores físicos) -> Comunicação (redes locais/LPWAN) -> Nuvem/Processamento (limpeza e estruturação) -> Inteligência (dashboards e Machine Learning para tomada de decisão).
*   **A Tomada de Decisão:** O papel prático é substituir o "achismo" por dados precisos de telemetria, permitindo economizar recursos hídricos e financeiros e prever com antecedência a estimativa de colheita.

### Glossário de Conceitos

| Termo | Definição | Importância no Campo |
|-------|-----------|----------------------|
| **IoT (Internet das Coisas)** | Rede de objetos físicos conectados que transmitem dados de telemetria. | Permite monitoramento remoto e em tempo real. |
| **Sensores** | Dispositivos físicos que convertem grandezas (umidade, calor) em dados digitais. | Atuam como os "olhos" da lavoura na coleta do solo. |
| **Big Data** | Volume massivo de dados variados gerados continuamente em alta velocidade. | Permite encontrar padrões preditivos de produtividade. |
| **Agricultura de Precisão** | Gestão agrícola baseada na variação espacial e temporal do talhão de terra. | Trata cada parte do solo de forma individualizada, gerando economia. |
| **M2M (Machine-to-Machine)** | Comunicação e transmissão de dados automatizada direta entre dispositivos. | Habilita a automação, como um sensor acionando um irrigador sozinho. |
| **LPWAN** | Redes de comunicação de baixo consumo energético e ampla cobertura. | Principal alternativa para superar a barreira da distância no campo. |

### Prompts Reutilizáveis

```text
Prompt 1: "Com base nos documentos de IoT no agronegócio, liste as principais variáveis do solo (ex: umidade, NPK) que sensores conseguem medir e descreva como a leitura incorreta afeta o pipeline de dados de tomada de decisão."
```

```text
Prompt 2: "Explique a diferença técnica e prática entre processamento de dados na nuvem (cloud) e processamento na ponta (edge computing) dentro do contexto de sensores isolados em lavouras brasileiras."
```

---

## 🛠️ Tecnologias e Ferramentas

- **NotebookLM** — Ambiente de IA para curadoria e pesquisa sobre os artigos selecionados.
- **GitHub** — Hospedagem, versionamento e portfólio profissional do projeto.

---

## 👤 Autor

**Carlos Oliveira Frugoni**

[![GitHub](https://img.shields.io/badge/GitHub-Perfil-181717?logo=github)](https://github.com/CarlosOliveira-Frugoni)

---

> 📝 Projeto desenvolvido como parte do Desafio Criativo do módulo de Inteligência Artificial da [Digital Innovation One (DIO)](https://dio.me).
