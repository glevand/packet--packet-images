FROM arm64v8/fedora:29

LABEL Description="Packet's Fedora 29 OS base image" Vendor="Packet.net" Version="2018.08.24.00"

RUN yum update  ${YUM_OPTS} -y && yum install ${YUM_OPTS} -y \
	audit \
	bash \
	bash-completion \
	ca-certificates \
	chrony \
	cloud-init \
	cloud-utils-growpart \
	curl \
	device-mapper-multipath \
	dhclient \
	ethstatus \
	hwdata \
	ioping \
	iotop \
	iperf \
	iscsi-initiator-utils \
	keyutils \
	logrotate \
	make \
	mdadm \
	mg \
	mtr \
	net-tools \
	NetworkManager-team \
	NetworkManager-tui \
	nmap-ncat \
	ntp \
	ntpdate \
	openssh-clients \
	openssh-server \
	openssl \
	parted \
	passwd \
	pciutils \
	redhat-lsb-core \
	rsync \
	rsyslog \
	screen \
	socat \
	sudo \
	sysstat \
	systemd \
	tar \
	tcpdump \
	teamd \
	tmux \
	traceroute \
	tuned \
	vim \
	wget \
	&& yum clean all

# Remove default dhcp config
RUN rm -f /etc/sysconfig/network-scripts/ifcfg-*

# Adjust root account
RUN passwd -d root && passwd -l root

# vim: set tabstop=4 shiftwidth=4:
