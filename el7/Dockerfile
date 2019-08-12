FROM centos:7
LABEL AUTHOR "Ben Nied <spacewreckage@gmail.com>"

RUN yum -y install gcc make bison flex git yum-utils spectool rpmbuild yum-builddep
RUN git clone https://github.com/bnied/kernel-lt-aufs.git /opt/kernel-lt-aufs

ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT [ "./entrypoint.sh" ]
