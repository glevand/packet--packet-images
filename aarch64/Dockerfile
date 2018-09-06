FROM arm64v8/fedora:28

LABEL Description="Packet's Fedora 28 OS base image" Vendor="Packet.net" Version="2018.08.24.00"

RUN yum update  ${YUM_OPTS} -y && yum install ${YUM_OPTS} -y \
	openssh-server \
	passwd \
	&& yum clean all

# Remove default dhcp config
RUN rm -f /etc/sysconfig/network-scripts/ifcfg-*

# Adjust root account
RUN passwd -d root && passwd -l root

# vim: set tabstop=4 shiftwidth=4:
