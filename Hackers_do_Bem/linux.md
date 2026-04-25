# Linux

O Linux é um dos sistemas operacionais de código aberto, ou seja, seu código-fonte está disponível para qualquer pessoa modificar, melhorar e distribuir de acordo com os termos das licenças de software livre. 

Desenvolvido pelo engenheiro de software finlandês Linus Torvalds, no início do anos 1990, os Linux cresceu rapidamente em popularidade devido a facilidade no processo de colaboração no desenvolvimento do sistema operacional. 

### Interfaces
Uma interface gráfica do usuário é conhecida pela sigla "GUI", que vem do termo em inglês graphical user interface. 
Este é um meio de interação entre um usuário e um sistema operacional que utiliza elementos visuais, como ícones, botões, 
janelas e menus, para facilitar a comunicação e a execução de tarefas. 

A interface gráfica do usuário pode ser dividida por elementos visuais (ícones, botões e painéis); 
dispositivos de entrada (mouse, teclado, telas); 
menus e barras de ferramentas; entre outros elementos.  



####  Estrutura de diretórios
Alguns comandos

  * **raiz (/)**: diretório primário no sistema de arquivos do Linux
  * **/boot (inicialização)**: Armazena os arquivos necessários para a inicialização do sistema
  * **/home (pasta do usuário)**: diretório pessoal para cada usuário armazenar seus próprios arquivos e configurações.
  * **/root (usuário root)**: pasta pessoal do usuário root, o superusuário com privilégios administrativos.


  * **bin**  - Diretório bin (binaries, binários) - pasta onde encontrar-se os executáveis utilizados pelos usuários. Ex.: ls, cp, apt.
  * **sbin** - Diretório sbin (system binaries) - pasta onde estão os executáveis de sistema, como: ip, route, fdisk, useradd.
  * **lib** - Diretório lib (Library, biblioteca) - onde encontra-se diversos arquivos como scripts utilizados por vários programas
  * **dev** - Diretório dev (Devices, dispositivos) - diretório onde ficam as representações de arquivos que possibilitam acesso aos dispositivos (HD, memória, seriais)
    * /dev/sda1 - /de

## Comandos Linux Manipulação de Arquivos 
 * **ls** (list - listar)
 * **clear** (limpar)
 * **cd** (change directory - mudar diretório)
 * **mkdir** (make directory - cria diretório)
 * **nano** (editor de texto)
 * **mv** (move - mover ou renomear)
 * **cp** (copy - copiar)
 * **rm** (remove - remover)

<br>

 * **pwd** (print work directory) - imprime caminho
 * **cat** (concatenar) ou imprimie arquivo
 * **sudo** (super user do) - elevação de privilegios
 * **ip a** (ip address) exibe endereços
 * **top / btop** (Gerenciador de tarefas)
 * **df -h**
 * **grep**


# Grupos - Usuarios - Permissões
useradd --help (printa os comandos)

### Usuario
Existem alguns tipos de usuarios
- Sistema
- Humano
  * root (administrador)
  * Usuário Básico 
```
sudo useradd -m "Nome"
```
Cria Senha
```
sudo passwd "Nome"
```
se vc for Adm o sistema vai pedir a senha de ADM

ae depois vc confere se foi adicionado 
```linux
nano /etc/passwd
```
<br>

```linux
sudo nano /etc/shadow
sudo passwd (nome)
Nova senha: 
Redigite a nova senha:

sudo adduser
```
Tambem vimos Grupos
- sudo
- Grupo com nome de usuario
- E nosso grupo 

Comandos para usuarios<br>
Adicione o usuario ao grupo sudo:
```
usermod -a -G sudo "nome"
```
Altere o shell do usuário:
```
chsh -s /bin/bash "nome"
```





# **SO**
Sistemas de Arquivos com funções para atender a demanda de diferentes sistemas!! 

Alguns itens que iremos Avaliar
 * **Integridade**
 * **Criptografia**
 * **Compactação**
 * **Snapshots**
 * **Permissões**
 * **Limites**
 * **Outros recursos**

