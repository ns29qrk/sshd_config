# sshd_config 日本語コメ

OpenSSH 8.9 Configuration for Ubuntu22  
version 0.1.5

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

## ポートの変更

必要がれば「Port 49152」を変更してください。

```Shell
xxx$ sudo vim /etc/ssh/sshd_config.d/xxx_sshd_config.conf
```

```diff
#D Port 22
-Port 49152
+Port 55522
```

変更できるポート番号は22または49152から65535までとなっています。

それ以外も設定はできますが、他のサービスとバッティングするかもしれません。

*注 ) ここで設定している55522はサンプルです。

## SSHのリロード

```Shell
~$ sudo systemctl restart sshd.service
```

## 更新履歴
### version 0.1.5
Port番号を変更

### version 0.1.4
Subsystem Sftpコメントアウト

### version 0.1.3
CompressionLevel削除  
HashKnownHosts削除  
CheckHostIP削除  

### version 0.1.2
HostKeyAlgorithmsの修正

### version 0.1.1
PubkeyAcceptedKeyTypesの修正

### version 0.1.0
初稿