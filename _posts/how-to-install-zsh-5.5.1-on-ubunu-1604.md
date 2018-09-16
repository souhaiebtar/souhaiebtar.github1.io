---
title: How to install zsh 5.5.1 on ubuntu 1604
layout: post
img: opensnitch.png
---
###Install go and config [1][1] [2][2]

```SHELL
wget http://ftp.br.debian.org/debian/pool/main/n/ncurses/libtinfo6_6.1+20180210-4_amd64.deb && wget http://ftp.br.debian.org/debian/pool/main/z/zsh/zsh-common_5.5.1-1_all.deb && wget http://ftp.br.debian.org/debian/pool/main/z/zsh/zsh_5.5.1-1+b1_amd64.deb
&& dpkg -i libtinfo6_6.1+20180210-4_amd64.deb && dpkg -i zsh-common_5.5.1-1_all.deb && dpkg -i zsh_5.5.1-1+b1_amd64.deb

```
___

#### Install opensnitch [3][3]

1. Install dependecies
```SHELL
sudo apt-get install protobuf-compiler libpcap-dev libnetfilter-queue-dev python3-pip
go get github.com/golang/protobuf/protoc-gen-go
go get -u github.com/golang/dep/cmd/dep
python3 -m pip install --user grpcio-tools
go get github.com/evilsocket/opensnitch
cd $GOPATH/src/github.com/evilsocket/opensnitch
make
sudo make install
sudo systemctl enable opensnitchd
sudo service opensnitchd start
cd $GOPATH/src/github.com/evilsocket/opensnitch/ui
cp opensnitch_ui.desktop ~/.config/autostart/
```



[1]: https://medium.com/@patdhlk/how-to-install-go-1-9-1-on-ubuntu-16-04-ee64c073cd79
[2]: https://www.samclarke.com/installing-go-1-9-on-ubuntu-16-04/

[3]: https://github.com/evilsocket/opensnitch
