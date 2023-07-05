FROM ubuntu:latest


RUN apt update -y
RUN apt upgrade -y

RUN apt install postfix dovecot-imapd dovecot-pop3d telnet -y

COPY main.cf /etc/postfit
COPY start_mail.sh /etc/init.d
COPY ./dovecot/* /etc/dovecot/conf.d

RUN chmod 755 /etc/init.d/start_mail.sh

EXPOSE 25/tcp
EXPOSE 587/tcp
EXPOSE 110/tcp
EXPOSE 143/tcp

CMD [ "/etc/init.d/start_mail.sh"]