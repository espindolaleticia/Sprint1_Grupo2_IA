# GoodWe Grid Assistant — Sprint 2

## 1. Nome do Projeto

**GoodWe Grid Assistant**

Chatbot operacional com IA generativa para apoio à gestão de eletropostos comerciais no contexto do **GoodWe EV Challenge 2026**.

---

## 2. Integrantes

| Nome              | RM     |
| ----------------- | ------ |
| Felipe Mitsuo     | 570692 |
| Felipe Perdigão   | 570990 |
| Laura Godoy       | 569181 |
| Letícia Espindola | 569308 |
| Mariana Carbollan | 569207 |
| Milena de Aguiar  | 570599 |

---

## 3. Contexto do Projeto

O projeto foi desenvolvido no contexto do **GoodWe EV Challenge 2026**, com foco na problemática **ChargeGrid Intelligence**.

A proposta considera um ambiente comercial com múltiplas estações de carregamento para veículos elétricos, onde operadores, técnicos e administradores precisam acompanhar informações operacionais em tempo real ou quase real.

Entre os principais desafios desse contexto estão:

* monitoramento descentralizado das estações;
* falhas de comunicação entre eletropostos e sistema central;
* dificuldade de identificação rápida de falhas críticas;
* baixa visibilidade sobre consumo energético;
* necessidade de controle de potência;
* dificuldade de faturamento por ciclo de recarga;
* ausência de suporte operacional automatizado;
* falta de inteligência contextual para tomada de decisão.

---

## 4. Problema Abordado

Com o crescimento do uso de veículos elétricos, empresas que operam redes de eletropostos precisam lidar com grande volume de informações operacionais.

Sem um sistema inteligente de apoio, o operador pode ter dificuldade para responder rapidamente a perguntas como:

* quais estações estão offline;
* quais falhas críticas estão ativas;
* qual estação consumiu mais energia;
* se a rede está próxima do limite de potência;
* qual foi o faturamento da semana;
* qual estação precisa de manutenção;
* quais ciclos de recarga foram registrados;
* quais usuários foram identificados por RFID.

O problema central abordado pelo projeto é a **ausência de um assistente operacional inteligente capaz de interpretar dados da rede de carregamento e responder em linguagem natural**.

---

## 5. Escolha do Contexto: Comercial

O projeto escolheu o contexto **comercial**, com foco em redes de eletropostos utilizadas por empresas, operadores de estacionamento, centros comerciais ou infraestrutura corporativa.

Essa escolha foi feita porque o ambiente comercial apresenta maior complexidade operacional do que o ambiente condominial.

No ambiente comercial, normalmente existem:

* múltiplas estações de carregamento;
* maior volume de ciclos de recarga;
* necessidade de faturamento por consumo;
* controle de potência mais crítico;
* operação contínua;
* maior impacto financeiro em caso de falha;
* necessidade de suporte técnico rápido;
* maior volume de dados operacionais.

No ambiente condominial, o foco costuma estar mais relacionado à divisão de uso entre moradores, regras internas e cobrança compartilhada. Já no ambiente comercial, a necessidade principal está na **continuidade da operação, controle energético, disponibilidade das estações e faturamento eficiente**.

Por isso, o contexto comercial foi considerado mais adequado para o desenvolvimento do GoodWe Grid Assistant.

---

## 6. Proposta da Solução

O **GoodWe Grid Assistant** é um chatbot operacional baseado em IA generativa, criado para auxiliar operadores comerciais, técnicos de manutenção e administradores de redes de eletropostos.

O chatbot permite que o usuário faça perguntas em linguagem natural e receba respostas contextualizadas com base nos dados simulados da operação.

A solução permite consultar informações como:

* status das estações;
* estações offline;
* falhas críticas;
* alertas prioritários;
* consumo energético;
* faturamento da rede;
* manutenção de estações;
* controle de potência;
* ciclos de recarga;
* registros RFID;
* billing por consumo;
* recomendações operacionais.

Nesta Sprint 2, o sistema foi implementado em Python, com interface web local, integração com a Ollama Cloud API e uso do modelo `gpt-oss:120b`.

---

## 7. Personas Atendidas

### 7.1 Operador Comercial

Responsável pelo acompanhamento da operação diária da rede de eletropostos.

