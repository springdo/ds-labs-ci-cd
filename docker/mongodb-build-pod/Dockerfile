FROM openshift/jenkins-slave-base-centos7:latest

USER root

RUN echo "[mongodb-org-3.6]" >> /etc/yum.repos.d/mongodb-org-3.6.repo && \
    echo "name=MongoDB Repository" >> /etc/yum.repos.d/mongodb-org-3.6.repo && \
    echo "baseurl=https://repo.mongodb.org/yum/redhat/7/mongodb-org/3.6/x86_64/" >> /etc/yum.repos.d/mongodb-org-3.6.repo && \
    echo "gpgcheck=1" >> /etc/yum.repos.d/mongodb-org-3.6.repo && \
    echo "enabled=1" >> /etc/yum.repos.d/mongodb-org-3.6.repo && \
    echo "gpgkey=https://www.mongodb.org/static/pgp/server-3.6.asc" >> /etc/yum.repos.d/mongodb-org-3.6.repo && \
    cat /etc/yum.repos.d/mongodb-org-3.6.repo && \ 
    yum install -y mongodb-org-tools 

USER 1001

# useful for verification of install
# RUN go version
# RUN go env
