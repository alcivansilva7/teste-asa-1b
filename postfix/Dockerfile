from ubuntu:latest


RUN apt update -y
RUN apt upgrade -y

RUN apt install postfix telnet -y

COPY main.cf /etc/postfix

EXPOSE 25/tcp
EXPOSE 587/tcp

CMD [ "/usr/sbin/postfix", "start-fg" ]