# File Systems

## EXT4 - Extended File System 4
 * **Integridade**: Journaling / fsck
 * **Criptografia**: Sim
 * **Compactação**: Não
 * **Snapshots**: Não
 * **Permissões**: Sim
 * **Limites**: Arquivo de 16TB / Partição
 * **EB Outros recursos**: Compatibilidade Windows/macOS, cotas em disco,
estabilidade e velocidade

## Btrfs - B-Tree File System
 * **Integridade**: Copia em Gravação (CoW) / auto reparo
 * **Criptografia**: Sim
 * **Compactação**: Sim
 * **Snapshots**: Sim
 * **Permissões**: Sim
 * **Limites**: Arquivo de 16EB / Partição 16EB
 * **Outros recursos**: Redimensionamento de volume, RAID, Backup Incremental,
Desduplicação de dados

## JFS - Journaled File System
 * **Integridade**: Journaling
 * **Criptografia**: Não
 * **Compactação**: Não
 * **Snapshots**: Não
 * **Permissões**: Sim
 * **Limites**: Arquivo de 4 PB / Partição 32 PB

## XFS - High Performace Scalable File System
 * **Integridade** Journaling
 * **Criptografia**: Não
 * **Compactação**: Não
 * **Snapshots**: Não
 * **Permissões**: Sim
 * **Limites**: Arquivo de 8 EB / Partição 16 EB
 * **Outros recursos**: aumentar o tamanho,
cotas, leitura e gravação paralela

## ReiserFS - Desuso
 * **Integridade**: Journaling / fsck
 * **Criptografia**: Não
 * **Compactação**: Não
 * **Snapshots**: Não
 * **Permissões**: Sim
 * **Limites**: Arquivo de 8 TB / Partição 16 TB


## ZFS 
 * **Integridade**: CoW Checksum / autorreparo
 * **Criptografia**: Sim
 * **Compactação**: Sim
 * **Snapshots**: Sim
 * **Permissões**: Sim
 * **Limites**: Arquivo de 16 EB / Partição 256 quadrilhões de zettabyte
 * **Outros recursos**: RAID-Z, Desduplicação de dados
<br>

# Permissões
Tipos
* **Leitura**([R]ead)
  >Consegue **lista e ler** o arquivo/pasta
* **Escrita**([W]rite)
  >Consegue **alterar e apagar** o arquivo/pasta
* **Execução**(e[X]ecute)
  >Consegue **executar e acessar** o arquivo/pasta

<br>

### Permissões pode ser:
 * Usuário Proprietário [user owner] (u)
 * Grupo [group] (g)
 * Outros [others] (o)

### ante
 * (d) Diretório
 * (-) Arquivo
 * (l) link
<br>

<img width="1003" height="519" alt="image" src="https://github.com/user-attachments/assets/50543e17-ae4e-45bc-bb76-6815d170ac5f" />


<br>
<img width="972" height="562" alt="image" src="https://github.com/user-attachments/assets/36962ec3-0550-4e9e-9e9b-6a7d3f79ead0" />
<img width="828" height="464" alt="image" src="https://github.com/user-attachments/assets/ef24e1cd-d20e-4979-9215-12bc4f261aa4" />
<img width="811" height="514" alt="image" src="https://github.com/user-attachments/assets/1264cfed-6c92-4de8-8c95-d9f8793f2594" />
<img width="826" height="488" alt="image" src="https://github.com/user-attachments/assets/ca0753b3-618a-4182-b78a-483aa745722c" />
<img width="792" height="503" alt="image" src="https://github.com/user-attachments/assets/78ad6e92-bd75-431d-80cf-651f23e3d366" />

<br>
<img width="797" height="694" alt="image" src="https://github.com/user-attachments/assets/52157543-6038-46e3-b85d-899f767a1385" />

## Chgrp/chown
<img width="1038" height="220" alt="image" src="https://github.com/user-attachments/assets/ab00eb40-ccee-4f45-a8a1-4db0fdb1643d" />




