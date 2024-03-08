FROM almalinux/9-init
ENV container=docker

# Install requirements.
RUN yum -y install rpm dnf-plugins-core \
 && yum -y update \
 && yum -y install \
      sudo \
      python3 \
      python3-pip \
      iproute \
 && yum clean all

# Upgrade pip to latest version.
RUN pip3 install --upgrade pip

# Disable requiretty.
RUN sed -i -e 's/^\(Defaults\s*requiretty\)/#--- \1/'  /etc/sudoers
