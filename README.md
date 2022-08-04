# sshd_config 日本語コメ

OpenSSH 8.9 Configuration for Ubuntu22  
version 0.12

## sshd_confingのダウンロード

xxxは任意で変更してください

```Shell
~$ mkdir xxx
~$ cd xxx
xxx$ git clone https://github.com/ns29qrk/sshd_config.git .
```

## sshd_confingをsshd_config.dにコピー

```Shell
xxx$ sudo cp sshd_config /etc/ssh/sshd_config.d/xxx_sshd_config.conf
xxx$ cd ..
~$ rm -Rf xxx
```

## SSHのリロード

```Shell
~$ sudo systemctl restart sshd
sudo systemctl restart sshd.service
```

## 更新履歴
version 0.12 HostKeyAlgorithmsの修正
version 0.11 PubkeyAcceptedKeyTypesの修正
version 0.1 初稿