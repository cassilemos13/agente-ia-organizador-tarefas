# 🤖 Agente IA – Organizador de Tarefas

Agente inteligente desenvolvido em Python, utilizando Google Agent Development Kit (ADK), Gemini e integração com a API do Trello para organizar tarefas por meio de conversas em linguagem natural.

## 🎯 Objetivo do projeto

O objetivo é desenvolver um agente de inteligência artificial capaz de auxiliar na organização das atividades diárias, criando, consultando, movimentando e removendo cartões diretamente em um quadro do Trello.

## 🛠️ Tecnologias utilizadas

- Python
- Google Agent Development Kit (ADK)
- Google Gemini
- Trello API
- Biblioteca py-trello
- python-dotenv

## ⚙️ Funcionalidades do agente

O agente possui cinco ferramentas principais:

1. **Consultar data e horário:** obtém o contexto temporal atual para organizar as atividades do dia.
2. **Adicionar tarefas:** cria cartões no quadro do Trello com nome e descrição.
3. **Listar tarefas:** consulta as atividades cadastradas, permitindo filtrar por status.
4. **Alterar status:** movimenta os cartões entre as listas A Fazer, Em Andamento e Concluído.
5. **Remover tarefas:** localiza um cartão pelo nome e realiza sua exclusão do Trello.

## 📋 Organização do quadro Trello

O agente utiliza um quadro chamado DIO, organizado em três listas:

- A Fazer
- Em andamento
- Concluído

## 🚀 Como executar o projeto

### 1. Pré-requisitos

- Python instalado.
- Git instalado.
- Conta no Trello.
- Chave de API e token do Trello.
- Chave de API do Google Gemini.

### 2. Clonar o repositório

```bash
git clone https://github.com/cassilemos13/agente-ia-organizador-tarefas.git
cd agente-ia-organizador-tarefas
```

### 3. Criar ambiente virtual

```bash
python -m venv .venv
```

Ativar no Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 4. Instalar dependências

```bash
pip install -r requirements.txt
```

### 5. Configurar as credenciais

Acesse a pasta:

`agents/agent04/agenttaskmanager/`

Faça uma cópia do arquivo `.env.exemplo` e renomeie a cópia para `.env`.

Preencha as variáveis com suas próprias credenciais:

```env
GOOGLE_GENAI_USE_VERTEXAI=0
GOOGLE_API_KEY=sua-chave-google
TRELLO_API_KEY=sua-chave-trello
TRELLO_API_SECRET=seu-segredo-trello
TRELLO_TOKEN=seu-token-trello
```

**Importante:** nunca publique o arquivo `.env` ou compartilhe suas credenciais. O arquivo está protegido pelo `.gitignore`.

### 6. Executar o agente

Na raiz do projeto, execute:

```bash
adk web agents/agent04/agenttaskmanager
```

O ADK Web será disponibilizado localmente em:

`http://127.0.0.1:8000`

## ✨ Melhoria implementada

Como melhoria do projeto, foi desenvolvida a ferramenta `remover_tarefa()`, permitindo que o agente exclua tarefas específicas diretamente do quadro do Trello.

A ferramenta percorre as listas do quadro, identifica o cartão pelo nome e realiza a exclusão, retornando uma mensagem de confirmação ou erro.

## 🧪 Testes realizados

Foram realizados testes práticos utilizando o ADK Web e o quadro real do Trello:

- Criação de uma tarefa de estudo de Python.
- Consulta das tarefas cadastradas.
- Alteração do status de A Fazer para Em Andamento.
- Criação de uma tarefa de teste para exclusão.
- Exclusão da tarefa de teste.
- Verificação da permanência das demais tarefas no quadro.

Os testes confirmaram o funcionamento das operações implementadas.

## 📁 Estrutura do projeto

```text
agente-ia-organizador-tarefas/
│
├── agents/
│   └── agent04/
│       └── agenttaskmanager/
│           ├── __init__.py
│           ├── agent.py
│           ├── .env.exemplo
│           └── .gitignore
│
├── .gitignore
├── README.md
└── requirements.txt
```

## 👩‍💻 Autora

Projeto desenvolvido por **Cassiane Lemos**, como parte dos estudos práticos de inteligência artificial e desenvolvimento de agentes com Python, na plataforma DIO.

---

**Projeto: Agente IA – Organizador de Tarefas**  
Integração entre inteligência artificial e organização de atividades com Trello.