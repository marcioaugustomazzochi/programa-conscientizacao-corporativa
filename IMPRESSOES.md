# 📢 Programa de Conscientização Corporativa

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/) 
[![Dependências](https://img.shields.io/badge/Dependencies-pip-green)](https://pip.pypa.io/) 
[![Env Variables](https://img.shields.io/badge/Env%20Variables-.env-yellow)](#) 
[![SMTP](https://img.shields.io/badge/SMTP-Config-orange)](#) 
[![Testado](https://img.shields.io/badge/Tested-Pass-brightgreen)](#) 
[![Automação](https://img.shields.io/badge/Automation-Cron-blueviolet)](#)

Este projeto tem como objetivo automatizar o envio de campanhas mensais de conscientização em Segurança da Informação via e-mail, garantindo que os colaboradores recebam conteúdos educativos ao longo de 12 meses.

## Estrutura do Projeto

programa-conscientizacao-corporativa/  
├── requirements.txt         # Dependências do Python  
├── .env                     # Variáveis de ambiente com credenciais de e-mail  
├── scripts/envio_emails.py  # Script principal para envio dos e-mails  
├── emails/                  # Templates HTML de cada mês  
│   ├── janeiro.html  
│   ├── fevereiro.html  
│   └── ...  
└── prints/                  # Capturas de tela documentando execução e resultados  

## 1️⃣ Instalação das dependências

No arquivo requirements.txt, adicione:  
python-dotenv  
schedule  

Depois instale todas as dependências:  
pip install -r requirements.txt  

Comentário: Essas bibliotecas permitem gerenciar variáveis de ambiente e agendamento de tarefas.  

**Print 1:**  
<img width="1920" height="936" alt="print_01_clone_repositorio" src="https://github.com/user-attachments/assets/d53dac56-ae9a-46b3-b75b-f26dc9f13c72" />

## 2️⃣ Configuração das variáveis de ambiente

Crie o arquivo .env (copiando de .env.exemplo) e configure suas credenciais:  
EMAIL_REMETENTE=seuemail@gmail.com  
EMAIL_SENHA=sua_senha_de_app  
SMTP_SERVIDOR=smtp.gmail.com  
SMTP_PORTA=587  
EMAIL_DESTINO=seuemail@gmail.com  

Comentário: As credenciais ficam fora do código, garantindo segurança. Nunca versionar o .env real no GitHub.  

**Print 2:**  
<img width="1920" height="936" alt="print_02_venv_ativo" src="https://github.com/user-attachments/assets/ce7a221e-7d2a-4a04-9847-f7587bfc45a4" />

## 3️⃣ Script de envio de e-mails

O script scripts/envio_emails.py realiza:  
- Leitura das variáveis de ambiente  
- Leitura do template HTML correspondente ao mês  
- Personalização do conteúdo com {{nome}} e {{mes}}  
- Conexão ao servidor SMTP e envio do e-mail  

Cada execução envia o e-mail referente a um mês de conscientização.  

**Print 3:**  
<img width="1920" height="936" alt="print_03_dependencias_instaladas" src="https://github.com/user-attachments/assets/5cf2168c-7c51-4843-8fae-dc4ef2e92b2c" />

## 4️⃣ Testando variáveis de ambiente

python -c "import os; from dotenv import load_dotenv; load_dotenv(); print(os.getenv('EMAIL_SENHA'))"  

Comentário: Isso confirma que o .env está correto.  

**Print 4:**  
<img width="1920" height="936" alt="print_04_env_configurado" src="https://github.com/user-attachments/assets/dc5febdb-5a7d-40cd-ae0d-2f8aad3af2b6" />

## 5️⃣ Execução do envio

Para enviar o e-mail de teste:  
python scripts/envio_emails.py  

Exemplo de logs no terminal:  
✅ Preparando envio do e-mail de Janeiro...  
Conectando em smtp.gmail.com:587...  
Login realizado com sucesso!  
📧 E-mail enviado para marciomazzochi@gmail.com referente a Janeiro ✅  

**Print 5:**  
<img width="1920" height="936" alt="print_teste_variavel_env" src="https://github.com/user-attachments/assets/43719f9e-3f6d-457d-87ac-cf9a2516a6ea" />

**Print 6:**  
<img width="1920" height="936" alt="print preparação para o envio" src="https://github.com/user-attachments/assets/48670593-2f02-430c-b1e6-a141c7f09851" />

## 6️⃣ Automação Mensal (Opcional)

Configure um cron job no Linux para enviar os e-mails automaticamente:  
crontab -e  

Exemplo: enviar dia 1º de cada mês às 9h:  
0 9 1 * * /usr/bin/python3 /home/kali/programa-conscientizacao-corporativa/scripts/envio_emails.py  

Comentário: Isso garante que a campanha de conscientização será enviada automaticamente durante os 12 meses.  

**Print 7:**  
<img width="1920" height="1080" alt="Print email enviado corretamente" src="https://github.com/user-attachments/assets/67c9a2fe-98c1-473a-b688-fec2cb09ccfe" />  
<img width="1920" height="1080" alt="print todos os emails enviados " src="https://github.com/user-attachments/assets/5c64b135-0642-4dd7-ac3e-4ea38ea70bda" />

## Conclusão

Este projeto demonstra como automatizar campanhas de conscientização corporativa utilizando Python, SMTP e variáveis de ambiente.  
Garante educação contínua dos colaboradores, mantém a segurança das credenciais e facilita a escalabilidade e manutenção do projeto.
