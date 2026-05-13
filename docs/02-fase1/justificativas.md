# 2.4 Justificativas

A escolha do conjunto tecnológico formado pelo **Ollama** e o modelo **Qwen 2.5 7B** é estrategicamente orientada para permitir a medição precisa dos atributos de qualidade do nosso software, especificamente focando nas características de **Eficiência** e **Portabilidade**, conforme delineado pelas normas de qualidade.

---

## 2.4.1 Por que o Qwen 2.5 7B?

### Tamanho e Viabilidade Local

O **Qwen 2.5 7B-Instruct** possui aproximadamente [**7,61 bilhões de parâmetros**](https://huggingface.co/Qwen/Qwen2.5-7B-Instruct), caracterizando-se como um modelo de linguagem grande (LLM) robusto, porém otimizado o suficiente para execução em hardware d
e consumo.  

Além disso, o modelo suporta **quantização**, processo que reduz significativamente o tamanho e o consumo de recursos computacionais, tornando-o ideal para testes de estresse e avaliação dos limites do hardware.

### Capacidade Multilíngue e de Contexto
O modelo oferece suporte avançado para mais de **29 idiomas**, incluindo o Português, além de suportar janelas de contexto extensas de até **131.072 tokens**.  

Essa capacidade permite submeter o sistema a cargas variáveis de processamento textual, possibilitando medir diretamente o impacto dessas cargas no desempenho do software.

---

## 2.4.2 Por que o Ollama?

### Isolamento de Ambiente (Offline)
O **Ollama** possibilita a execução local e totalmente offline de modelos de linguagem. Isso é essencial para testes de **Eficiência**, pois elimina variáveis externas imprevisíveis, como:

- Latência de rede;
- Gargalos de servidores em nuvem;
- Instabilidades de conexão.

Dessa forma, os resultados obtidos refletem exclusivamente o desempenho do hardware local e da aplicação.

### Agilidade na Implantação
O Ollama foi desenvolvido para simplificar a execução de modelos abertos localmente, oferecendo:

- Compatibilidade multiplataforma;
- Suporte à conteinerização via Docker;
- Facilidade de configuração.

Essas características tornam a ferramenta ideal para avaliar e metrificar atributos relacionados à **Portabilidade**.

---

## 2.4.3 Estruturação da Medição (Abordagem GQM)

Para garantir que a coleta de dados esteja alinhada aos objetivos da pesquisa, utiliza-se o framework **GQM (Goal-Question-Metric)**.

A definição do propósito analítico estrutura-se da seguinte forma:

- **Objeto de análise:** o modelo Qwen 2.5 7B executado sob o motor do Ollama;
- **Propósito:** compreender e metrificar o comportamento do sistema;
- **Foco:** atributos de qualidade relacionados à Eficiência e Portabilidade;
- **Ponto de vista:** equipe de desenvolvimento e testes;
- **Contexto:** ambiente operacional do software.

---

## 2.4.4 Mapeamento das Métricas (ISO/IEC TR 25021)

Com base no relatório técnico **ISO/IEC TR 25021**, que define elementos de medida de qualidade, a justificativa dessa arquitetura se fundamenta nas seguintes métricas associadas às características escolhidas.

---

### 1. Eficiência (Efficiency)

#### Comportamento no Tempo (Time Behaviour)
Com a execução local do Qwen, serão avaliadas métricas como:

- **Mean Response Time:** tempo médio entre a requisição e a geração da resposta;
- **Throughput:** rendimento medido em tokens processados por segundo.

#### Utilização de Recursos (Resource Utilization)
Durante a geração textual do Qwen 2.5, serão utilizadas ferramentas de monitoramento para aferir métricas como:

- **Maximum Memory Utilization:** utilização máxima de memória RAM/VRAM;
- **I/O Loading Limits:** limites de carga de entrada e saída do sistema.

---

### 2. Portabilidade (Portability)

#### Adaptabilidade (Adaptability)
A combinação entre Ollama e Docker possibilita avaliar métricas relacionadas a:

- **Hardware Environmental Adaptability:** capacidade de execução em diferentes configurações de hardware;
- **System Software Environmental Adaptability:** adaptação a diferentes sistemas operacionais e ambientes Docker.

#### Instalabilidade (Installability)
O esforço necessário para preparar o ambiente local será medido utilizando métricas voltadas para:

- **Ease of Installation:** facilidade de instalação e configuração do ambiente;
- Tempo necessário para implantação;
- Taxa de sucesso na execução em diferentes ambientes.

# Referências Bibliográficas

> 1. ISO/IEC. *ISO/IEC TR 25021:2007: Software engineering — Software product Quality Requirements and Evaluation (SQuaRE) — Quality measure elements*. 1. ed. Genebra: International Organization for Standardization / International Electrotechnical Commission, 2007.

> 2. RAMOS, Cristiane Soares. *Medição baseada em objetivos: “Determinando o que medir”*. Material da disciplina FGA0278 - Qualidade de Software 1. Faculdade do Gama (FGA), Universidade de Brasília (UnB), 2024.

> 3. QWEN. *Qwen/Qwen2.5-7B-Instruct*. Repositório de modelos Hugging Face, 2024. Disponível em: <https://huggingface.co/Qwen/Qwen2.5-7B-Instruct>. Acesso em: 13 maio 2026.

> 4. QWEN TEAM. *Qwen2 Technical Report*. 2024. Disponível em: <https://arxiv.org/abs/2407.10671>. Acesso em: 13 maio 2026.

> 5. OLLAMA INC. *Ollama: The easiest way to build with open models*. Portal oficial de documentação, 2026. Disponível em: <https://ollama.com>. Acesso em: 13 maio 2026.