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

## Instalação das dependências

Abra o arquivo `requirements.txt` e adicione:

python-dotenv  
schedule  

Depois instale todas as dependências:

pip install -r requirements.txt  

*Comentário:* Essas bibliotecas permitem gerenciar variáveis de ambiente e agendamento de tarefas.

## Configuração das variáveis de ambiente

Crie o arquivo `.env` (copiando de `.env.exemplo`) e configure suas credenciais:

EMAIL_REMETENTE=seuemail@gmail.com  
EMAIL_SENHA=sua_senha_de_app  
SMTP_SERVIDOR=smtp.gmail.com  
SMTP_PORTA=587  
EMAIL_DESTINO=seuemail@gmail.com  

*Comentário:* As credenciais ficam fora do código, garantindo segurança. **Nunca versionar o `.env` real** no GitHub.

## Script de envio de e-mails

O script `scripts/envio_emails.py` realiza leitura das variáveis de ambiente, leitura do template HTML correspondente ao mês, personalização do conteúdo com `{{nome}}` e `{{mes}}` e conexão ao servidor SMTP para envio do e-mail. Cada execução envia um mês de conscientização para o destinatário configurado.

## Testando variáveis de ambiente

python -c "import os; from dotenv import load_dotenv; load_dotenv(); print(os.getenv('EMAIL_SENHA'))"  

*Comentário:* Isso ajuda a confirmar que o `.env` está correto.

## Execução do envio

Para enviar o e-mail de teste:

python scripts/envio_emails.py  

- O script conecta ao SMTP, realiza login e envia o e-mail referente ao mês definido (por exemplo, Janeiro).  
- No terminal, você verá logs como:

✅ Preparando envio do e-mail de Janeiro...  
Conectando em smtp.gmail.com:587...  
Login realizado com sucesso!  
📧 E-mail enviado para marciomazzochi@gmail.com referente a Janeiro ✅

## Automação Mensal (Opcional)

Para enviar os e-mails automaticamente uma vez por mês, configure um cron job no Linux:

crontab -e  

Exemplo: enviar dia 1º de cada mês às 9h:

0 9 1 * * /usr/bin/python3 /home/kali/programa-conscientizacao-corporativa/scripts/envio_emails.py  

*Comentário:* Isso garante que a campanha de conscientização será enviada automaticamente durante os 12 meses.

## Resultados e Prints

Aqui você pode adicionar **7 prints** para documentar cada etapa do projeto:

**Print 1** – Configuração do arquivo `.env` com credenciais.  
**Print 2** – Instalação das dependências via pip.  
**Print 3** – Template HTML do e-mail pronto para envio.  
**Print 4** – Execução do script mostrando envio do e-mail de Janeiro.  
**Print 5** – E-mail de Janeiro recebido na caixa de entrada.  
**Print 6** – Cron job configurado para envio mensal.  
**Print 7** – Caixa de entrada mostrando os e-mails de Janeiro a Dezembro.

## Conclusão

Este projeto demonstra como automatizar campanhas de conscientização corporativa utilizando Python, SMTP e variáveis de ambiente. Garante educação contínua dos colaboradores, mantém segurança das credenciais e facilita escalabilidade e manutenção do projeto.
