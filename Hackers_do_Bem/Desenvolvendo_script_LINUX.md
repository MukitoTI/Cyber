# SCRIPTS SH

### verificação.sh

O `netstat` lista todas as conexões ativas no sistema linux
```
#! /bin/bash

echo "Listando conexão ativas: "
netstat

```


### autenticacao.sh

o arquivo `autenticação` depende de um outro arquivo tipo `log.txt` ou qual quer outro arquivo para analisar uma palavra especifica dentro do arquivo como `Failed password`
```
#! /bin/bash

echo "Procurando por tentativas de login que falharam
grep "Failed password" log.txt

```


### atualizacao.sh

atualizando os pacotes e relises do sistema
```
#! /bin/bash

echo "Verificando atualizações disoniveis: "
apt-get update
apt-get upgrade -s | grep "upgraded, "
```


### vulnerabilidade.sh

```
#! /bin/bash

site="https://www.google.com"
vulnerabilidade="CVE-2014-6271"
echo
resultado=$(curl -s -I "$site" | grep "$vulnerabilidade")

if [ -n "$resultado" ]; then
  echo "Vulnerabilidade detectada: "
else
  echo "Site seguro: "
fi
```

---

#### Script.txt

```
#! /bin/bash

echo "Criando um diretorio e copiando um arquivo ..."

mkdir Qualquer_novo
cp arquivo.txt Qualquer_novo
echo "Diretorio criado e arquivo copiado!" 

```

### renomeando.txt
```
#! /bin/bash

echo "Listando conteudo e diretorio e renomenadno um arquivo "
ls novo_diretorio
mv arquivo.txt novo_arquivo.txt
echo "Arquivo renomeado"
```




