FROM centos:7

RUN yum -y update
RUN yum install -y bind bind-chroot bind-utils unbound vim
RUN groupadd bind
RUN useradd -m bind -g bind -s /sbin/nologin

RUN /usr/sbin/rndc-confgen -a  -t /var/named/chroot -u bind -r /dev/urandom

EXPOSE 53/UDP
EXPOSE 53/TCP

COPY named.conf /var/named/chroot/etc/
COPY sample.com.zone /var/named/chroot/var/named/
COPY localhost.rev /var/named/chroot/var/named/
COPY named.root /var/named/chroot/var/named/
RUN chown -R bind:bind /var/named/chroot/

RUN yum -y clean all

CMD ["/usr/sbin/named", "-u", "bind", "-t", "/var/named/chroot", "-c", "/etc/named.conf", "-g"]