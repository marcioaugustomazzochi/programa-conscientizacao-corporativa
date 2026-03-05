[![Python 3.x](https://img.shields.io/badge/Python-3.x-blue)](https://www.python.org/)
[![SMTP Configurado](https://img.shields.io/badge/SMTP-OK-blueviolet)]()
[![Env Variables](https://img.shields.io/badge/Env-.env-yellow)]()
[![Automação Cron](https://img.shields.io/badge/Automação-Cron-red)]()
[![Docker Suportado](https://img.shields.io/badge/Docker-Sim-blue)]()
[![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow)]()
[![License MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Versão](https://img.shields.io/badge/Versão-1.0.0-lightgrey)]()
[![Concluído](https://img.shields.io/badge/Concluído-Parcial-brightgreen)]()
[![Code Quality](https://img.shields.io/badge/Qualidade-Clean-blue)]()

# 📢 Programa de Conscientização Corporativa

Sistema automatizado de envio mensal de e-mails para campanhas de conscientização em Segurança da Informação no ambiente corporativo.

---

## 🎯 Objetivo

Este projeto tem como finalidade apoiar empresas na promoção da cultura de Segurança da Informação por meio do envio programado de conteúdos educativos aos colaboradores.

A solução automatiza campanhas de awareness ao longo de 12 meses, contribuindo para:

- ✅ Redução de riscos humanos  
- ✅ Fortalecimento da cultura de segurança  
- ✅ Apoio a iniciativas de Compliance e LGPD  
- ✅ Educação contínua dos colaboradores  

---

## 🛠️ Ferramentas e Tecnologias

Este projeto utiliza as seguintes ferramentas e tecnologias:

- 🐍 **Python 3.x** – Linguagem principal para automação, leitura de templates HTML e envio de e-mails via SMTP.  
- 📦 **pip** – Gerenciador de pacotes para instalar dependências do projeto.  
- 🌿 **python-dotenv** – Biblioteca para carregar variáveis de ambiente de forma segura, mantendo credenciais fora do código.  
- ⏱️ **schedule** – Biblioteca para agendamento de tarefas periódicas em Python, permitindo execução mensal automatizada.  
- 📧 **SMTP** – Protocolo de envio de e-mails para integração com servidores de e-mail corporativos ou pessoais.  
- 🎨 **HTML/CSS** – Para criação de templates de e-mails educativos e visualmente atrativos.  
- 🖥️ **cron (Linux/Mac)** – Agendador de tarefas do sistema para automatizar o envio mensal de e-mails.  
- 🔧 **Git/GitHub** – Controle de versão do código e documentação do projeto, hospedagem de repositório público.  
- 🐳 **Docker (opcional)** – Para containerização do sistema, garantindo consistência do ambiente de execução.

  ---

  ## 🧠 Como funciona

O sistema realiza:

1. 📅 Agendamento automático mensal  
2. 📧 Envio de e-mails educativos em HTML  
3. 🔐 Uso de variáveis de ambiente para credenciais  
4. 🐍 Orquestração via Python  
5. ⚙️ Possibilidade de execução via scheduler ou cron  

---

## 📂 Estrutura do projeto

programa-conscientizacao-corporativa/  
│  
├── emails/  
│   ├── janeiro.html  
│   ├── fevereiro.html  
│   ├── marco.html  
│   └── ...  
│  
├── scripts/  
│   └── envio_emails.py  
│  
├── .env.exemplo  
├── requirements.txt  
└── README.md  

---

## 🚀 Como executar

### 1️⃣ Clonar o repositório

git clone https://github.com/SEU-USUARIO/programa-conscientizacao-corporativa.git  
cd programa-conscientizacao-corporativa  

---

### 2️⃣ Criar e ativar ambiente virtual (opcional)

python -m venv venv  
source venv/bin/activate  # Linux/Mac  
venv\Scripts\activate     # Windows  

---

### 3️⃣ Instalar dependências

pip install -r requirements.txt  

---

### 4️⃣ Configurar variáveis de ambiente

Copie o arquivo de exemplo:

cp .env.exemplo .env  

Edite o `.env` com suas credenciais SMTP.

Exemplo:

EMAIL_REMETENTE=seuemail@empresa.com  
EMAIL_SENHA=sua_senha_segura  
SMTP_SERVIDOR=smtp.empresa.com  
SMTP_PORTA=587  
EMAIL_DESTINO=destinatario@empresa.com  

⚠️ **Nunca versionar o arquivo `.env` real.**

---

### 5️⃣ Executar o sistema

Execução manual:

python scripts/envio_emails.py  

Se houver scheduler:

python src/scheduler.py  

---

## 🗓️ Agendamento automático (opcional)

### Linux (cron)

crontab -e  

Exemplo de execução mensal:

0 9 1 * * /usr/bin/python3 /caminho/projeto/scripts/envio_emails.py  

---

## 🛡️ Boas práticas de segurança

- 🔒 Utilize senha de aplicativo no e-mail  
- 🔒 Não exponha credenciais no código  
- 🔒 Use variáveis de ambiente  
- 🔒 Restrinja permissões do SMTP  
- 🔒 Mantenha logs de envio  

---

## 📌 Possíveis melhorias futuras

- 📊 Dashboard de métricas de abertura  
- 📩 Integração com serviços de e-mail (SendGrid, SES)  
- 👥 Segmentação por área/departamento  
- 🧪 Testes automatizados  
- 🐳 Containerização com Docker  

---

## 👨‍💻 Autor

Projeto desenvolvido para fins educacionais e de demonstração de automação em campanhas de Segurança da Informação.
