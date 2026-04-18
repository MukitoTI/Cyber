# Criando Usuarios
É muito comum no ambiente de trabalho ou no doméstico que o mesmo dispositivo seja compartilhado com duas ou mais pessoas os mesmo tempo. 
Se por um lado esse compartilhamento possa gerar uma economia financeira, por outro, esse procedimento pode deixar brechas na segurança dos indivíduos e no sistema operacional de uma empresa. 
Nesse sentido, o Windows apresenta a possibilidade da criação de usuários diferentes dentro do sistema. Vamos entender como isso funciona? 
<br>
## Usuários

A criação de usuários no Windows é um aspecto fundamental para a segurança, organização e personalização de um sistema operacional. 
Essa prática desempenha um papel crucial em ambientes pessoais, corporativos e educacionais, oferecendo uma série de benefícios importantes. 

### Segurança
A criação de usuários individuais permite que cada pessoa que utilize o computador tenha sua própria conta. Isso é essencial para manter a privacidade e a segurança dos dados.

### Controle de Acesso
Através da criação de usuários, é possível controlar quem tem acesso ao computador e aos recursos compartilhados.

### Personalização
Cada usuário pode personalizar sua própria área de trabalho, configurações de sistema e preferências.


# Criando Usuarios
1. Gerenciamento do computador
2. Configurações
    * Grupo Familia
3. Win + R
    * "control userpasswords2"
4. Modo Texto (CMD - Adm)
   * "net user meuamigo /add"

**Consulta usuarios**
```
net user
```

# Criando Grupos
1. Gerenciamento do computador
2. Modo Texto (CMD - Adm)
   * "net localgrupo grupo-leitura /add"
   * **Adiciona user no grupo** "net localgrupo grupo-leitura meuamigo /add"

**Consulta usuarios no grupo**
```
net localgrupo grupo-leitura
```

## Gerenciamento de grupos e permissões

Para continuar com a configuração da criação de usuários do Windows, outro passo importante é a criação das permissões do sistema operacional Windows. 
Esta etapa é muito importante para o gerenciamento de segurança e acesso a recursos, como arquivos, pastas, impressoras e compartilhamentos de rede. 

Confira na lista abaixo alguns pontos essenciais sobre as permissões do Windows. 
  * **Camadas de Proteção**: O sistema de permissões do Windows opera em várias camadas, oferecendo um nível de granularidade impressionante.
  * **Grupos de Usuários**: Para simplificar a atribuição de permissões, o Windows permite que os usuários sejam agrupados em conjuntos chamados "grupos".
  * **Backup e Recuperação**: Permissões bem gerenciadas ajudam a proteger dados importantes de exclusões acidentais ou maliciosas.


### Compartilhamento em Rede
Uma ferramenta do Windows muito vantajosa para as empresas é o compartilhamento de rede. 
Essa funcionalidade permite a troca de informações e recursos entre computadores em uma rede local, melhorando a colaboração, a acessibilidade e a eficiência de diversas maneiras. 

O compartilhamento de rede também pode trazer outros benefícios aos usuários, como o acesso remoto aos arquivos, a centralização de recursos e armazenamento de dados 
em um só ambiente e a segurança no controle de acesso dos usuários.
