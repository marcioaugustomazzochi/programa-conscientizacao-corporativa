![Python](https://img.shields.io/badge/Python-3.x-blue)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![License](https://img.shields.io/badge/license-MIT-green)

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
