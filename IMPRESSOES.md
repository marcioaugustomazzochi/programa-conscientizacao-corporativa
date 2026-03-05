# 📢 Programa de Conscientização Corporativa

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
![Print 1 – Instalação das dependências via pip](prints/print1.png)

## 2️⃣ Configuração das variáveis de ambiente

Crie o arquivo .env (copiando de .env.exemplo) e configure suas credenciais:  
EMAIL_REMETENTE=seuemail@gmail.com  
EMAIL_SENHA=sua_senha_de_app  
SMTP_SERVIDOR=smtp.gmail.com  
SMTP_PORTA=587  
EMAIL_DESTINO=seuemail@gmail.com  

Comentário: As credenciais ficam fora do código, garantindo segurança. Nunca versionar o .env real no GitHub.  

**Print 2:**  
![Print 2 – Configuração do arquivo .env com credenciais](prints/print2.png)

## 3️⃣ Script de envio de e-mails

O script scripts/envio_emails.py realiza:  
- Leitura das variáveis de ambiente  
- Leitura do template HTML correspondente ao mês  
- Personalização do conteúdo com {{nome}} e {{mes}}  
- Conexão ao servidor SMTP e envio do e-mail  

Cada execução envia o e-mail referente a um mês de conscientização.  

**Print 3:**  
![Print 3 – Template HTML do e-mail pronto para envio](prints/print3.png)

## 4️⃣ Testando variáveis de ambiente

python -c "import os; from dotenv import load_dotenv; load_dotenv(); print(os.getenv('EMAIL_SENHA'))"  

Comentário: Isso confirma que o .env está correto.  

**Print 4:**  
![Print 4 – Teste do carregamento das variáveis de ambiente](prints/print4.png)

## 5️⃣ Execução do envio

Para enviar o e-mail de teste:  
python scripts/envio_emails.py  

Exemplo de logs no terminal:  
✅ Preparando envio do e-mail de Janeiro...  
Conectando em smtp.gmail.com:587...  
Login realizado com sucesso!  
📧 E-mail enviado para marciomazzochi@gmail.com referente a Janeiro ✅  

**Print 5:**  
![Print 5 – Execução do script mostrando envio do e-mail de Janeiro](prints/print5.png)  

**Print 6:**  
![Print 6 – E-mail de Janeiro recebido na caixa de entrada](prints/print6.png)

## 6️⃣ Automação Mensal (Opcional)

Configure um cron job no Linux para enviar os e-mails automaticamente:  
crontab -e  

Exemplo: enviar dia 1º de cada mês às 9h:  
0 9 1 * * /usr/bin/python3 /home/kali/programa-conscientizacao-corporativa/scripts/envio_emails.py  

Comentário: Isso garante que a campanha de conscientização será enviada automaticamente durante os 12 meses.  

**Print 7:**  
![Print 7 – Cron job configurado para envio mensal](prints/print7.png)

## Conclusão

Este projeto demonstra como automatizar campanhas de conscientização corporativa utilizando Python, SMTP e variáveis de ambiente.  
Garante educação contínua dos colaboradores, mantém a segurança das credenciais e facilita a escalabilidade e manutenção do projeto.
