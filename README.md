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

```text
programa-conscientizacao-corporativa
│
├─ emails
│  ├─ mes01_phishing.html
│  ├─ mes02_senhas.html
│  └─ ...
│
├─ src
│  ├─ send_email.py
│  └─ scheduler.py
│
├─ config
│  └─ .env
│
├─ requirements.txt
├─ .gitignore
└─ README.md
🚀 Tecnologias utilizadas

Python 3

SMTP (envio de e-mail)

python-dotenv

schedule

HTML para templates

⚙️ Configuração
1️⃣ Clonar o repositório
git clone https://github.com/SEU-USUARIO/programa-conscientizacao-corporativa.git
cd programa-conscientizacao-corporativa
2️⃣ Criar ambiente virtual
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
3️⃣ Configurar variáveis de ambiente

Criar arquivo:

config/.env

Exemplo:

EMAIL_USER=seuemail@gmail.com
EMAIL_PASS=sua_senha_de_app
EMAIL_TO=destinatario@empresa.com

⚠️ Nunca versionar credenciais reais.

▶️ Execução
python src/scheduler.py
📆 Temas sugeridos para os 12 meses

Phishing

Senhas fortes

Engenharia social

Uso seguro do e-mail

Dispositivos removíveis

Trabalho remoto seguro

Atualizações e patches

Backup

Wi-Fi público

LGPD e privacidade

Ransomware

Boas práticas gerais

🔐 Boas práticas de segurança

❌ Não versionar o arquivo .env

❌ Não expor senhas ou tokens

✅ Utilizar senha de aplicativo de e-mail

✅ Revisar lista de destinatários

✅ Validar conformidade com LGPD

📊 Possíveis melhorias futuras

📈 Métricas de abertura de e-mail

🏢 Suporte multiempresa

🌐 Interface web administrativa

☁️ Execução via GitHub Actions

📱 Templates responsivos

👨‍💻 Autor

Projeto desenvolvido para fins educacionais e de promoção da cultura de Segurança da Informação.

📄 Licença

Este projeto é destinado a fins educacionais e pode ser adaptado conforme a necessidade da organização.
