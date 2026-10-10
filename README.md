# Hlídač n8n zvenku

GitHub Actions každých 10 minut volá `https://n8n.4lp.cz/healthz` a heartbeat
webhook (workflow „PK · Heartbeat pro externí hlídání (GitHub)“, ten sáhne do Neonu).
Po 3 neúspěšných pokusech job selže → GitHub pošle e-mail, a pokud je nastavený
secret `TELEGRAM_BOT_TOKEN`, přijde i zpráva na Telegram.
