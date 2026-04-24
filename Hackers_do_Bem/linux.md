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

  * **pwd** (print work directory) - imprime caminho
  * **cat** (concatenar) ou imprimie arquivo
  * **sudo** (super user do) - elevação de privilegios
  * **ip a** (ip address) exibe endereços
  * **top / btop** (Gerenciador de tarefas)
  * **df -h**
  * **grep**


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
**Integridade**: Journaling / fsck

## Btrfs - B-Tree File System
**Integridade**: Copia em Gravação (CoW) / auto reparo

## JFS - Journaled File System
**Integridade**: Journaling

## XFS - High Performace Scalable File System
**Integridade** Journaling

## ReiserFS - Desuso
**Integridade**: Journaling / fsck

## ZFS 
**Integridade**: CoW Checksum / auto reparo


