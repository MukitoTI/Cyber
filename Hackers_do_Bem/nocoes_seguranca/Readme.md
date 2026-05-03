# Scripts (avancados)


Um script que verifica portas abertas em um sistema e alerta sobre portas não autorizadas ou
suspeitas.

### portas.sh
```
#!/bin/bash

host="127.0.0.1"
portas=("80" "22" "443" "3389")

for porta in "${portas[@]}"; do
  nc -zv "$host" "$porta" > /dev/null 2>&1
  if [ $? -eq 0 ]; then
    echo "Porta $porta está aberta em $host"
  else
    echo "Porta $porta está fechada em $host"
  fi
done
```

**nc** - netcat - ouve as portas <br>
**zv** - verboze
**2>&1** - Tratando o erro


### falhas

#### logs.txt
```
hteste
taetae
koaksoks
am,cnv,mcnv
oiajoijadf asd
aoseijuroaieujroaiseju
aksjdflkajsdflaksdjf
lakjdml,nm,ne

apsio ´poi cv
qpoieujiãçljadsflçajsd çlajdf
Failed Password
pdori tps ipoi
lçskd .lk,m kdslfj
sporui t09puower opiwujr
lsçkj çsldfk gçsldfkg çsdfl
```

### + 1


### vunerabilidade.sh
```
#! /bin/bash

sistema="Ubuntu"
versao="20.04"

vulnerabilidade=$(grep "$sistema $versao" cve_database.txt)

if [ -n "$vulnerabilidade" ]; then
  echo "Vulnerabilidade conhecida encontrada no sistema $sistema $versao."
else
  echo "Nenhuma vulnerabilidade conhecida encontrada."
fi

```


### forense.sh
```
#! /bin/bash

output_dir="/evidencias"
log_file="auth.log"

mkdir -p "$output_dir"
cp "$log_file" "output_dir/syslog.log"
echo "Evidencias coletadas"
```
