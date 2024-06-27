FROM nginx:latest

COPY ./ssl/icecweb.com_ssl_certificate.cer /etc/nginx/ssl/
COPY ./ssl/_.icecweb.com_private_key.key /etc/nginx/ssl/
COPY ./ssl/_.icecweb.com_ssl_certificate_INTERMEDIATE.cer /etc/nginx/ssl/

RUN chmod 644 /etc/nginx/ssl/icecweb.com_ssl_certificate.cer && \
    chmod 600 /etc/nginx/ssl/_.icecweb.com_private_key.key

RUN cat /etc/nginx/ssl/icecweb.com_ssl_certificate.cer /etc/nginx/ssl/_.icecweb.com_ssl_certificate_INTERMEDIATE.cer > /etc/nginx/ssl/certificate.crt && \
    chmod 644 /etc/nginx/ssl/certificate.crt