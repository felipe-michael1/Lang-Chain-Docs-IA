# 📚 Converse com seus Documentos usando IA (RAG)

Aplicação web interativa que permite **conversar com documentos PDF utilizando Inteligência Artificial**, baseada na arquitetura **RAG (Retrieval-Augmented Generation)**.

O sistema permite ao usuário enviar documentos, indexá-los automaticamente e realizar perguntas em linguagem natural, recebendo respostas **baseadas no conteúdo real dos arquivos**, com indicação das fontes.

---

## 🚀 Visão Geral

Esta aplicação foi desenvolvida para resolver um problema comum em ambientes corporativos e acadêmicos:

> **Como extrair conhecimento rapidamente de documentos extensos sem precisar lê-los por completo?**

A solução combina:

* **Indexação semântica**
* **Busca vetorial**
* **Modelos de linguagem (LLMs)**
* **Interface web simples e intuitiva**

---

## 🧠 Arquitetura (RAG)

O fluxo da aplicação segue o padrão **Retrieval-Augmented Generation**:

1. Upload de documentos PDF
2. Extração e divisão do texto (chunking)
3. Geração de embeddings
4. Armazenamento vetorial com FAISS
5. Recuperação de contexto relevante
6. Geração de resposta com LLM
7. Exibição da resposta com fontes

```text
Usuário → Streamlit → Retriever (FAISS)
                     ↓
                Documentos relevantes
                     ↓
                 LLM (Resposta)
```

---

## 🛠️ Tecnologias Utilizadas

### 🔹 Frontend

* **Streamlit** (UI interativa)

### 🔹 Backend / IA

* **Python**
* **LangChain**
* **FAISS** (Vector Store)
* **HuggingFace Embeddings (BAAI/bge-m3)**

### 🔹 Modelos de Linguagem (LLMs)

Suporte a múltiplos provedores:

* HuggingFace Hub
* OpenAI
* Ollama (local)
* Groq (LLaMA 3)

---

## 📂 Estrutura do Projeto

```text
.
├── app.py
├── vectorstore/
│   └── db_faiss/
├── .env
├── requirements.txt
└── README.md
```

---

## 📄 Funcionalidades

* Upload de múltiplos PDFs
* Indexação automática dos documentos
* Conversa contextual com histórico
* Recuperação semântica (MMR)
* Respostas em português
* Exibição das fontes utilizadas
* Suporte a múltiplos LLMs
* Execução local ou via APIs externas

---

## 💬 Exemplo de Uso

**Pergunta do usuário:**

> Quais são os principais conceitos abordados neste documento?

**Resposta do sistema:**

* Texto gerado com base nos PDFs
* Fontes exibidas por página e documento

---

## ⚙️ Como Executar o Projeto

### 1️⃣ Clonar o repositório

```bash
git clone https://github.com/seu-usuario/chat-com-documentos-rag.git
cd chat-com-documentos-rag
```

---

### 2️⃣ Criar ambiente virtual

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

---

### 3️⃣ Instalar dependências

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Configurar variáveis de ambiente

Crie um arquivo `.env` com as chaves necessárias:

```env
OPENAI_API_KEY=seu_token
HUGGINGFACEHUB_API_TOKEN=seu_token
GROQ_API_KEY=seu_token
```

---

### 5️⃣ Executar a aplicação

```bash
streamlit run app.py
```

---

## 🧪 Estratégias Técnicas Utilizadas

* **Chunking inteligente** com sobreposição
* **Busca vetorial MMR** para maior diversidade
* **History-aware retriever** (contexto de conversa)
* Separação clara entre:

  * Indexação
  * Recuperação
  * Geração de respostas

---

## 🔐 Boas Práticas

* Uso de `.env` para credenciais
* Código modular e legível
* Arquitetura extensível para novos modelos
* Preparado para escalabilidade futura

---

## 🚀 Possíveis Melhorias Futuras

* Cache de embeddings
* Persistência do histórico em banco
* Autenticação de usuários
* Upload de outros formatos (DOCX, TXT)
* Interface de seleção de modelo
* Deploy em cloud (AWS / GCP)

---

## 🧠 O que este projeto demonstra

* Conhecimento em **IA aplicada**
* Arquitetura **RAG**
* Integração com múltiplos LLMs
* Uso prático de embeddings e vetores
* Pensamento de **system design**
* Capacidade de transformar IA em produto

---

## 👤 Autor

Felipe

Projeto desenvolvido para estudo, portfólio e demonstração de habilidades em **IA, Backend e Engenharia de Software**.
