# renew-letsencrypt
One script to renew Let's Encrypt certificate with crontab.

# Steps

Clone "letsencrypt/letsencrypt" to your repository
cd /opt/

git clone https://github.com/letsencrypt/letsencrypt

cd letsencrypt

chmod +x letsencrypt-auto

git clone renew_letsencrypt.sh to your server.

cd /opt/

git clone https://github.com/infinityonhigh9669/renew-letsencrypt

cd renew-letsencrypt

chmod +x renew_letsencrypt.sh

# Add script to crond at 00:00 on day-of-month 1.

crontab -e

# Add the line below:

@monthly /opt/renew-lets-encrypt/renew_letsencrypt.sh

# Restart CRON service

service cron restart
