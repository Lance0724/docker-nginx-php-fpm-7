# Pull base image
FROM mysql:5.7.26 as mysql57

# Locale Timezone
#RUN sed -i -e "s/LANG=\"en_US.UTF-8\"/LANG=\"zh_CN.UTF-8\"/g" /etc/locale.conf && \
RUN cp -p /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

# User
# RUN groupmod --gid 1000 mysql && usermod mysql --uid 1000 --gid 1000

# Httpd setting(mod_php)
#COPY ./conf/my.cnf /etc/my.cnf
#RUN chmod 644 /etc/my.cnf
#WORKDIR /var/lib/mysql
#VOLUME ["/var/log/"]

# Listen port
EXPOSE 3306

# Startup
#ENTRYPOINT ["/usr/sbin/mysqld"]

# RUN rpm -Uvh   http://repo.mysql.com/mysql80-community-release-el7-1.noarch.rpm && \
#    yum-config-manager --disable mysql56-community && \
#    yum-config-manager --enable mysql57-community && \
#    yum-config-manager --disable mysql80-community && \
#    yum install -y mysql-community-server

#RUN systemctl enable mysqld && \
#    semanage port -a -t mysqld_port_t -p tcp 3306 && \
#    mysqld_safe --skip-grant-tables&

#RUN mysql -hlocalhost -uroot mysql  -e "UPDATE user SET password=PASSWORD("zhonghezhikong") WHERE user='root'; FLUSH PRIVILEGES;" && \
#    pkill mysqld_safe && \
#    systemctl start mysqld 
    

#RUN yum clean all

#CMD mysql