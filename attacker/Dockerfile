FROM ubuntu
ENV TZ=America/Argentina/Buenos_Aires
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get -y update
RUN apt-get -y install python3 python3-pip wget iproute2
RUN apt-get -y install python3-scapy
RUN wget -O /usr/bin/sshesame https://github.com/jaksi/sshesame/releases/download/v0.0.18/sshesame-linux-amd64
RUN chmod +x /usr/bin/sshesame
COPY sshesame.yml /etc/
CMD sshesame -config /etc/sshesame.yml
