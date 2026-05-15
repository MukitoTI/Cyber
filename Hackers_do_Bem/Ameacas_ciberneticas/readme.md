# CIBER

# Engenharia social 

É a prática de manipular pessoas para obter acesso a informações confidenciais ou realizar ações maliciosas por meio de técnicas psicológicas, como persuasão, intimidação ou falsificação de identidade. A conscientização sobre esses métodos é crucial para evitar ataques e proteger informações sensíveis. 

## Phishing

É uma prática de engenharia social na qual criminosos enviam mensagens falsas, muitas vezes por e-mail, fingindo ser entidades confiáveis para induzir vítimas a compartilhar informações confidenciais. 

## Ataques man-in-the-middle 

Ocorrem quando um adversário intercepta e altera comunicações entre duas partes sem o conhecimento delas, buscando capturar dados sensíveis ou realizar atividades maliciosas. Para isso, o atacante se posiciona entre o remetente e o destinatário, podendo usar técnicas como ARP spoofing ou DNS spoofing. Para se proteger, é essencial utilizar criptografia forte, autenticação de dois fatores e manter softwares atualizados. 

## Ataques de força bruta (Brute Force)

São tentativas automatizadas de descobrir senhas ou chaves criptográficas, testando todas as combinações possíveis. São eficazes contra sistemas com senhas fracas ou previsíveis e podem ser usados para acesso não autorizado a sistemas e contas de usuário. Medidas de segurança incluem senhas fortes, autenticação de dois fatores e limitação de tentativas de login. 

é como tentar abrir um cofre testando todas as combinações possíveis
Exemplo com o dicionario **rockyou.txt** para quebra de um hash MD5.

**$hashcat -m 0 42f749ade7f9e195bf475f37a44cafcb ../wordlists/rockyou.txt**

### Ataques de DDoS (distributed denial of service) 

São uma tentativa maliciosa de sobrecarregar um serviço online, como um site ou uma rede, inundando-o com tráfego artificial de múltiplas fontes, o que resulta na negação de serviço para usuários legítimos, tornando-o inacessível. Geralmente, os ataques DDoS são executados por meio de botnets, que são redes de dispositivos comprometidos e controlados pelo atacante. 

### Ataques de injections

São vulnerabilidades cibernéticas nas quais invasores inserem um código malicioso em sistemas por meio de campos de entrada, como formulários web. Alguns exemplos são a injeção SQL, XSS e a injeção de comandos, permitindo acesso não autorizado a dados, execução de scripts maliciosos e controle do sistema afetado. Prevenir esses ataques exige práticas de segurança robustas, como validação e sanitização de entrada de dados. 

### Prevenindo ataques

* Utilização de HTTPS para conexões seguras
* Implementações de VPNs.
* Verificação cuidadosa



