# Anonimização e Privacidade de Dados Pessoais Orientada por IA

**Fundação Hermínio Ometto (FHO)**

## 👥 Autores
* **Arlyson da Silva Nascimento 11**
* **Kauan Vitor Torres de Melo**
* **Richard Nicholas Rocha**

## 🎯 Objetivo
Este projeto desenvolveu uma solução de **Anonimização Hierárquica** utilizando o modelo de Inteligência Artificial **T5 (Transformer)**. O objetivo foi proteger dados sensíveis (LGPD) em textos não estruturados, equilibrando privacidade e utilidade.

## 🧠 Metodologia
Utilizamos a técnica de *Fine-Tuning* no modelo `t5-small` com um dataset sintético de 20.000 frases, aplicando três níveis de risco:
1.  **Risco Crítico (Supressão):** Remoção total de CPFs, Senhas e Telefones.
2.  **Risco Alto (Generalização):** Substituição de Nomes e E-mails por tags `[NOME]`.
3.  **Risco Baixo (Manutenção):** Preservação de Cidades e Cargos para manter o contexto.

## 📊 Resultados
O modelo atingiu alta eficácia na detecção de dados críticos, incluindo a capacidade de identificar CPFs não formatados (apenas números).

| Categoria | Ação | Taxa de Sucesso (Estimada) |
| :--- | :--- | :--- |
| **Crítico** (CPF/Senha) | Supressão | ~62.5% |
| **Baixo** (Contexto) | Manutenção | ~71.4% |
| **Alto** (Nomes) | Generalização | ~50% (Limitação de vocabulário) |

## 🛠️ Como Executar
O código principal está no arquivo `Codigo_Final.ipynb`. Ele pode ser executado diretamente no Google Colab ou Kaggle.

---
*Trabalho apresentado à disciplina de Inteligência Artificial I - Prof. Renato Luciano Cagnin.*
