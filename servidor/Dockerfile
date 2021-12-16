FROM python:3
LABEL version="1.0.0" description="Aplicação para DSI" maintainer="Redes dockers"
WORKDIR /var/www/redes_dockers
COPY . .
EXPOSE 11120
RUN chmod +x ./commands.sh
RUN ./commands.sh
CMD ["python3", "tcpserver2.py"]
