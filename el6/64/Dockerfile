FROM centos:centos6
LABEL AUTHOR "Ben Nied <spacewreckage@gmail.com>"

ADD cfg/devtoolset-3.repo /etc/yum.repos.d/
RUN yum -y install gcc make bison flex git yum-utils spectool rpmbuild yum-builddep devtoolset-3-toolchain
RUN git clone https://github.com/bnied/kernel-lt-aufs.git /opt/kernel-lt-aufs

ADD entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
ENTRYPOINT [ "./entrypoint.sh" ]
