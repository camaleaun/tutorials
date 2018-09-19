# Chave SSH e conectar servidor via SSH

Visualiza sua chave.

```sh
$ cat ~/.ssh/id_rsa.pub
```

Gera a chave.

```sh
$ ssh-keygen -t rsa -C "account@domain"
```

Copia sua chave para as autorizadas no servidor.

```sh
$ cat ~/.ssh/id_rsa.pub | ssh username@server 'cat >> ~/.ssh/authorized_keys'
```

Conecta ao servidor.

```sh
$ ssh username@server
```

Recebe no servidor a atual versão do repositório.

```sh
$ git pull
```

Scan after clone keys.

```sh
$ ssh-keyscan -t rsa domain >> ~/.ssh/known_hosts
```
