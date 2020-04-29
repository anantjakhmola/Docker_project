FROM ubuntu:16.04

RUN apt update
RUN apt install -y curl wget gnupg less lsof net-tools git apt-utils -y


# WORKDIR
RUN mkdir /works
WORKDIR /works

# Python
RUN apt-get install apt-transport-https
RUN apt-get update
RUN apt install python3 -y
ENV PATH="${PATH}:/usr/lib/python3/"
ENV PATH="${PATH}:/usr/lib/python3/dist-packages/"
ENV PATH="${PATH}:/usr/lib/python3.5/"

#RUN pub global activate webdev
#RUN pub global activate stagehand

#
# CODE-SERVER
RUN wget https://github.com/cdr/code-server/releases/download/1.939-vsc1.33.1/code-server1.939-vsc1.33.1-linux-x64.tar.gz
RUN tar xzf code-server1.939-vsc1.33.1-linux-x64.tar.gz -C ./ --strip-components 1


# FLUTTER
#RUN apt-get install xz-utils -y 
#RUN wget https://storage.googleapis.com/flutter_infra/releases/stable/linux/flutter_linux_v1.12.13+hotfix.9-stable.tar.xz
RUN mkdir /works/development
WORKDIR /works/development
#RUN tar xf ../flutter_linux_v1.12.13+hotfix.9-stable.tar.xz
#ENV PATH="${PATH}:/works/development/flutter/bin"
#RUN flutter precache
#RUN flutter packages global activate webdev 



#
# FLUTTER CODE
#RUN git clone https://github.com/flutter/flutter_web.git
#WORKDIR /works/development/flutter_web/examples/hello_world/
#RUN flutter packages upgrade
#RUN flutter pub get
RUN git clone https://github.com/anantjakhmola/python_TUI.git pythondir
WORKDIR /works/development/pythondir/
