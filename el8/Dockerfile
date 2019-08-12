FROM oraclelinux:8-slim
LABEL AUTHOR "Ben Nied <spacewreckage@gmail.com>"

RUN dnf -y install gcc make bison flex git dnf-utils spectool rpm-build dnf-plugins-core
RUN git clone https://github.com/bnied/kernel-lt-aufs.git /opt/kernel-lt-aufs

ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT [ "./entrypoint.sh" ]
