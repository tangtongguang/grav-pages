---
title: Linux

page-toc:
  active: true
---

### jenkins

`visudo` 修改jenkins执行bash脚本的权限

```bash
jenkins ALL=NOPASSWD: /var/lib/jenkins/script/
jenkins ALL=(ALL) NOPASSWD:ALL
```


### docker 无响应时

```bash
netstat -ntpl
#查看服务

ps auxwwf
#查看进程树

kill -9 pid
#杀死进程 -9 强制

```

### git 保存密码

`git config credential.helper manager`

### vim docs

`find /usr/share/vim/vim81/doc -name "*.txt" -exec perl /usr/share/vim/vim81/doc/vim2html.pl /usr/share/vim/vim81/doc/tags {} \;`

### man-pages

Man2html configuration file for apache2

```apache
<Location "/cgi-bin/man/">
  <IfModule mod_authz_host.c>
    Require local
    # Require ip 192.0.2.0/24
    # Require ip 2001:db8::a00:20ff:fea7:ccea/10
  </IfModule>
</Location>
```


