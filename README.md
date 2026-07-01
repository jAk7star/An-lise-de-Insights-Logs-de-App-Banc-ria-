## 📊 An-lise-de-Insights-Logs-de-App-Banc-ria-

## 📝 Descrição do Projeto
Este projeto consiste numa **Análise de Insights** baseada numa base de dados contendo logs de utilização da aplicação de um banco digital fictício. O objetivo principal é extrair métricas de desempenho, identificar estrangulamentos operacionais (como latência e falhas em transações) e diagnosticar a estabilidade de serviços críticos, como transferências financeiras, autenticação e apoio ao cliente.

Além da análise de dados estruturada, o grande diferencial deste repositório é a documentação de todo o processo de **Engenharia de Prompt**. O projeto demonstra como instruir o modelo **Google Gemini**, estruturando os comandos para maximizar a precisão da IA, de forma a automatizar a extração de insights, classificar o estado dos serviços e gerar resumos executivos a partir de dados brutos de log.

## 🚀 Principais Insights e Diagnóstico
A partir da análise dos registos (cerca de 1.200 eventos), foram identificados os seguintes cenários:
* **Pix (Estado Crítico):** Elevado volume de transações com estado `TIMEOUT`, `PENDING` e `FAILED`, exigindo revisão nas políticas de repetição (retry).
* **Infraestrutura (Degradada):** Picos de latência a atingir mais de 7.000 ms, gerando feedback direto de lentidão por parte dos utilizadores.
* **Chatbot (Insatisfatório):** Respostas inadequadas ou repetitivas, indicando a necessidade de aprimorar a compreensão de contexto.
* **Autenticação (Instável):** Falhas recorrentes no processo de início de sessão (login).
* **Análise Arquitetural:** Avaliação de compromissos (trade-offs) arquiteturais, considerando propriedades ACID e o Teorema CAP nos fluxos de processamento.

## 📂 Estrutura do Repositório

* `docs/`: Ficheiros explicativos, relatórios gerados e o Resumo Executivo Técnico.
* `data/`: Amostras dos dados de log estruturados utilizados para a análise (dados 100% fictícios).

## 🧠 Engenharia de Prompt com Gemini e Metodologia
Tanto nos notebooks como nos ficheiros de documentação, encontra-se detalhada a explicação de como o processo funciona para criar o prompt ideal utilizando o **Gemini**. A metodologia abrange:
1. **Definição de Contexto no Gemini:** Parametrização do modelo para atuar como um analista de dados/engenheiro de fiabilidade (SRE).
2. **Injeção de Dados:** Estruturação dos logs para um consumo eficiente pela arquitetura do LLM.
3. **Instruções de Saída:** Comandos específicos para gerar tabelas de diagnóstico (Tema, Sentimento, Evidência e Ação Sugerida) e definir prioridades de atuação com foco em observabilidade.

## 🛠️ Tecnologias e Conceitos Abordados
* Análise de Dados / Processamento de Logs
* Engenharia de Prompt (Google Gemini) / Inteligência Artificial
* Arquitetura de Bases de Dados (Transações ACID, Teorema CAP, SQL/NoSQL)
* Observabilidade e SRE (Site Reliability Engineering)

## ⚙️ Como Reproduzir
1. Clone este repositório:
   ```bash
   git clone (https://github.com/jAk7star/An-lise-de-Insights-Logs-de-App-Banc-ria-.git)
