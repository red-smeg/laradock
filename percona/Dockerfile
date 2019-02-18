FROM percona:5.7
USER root

LABEL maintainer="DTUNES <diegotdai@gmai.com>"

# Added by M.B for additional utils required to use sync scripts
#RUN apt-get update && yes N | apt-get install -y \
#  --no-install-suggests qpress percona-xtrabackup-24 \
#  && rm -rf /var/lib/apt/lists/*

RUN yum -y install qpress percona-xtrabackup-24

# Add Sync scripts and key files afterward

RUN chown -R mysql:root /var/lib/mysql/

COPY my.cnf /etc/mysql/conf.d/my.cnf

CMD ["mysqld"]

EXPOSE 3306
