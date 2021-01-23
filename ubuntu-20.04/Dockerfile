FROM ubuntu:20.04

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    apt-utils \
    bash \
    ca-certificates \
    #iproute2 \
    #locales \
    python3 \
    #python3-pip \
    #python3-setuptools \
    #rsyslog \
    #software-properties-common \
    sudo \
    #systemd \
    #systemd-cron \
  #&& rm -Rf /var/lib/apt/lists/* \
  #&& rm -Rf /usr/share/doc && rm -Rf /usr/share/man \
  && apt-get clean
#RUN sed -i 's/^\($ModLoad imklog\)/#\1/' /etc/rsyslog.conf

# Fix potential UTF-8 errors with ansible-test.
#RUN locale-gen en_US.UTF-8

#RUN pip3 install ansible

# Install Ansible inventory file.
#RUN mkdir -p /etc/ansible
#RUN echo "[local]\nlocalhost ansible_connection=local" > /etc/ansible/hosts

# Remove unnecessary getty and udev targets that result in high CPU usage when using
# multiple containers with Molecule (https://github.com/ansible/molecule/issues/1104)
#RUN rm -f /lib/systemd/system/systemd*udev* \
#  && rm -f /lib/systemd/system/getty.target

#VOLUME ["/sys/fs/cgroup", "/tmp", "/run"]
#CMD ["/lib/systemd/systemd"]