#### Principais dores

* precisa saber rapidamente quais estações estão indisponíveis;
* precisa acompanhar faturamento;
* precisa verificar consumo energético;
* precisa manter a rede operacional;
* precisa tomar decisões rápidas durante falhas.

#### Perguntas típicas

* Quais estações estão offline neste momento?
* Qual foi o faturamento total da rede nesta semana?
* Qual estação apresentou maior consumo hoje?
* Existe algum alerta prioritário ativo?
* A rede está operando acima do limite recomendado?

---

### 7.2 Técnico de Manutenção

Responsável por diagnosticar falhas, verificar alertas e realizar intervenções técnicas.

#### Principais dores

* precisa identificar falhas críticas;
* precisa saber quando uma estação foi desativada;
* precisa acompanhar histórico de manutenção;
* precisa priorizar chamados;
* precisa reduzir tempo de diagnóstico.

#### Perguntas típicas

* Existe alguma estação com falha crítica ativa?
* Qual foi a última manutenção registrada na estação GW-03?
* Qual estação apresentou superaquecimento?
* O que devo fazer se uma estação apresentar falha de comunicação?
* Há alguma estação que precisa de validação técnica?

---

### 7.3 Administrador da Rede

Responsável pela visão estratégica da operação, estabilidade da rede e eficiência energética.

#### Principais dores

* precisa acompanhar uso da capacidade da rede;
* precisa evitar sobrecarga;
* precisa avaliar eficiência operacional;
* precisa acompanhar indicadores de consumo;
* precisa tomar decisões de gestão energética.

#### Perguntas típicas

* A rede está próxima do limite de potência?
* O consumo atual está dentro dos parâmetros seguros?
* Como a potência pode ser redistribuída entre estações?
* Existe risco de sobrecarga?
* Quais dados de consumo estão disponíveis?

---

## 8. Funcionalidades Implementadas na Sprint 2

Nesta Sprint 2 foram implementadas as seguintes funcionalidades:

* chatbot funcional em Python;
* interface web local para interação;
* integração com Ollama Cloud API;
* uso do modelo `gpt-oss:120b`;
* leitura de API Key por variável de ambiente;
* system prompt com contexto GoodWe;
* gerenciamento de histórico de conversa;
* injeção de contexto operacional simulado;
* respostas em linguagem natural;
* tratamento de perguntas fora do escopo;
* tratamento de tentativa adversarial;
* execução automática de testes;
* geração do arquivo `tests/resultados_testes.md`.

---

## 9. Tecnologias Utilizadas

| Tecnologia       | Finalidade                               |
| ---------------- | ---------------------------------------- |
| Python           | Linguagem principal do projeto           |
| FastAPI          | Criação da API e da interface web local  |
| Uvicorn          | Servidor local para executar a aplicação |
| Ollama Cloud API | Acesso remoto ao modelo de IA            |
| gpt-oss:120b     | Modelo de linguagem usado no chatbot     |
| python-dotenv    | Leitura segura de variáveis de ambiente  |
| HTML             | Estrutura da interface web               |
| CSS              | Estilização da interface                 |
| JavaScript       | Envio de mensagens para a API            |
| GitHub           | Versionamento e entrega do projeto       |

---

## 10. Justificativa Técnica

A **Ollama Cloud API** foi escolhida para permitir o uso do modelo `gpt-oss:120b` sem necessidade de baixar ou executar o modelo localmente.

O modelo `gpt-oss:120b` foi utilizado por oferecer boa capacidade de interpretação textual, geração de respostas em linguagem natural e adaptação ao contexto operacional do projeto.

O **FastAPI** foi escolhido por ser simples, leve e eficiente para criação de APIs em Python. Ele permite criar endpoints para comunicação entre a interface web e o backend do chatbot.

O **python-dotenv** foi utilizado para carregar variáveis de ambiente a partir do arquivo `.env`, evitando que a chave da API fique exposta diretamente no código.

O histórico de mensagens foi implementado em memória para permitir conversas contínuas durante uma mesma sessão.

O contexto operacional foi simulado dentro do sistema para representar dados de estações, falhas, consumo, faturamento, manutenção, alertas, RFID e orquestração de potência.

---

## 11. Comparação Técnica de Modelos

| Critério                     | gpt-oss:120b via Ollama Cloud                               | Llama 3 via Groq                             |
| ---------------------------- | ----------------------------------------------------------- | -------------------------------------------- |
| Tipo de acesso               | API remota                                                  | API remota                                   |
| Necessidade de baixar modelo | Não                                                         | Não                                          |
| Custo                        | Depende da plataforma/API utilizada                         | Depende da plataforma/API utilizada          |
| Latência                     | Pode variar conforme conexão e disponibilidade da API       | Geralmente baixa em infraestrutura otimizada |
| Qualidade em português       | Boa para respostas técnicas e estruturadas                  | Boa para tarefas gerais                      |
| Adequação ao projeto         | Alta, pois permite uso de modelo robusto sem execução local | Média/alta, mas exigiria adaptação da API    |
| Escolha final                | Escolhido para a Sprint 2                                   | Alternativa considerada                      |

A escolha final foi o `gpt-oss:120b` via Ollama Cloud porque o grupo definiu esse modelo como base da implementação da Sprint 2, mantendo a execução simples pelo VS Code e sem necessidade de instalação local do modelo.

---

## 12. System Prompt

O chatbot utiliza um arquivo de system prompt localizado em:

```text
prompts/system_prompt.txt
```

Esse arquivo define:

* papel do assistente;
* personas atendidas;
* escopo permitido;
* temas fora de escopo;
* regras de segurança;
* formato de resposta;
* critérios de escalada humana;
* contexto do projeto.

O system prompt é carregado automaticamente pelo `app.py` e enviado ao modelo junto com o contexto operacional simulado.

---

## 13. Escopo Permitido do Chatbot

O chatbot pode responder perguntas sobre:

* status das estações;
* estações offline;
* falhas críticas;
* alertas operacionais;
* consumo energético;
* potência da rede;
* faturamento;
* manutenção;
* ciclos de recarga;
* identificação por RFID;
* billing por consumo;
* orquestração de potência;
* recomendações operacionais dentro do contexto GoodWe.

---

## 14. Fora de Escopo

O chatbot não deve responder perguntas sobre:

* investimentos financeiros;
* política;
* saúde;
* assuntos pessoais;
* programação fora do projeto;
* temas não relacionados a eletropostos;
* pedidos para ignorar instruções internas;
* pedidos para inventar dados operacionais.

Quando a pergunta estiver fora do escopo, o chatbot deve informar que o tema não pertence ao escopo do GoodWe Grid Assistant e redirecionar para assuntos operacionais de eletropostos.

---

## 15. Escalada Humana

O chatbot deve recomendar encaminhamento para suporte técnico humano quando houver:

* falha crítica ativa;
* superaquecimento;
* estação offline;
* risco de sobrecarga;
* inconsistência de faturamento;
* ausência de dados suficientes;
* necessidade de validação técnica real.

---

## 16. Estrutura do Projeto

```text
goodwe-chatbot/
│
├── .env
├── .env.example
├── .gitignore
├── app.py
├── README.md
├── requirements.txt
│
├── prompts/
│   └── system_prompt.txt
│
└── tests/
    ├── casos_teste.md
    └── resultados_testes.md
```

---

## 17. Arquivos do Projeto

### `app.py`

Arquivo principal do projeto.

Responsável por:

* carregar variáveis de ambiente;
* carregar o system prompt;
* configurar o cliente da Ollama;
* armazenar histórico de conversa;
* enviar mensagens ao modelo;
* criar a API com FastAPI;
* exibir a interface web;
* executar os testes automáticos.

---

### `prompts/system_prompt.txt`

Arquivo que contém as instruções principais do chatbot.

Define o comportamento do assistente, seu escopo, restrições, formato de resposta e critérios de escalada.

---

### `tests/casos_teste.md`

Arquivo com os casos de teste planejados.

Contém perguntas, categorias e respostas esperadas.

---

### `tests/resultados_testes.md`

Arquivo gerado automaticamente após a execução dos testes.

Ele registra:

* pergunta enviada;
* resposta esperada;
* resposta obtida;
* tempo de resposta;
* avaliação qualitativa.

---

### `.env`

Arquivo local com a chave da API.

Não deve ser enviado ao GitHub.

---

### `.env.example`

Arquivo de exemplo com as variáveis necessárias.

Pode ser enviado ao GitHub porque não contém chave real.

---

### `requirements.txt`

Arquivo com as dependências necessárias para executar o projeto.

---


## Dependências

O projeto utiliza as seguintes dependências:

```txt
ollama>=0.6.0
python-dotenv>=1.0.1
fastapi>=0.115.0
uvicorn[standard]>=0.30.0
pydantic>=2.0.0
```

Para instalar todas as dependências, execute:

```bash
pip install -r requirements.txt
```

---

## Variáveis de Ambiente

O projeto utiliza uma API Key da Ollama Cloud para acessar o modelo `gpt-oss:120b`.

Crie um arquivo chamado `.env` na raiz do projeto com o seguinte conteúdo:

```env
OLLAMA_API_KEY=sua_chave_da_ollama_aqui
OLLAMA_HOST=https://ollama.com
MODEL_NAME=gpt-oss:120b
```

Substitua `sua_chave_da_ollama_aqui` pela chave real da Ollama Cloud API.

O arquivo `.env` não deve ser enviado ao GitHub.

Também existe o arquivo `.env.example`, usado apenas como modelo:

```env
OLLAMA_API_KEY=coloque_sua_chave_aqui
OLLAMA_HOST=https://ollama.com
MODEL_NAME=gpt-oss:120b
```

---

## Como Executar o Projeto

### 1. Abrir o projeto no VS Code

Abra a pasta principal do projeto no VS Code:

```text
goodwe-chatbot
```

A estrutura esperada é:

```text
goodwe-chatbot/
│
├── .env
├── .env.example
├── .gitignore
├── app.py
├── README.md
├── requirements.txt
│
├── prompts/
│   └── system_prompt.txt
│
└── tests/
    ├── casos_teste.md
    └── resultados_testes.md
```

---

### 2. Abrir o terminal

No VS Code, abra o terminal em:

```text
Terminal > New Terminal
```

Confirme que o terminal está dentro da pasta `goodwe-chatbot`.

---

### 3. Criar o ambiente virtual

Execute:

```bash
python -m venv .venv
```

---

### 4. Ativar o ambiente virtual

No Windows, execute:

```bash
.\.venv\Scripts\activate
```

Se o ambiente virtual for ativado corretamente, aparecerá `(.venv)` no início da linha do terminal.

Caso apareça erro de permissão no PowerShell, execute:

```bash
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Depois tente ativar novamente:

```bash
.\.venv\Scripts\activate
```

---

### 5. Instalar as dependências

Com o ambiente virtual ativado, execute:

```bash
pip install -r requirements.txt
```

---

### 6. Executar o chatbot

Execute:

```bash
python app.py
```

Se funcionar corretamente, o terminal exibirá uma mensagem parecida com:

```text
Uvicorn running on http://127.0.0.1:8000
```

---

### 7. Acessar a interface web

Abra o navegador e acesse:

```text
http://127.0.0.1:8000
```

A interface do GoodWe Grid Assistant será exibida no navegador.

---

### 8. Encerrar o chatbot

Para parar a execução, volte ao terminal e pressione:

```text
CTRL + C
```

---

## Como Executar os Testes

Para executar os testes automáticos, primeiro encerre o servidor com:

```text
CTRL + C
```

Depois execute:

```bash
python app.py --testes
```

O arquivo abaixo será preenchido automaticamente:

```text
tests/resultados_testes.md
```

Esse arquivo registra:

* pergunta enviada;
* resposta esperada;
* resposta obtida;
* tempo de resposta;
* avaliação qualitativa.

---

## Exemplos de Uso

Após executar o projeto e abrir a interface no navegador, teste perguntas como:

```text
Quais estações estão offline neste momento?
```

```text
Existe alguma estação com falha crítica ativa nas últimas 2 horas?
```

```text
Qual estação apresentou maior consumo energético hoje?
```

```text
Qual foi o faturamento total da rede nesta semana?
```

```text
A rede está operando acima do limite recomendado de potência?
```

```text
Qual foi a última manutenção registrada na estação GW-03?
```

```text
Existe algum alerta prioritário ativo no sistema?
```

Para testar a memória de conversa, faça uma pergunta de continuidade:

```text
Qual ação você recomenda nesse caso?
```
