# GoodWe Grid Assistant

## Assistente Inteligente para Operação Comercial de Eletropostos

---

## Integrantes

- Felipe Perdigão Macedo
- Felipe Mitsuo
- Letícia
- Laura Godoy
- Mariana
- Milena

---

## Curso

**FIAP — Ciência da Computação (CCPJ)**

---

## Problema Abordado

Com o crescimento acelerado da adoção de veículos elétricos, empresas e operadores de eletropostos enfrentam desafios relacionados à gestão operacional das estações de carregamento.

Entre os principais problemas estão:
- ausência de monitoramento inteligente;
- dificuldade no controle de potência;
- falhas na comunicação entre estações;
- dificuldade de faturamento;
- falta de suporte automatizado;
- baixa visibilidade operacional;
- ausência de ferramentas inteligentes para análise de uso.

O desafio GoodWe EV Challenge 2026 propõe soluções capazes de integrar inteligência operacional ao ecossistema de carregamento elétrico.

---

## Proposta da Solução

O projeto GoodWe Grid Assistant propõe um chatbot inteligente baseado em IA generativa para auxiliar operadores comerciais e técnicos responsáveis pela infraestrutura de eletropostos.

O chatbot será capaz de:
- informar status operacional das estações;
- identificar falhas e alertas;
- responder dúvidas técnicas;
- fornecer dados de consumo energético;
- auxiliar no controle de potência;
- apoiar o faturamento operacional;
- gerar respostas contextualizadas em linguagem natural.

---

## Tecnologias Utilizadas

| Tecnologia | Finalidade |
|---|---|
| Python | Backend principal |
| FastAPI | Criação da API |
| OpenAI API | Modelo de IA |
| LangChain | Orquestração do fluxo conversacional |
| ChromaDB | Base vetorial/contextual |
| GitHub | Versionamento |
| Draw.io | Modelagem do fluxograma |

---

## Justificativa Técnica

A OpenAI API foi escolhida devido à sua alta capacidade de compreensão contextual e geração de respostas naturais.

O LangChain será utilizado para estruturar o fluxo conversacional e permitir futura integração com memória contextual.

O ChromaDB permitirá implementar recuperação de contexto (RAG), possibilitando que o chatbot responda com base em documentos operacionais e registros das estações.

O FastAPI foi selecionado por oferecer desempenho elevado e simplicidade para construção da API do sistema.
