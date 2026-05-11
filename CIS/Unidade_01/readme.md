## 🎯 Objetivo de aprendizagem

Você ser capaz de reconhecer os principais conceitos e técnicas para o monitoramento e defesa da rede de computadores da sua organização, 
referente ao Controle 13 do CIS Controls.

### Por que é importante monitorar e defender a rede?

*"Não podemos confiar que as defesas da rede sejam perfeitas. Os adversários continuam a evoluir e amadurecer, 
à medida que compartilham ou vendem informações entre sua comunidade sobre exploits e desvios para controles de segurança. 
Mesmo que as ferramentas de segurança funcionem ‘conforme anunciado’, é necessário um entendimento da postura de risco 
corporativo para configurá-las, ajustá-las e registrá-las em log para serem eficazes."* - CIS (2021).


Agentes maliciosos podem perpetrar ataques que comprometam ativos da sua rede de computadores, permanecendo infiltrados durante dias, 
semanas ou até mesmo meses sem serem detectados, monitorando, por exemplo, o tráfego da rede, coletando as credenciais em uso e/ou 
acessando e exfiltrando dados. 
O CIS cita a importância de uma consciência situacional abrangente no processo de prevenção, detecção e resposta às ameaças cibernéticas.  

De forma geral, grande parte das nossas atividades e comportamentos diários são padronizados e previsíveis. 
Observar e mapear esses padrões de comportamento de modo a estabelecer linhas de base torna mais óbvio identificar alterações ou anomalias, 
fazendo com que a aplicação dos tratamentos para possíveis ameaças seja muito mais rápida. Mas, para tal, é necessário que se tenha uma compreensão 
abrangente do ambiente operacional, por meio do monitoramento e aprimoramento da conscientização situacional dos profissionais.

Para demonstrar a importância do conhecimento, das competências e habilidades necessárias para tratar o tema, 
o National Institute of Standards and Technology (NIST), por meio da Iniciativa Nacional para Educação em Cibersegurança 
(National Initiative for Cybersecurity Education - NICE), sinalizou em seu framework que é necessário ter em mente que a monitoração da rede é essencial 
para buscar ativamente remediar atividades não autorizadas. Adicionalmente, também incluiu nesse documento a função 
“T0166 Executar a correlação de eventos usando informações coletadas de uma variedade de fontes dentro da empresa para obter consciência situacional 
e determinar a eficácia de um ataque observado” (NIST, 2017). 

```
Para visualizar a lista de todas as tarefas que foram identificadas pelo NIST como parte de uma função de trabalho de segurança cibernética,
acesse o documento NIST Special Publication 800-181, clicando neste link(opens in a new tab). NIST 2017
```
---

`https://www.nist.gov/itl/applied-cybersecurity/nice/nice-framework-resource-center/nice-framework-current-versions`


### Quais os procedimentos gerais e técnicas a monitoração e defesa da rede devem compreender?

Quanto mais equipamentos conectados na infraestrutura de rede, mais dados são trafegados, mais suscetível essa rede está a vulnerabilidades e ameaças, e mais compreensão e visibilidade são necessários para incrementar a sua segurança. Ainda, para deixar ainda mais complexo esse contexto, não há mais uma fronteira tão clara e bem definida dos limites dos recursos da infraestrutura de rede de uma organização, podendo os seus dados críticos estarem dispersos em uma infraestrutura de rede interna e/ou em serviços ou nuvens públicas e/ou em dispositivos pessoais conectados remotamente.

Nesse sentido, um conceito chamado de consciência situacional de segurança de rede (em inglês, Network Security Situational Awareness) está sendo bastante aplicado no tema segurança da infraestrutura de rede.


É fato que as ferramentas não substituem pessoal qualificado em segurança da informação e administradores de sistema. Mesmo com ferramentas automatizadas de análise e correlação de logs, a experiência humana e sua intuição são frequentemente necessárias para ajudar a identificar e compreender os ataques cibernéticos. Uma equipe treinada e organizada está no centro desse processo e é responsável pela identificação, parametrização e implementação das medidas de segurança mais adequadas para a proteção necessária, assim como pela definição das fontes de dados que serão coletadas; afinal, espaços e processamentos são limitados.

Além disso, sem um monitoramento contínuo que permita que as equipes recebam os alertas e respondam rapidamente aos incidentes cibernéticos, essas ferramentas perdem a eficácia.

Muitos são os fatores que podem prejudicar a evolução de um modelo tradicional de monitoramento e defesa da rede para uma abordagem de consciência situacional de segurança de rede, sendo alguns deles:

  * Ausência de monitoração em tempo real dos ativos corporativos e de software.
  * Segurança baseada em assinaturas e ataques conhecidos, não identificando as ameaças persistentes e avançados (APT).
  * Equipes de segurança multifuncionais, enxutas e dependentes de atividades predominantemente manuais.
  * Análise de vulnerabilidades em sistemas operacionais e aplicações, negligenciando as possíveis falhas de segurança relacionadas aos dispositivos de rede.

Essa necessidade também é sinalizada pela ABNT NBR ISSO/IEC 27002:2022 (ABNT, 2022), orientando que sejam implementados os controles que possam assegurar a segurança das informações nas redes e para proteger os serviços conectados de acesso não autorizado.

Na prática, quando apropriado e suportado, a detecção e análise inicial dessas atividades devem ser realizadas por meio de sistemas de detecção de intrusos, conhecidos como IDS (Intrusion Detection System).  Um IDS é passivo e não altera o fluxo dos dados trafegados na infraestrutura de rede. Seu objetivo é “escutar”, detectar e alertar e, caso necessário, poderá também enviar os eventos para plataformas centralizadas de armazenamento, correlação e geração de eventos.

Tais plataformas centralizadas de armazenamento, correlação e geração de eventos são atualmente batizadas pelo mercado como sendo plataformas de SIEM (Security Information and Event Management). 


# SIEM

Coleta dados de log de eventos de várias fontes, identifica atividades que se desviam da norma com análise em tempo real e toma as medidas apropriadas. Veja na figura como funciona esse processo.

<img width="755" height="448" alt="image" src="https://github.com/user-attachments/assets/1430bc0c-3ad2-4e09-a9b3-8ca4a5045d03" />


# IDS

É por padrão, classificado de acordo com o local onde a detecção deverá ser realizada. Exemplificando: um IDS pode ser instalado diretamente em uma estação de trabalho ou um servidor de rede, coletando e analisando atividades pontuais realizadas nestes equipamentos; ou em um segmento específico de rede, coletando e analisando o fluxo de quaisquer dados que trafegam através deste segmento. Esses modelos são conhecidos como HIDS (Host-based intrusion detection system) e NIDS (Network-based intrusion detection system), respectivamente. Ambos têm suas vantagens, desvantagens, complexidades e custos diferenciados, e a escolha dependerá do contexto de cada organização.


<img width="757" height="476" alt="image" src="https://github.com/user-attachments/assets/1708369b-c5a8-4010-b5be-efc539d19103" />


Um IDS pode ser baseado em assinaturas ou em anomalias. Clique em cada um para compreender.

### Assinatura
Compara o tráfego de dados analisado com um banco de dados de ataques e atividades maliciosas já conhecidas. Se houver uma correspondência próxima, o IDS identifica e alerta sobre a possível intrusão.

### Anomalias
Monitora o tráfego em busca de desvios do comportamento normal. Ele estabelece um perfil do tráfego típico e alerta se detectar atividades que estão fora desse padrão. Pode utilizar, por exemplo, tecnologias de inteligência artificial e/ou aprendizado de máquina para identificação desses comportamentos anômalos.


Além disso, pela quantidade de dados coletados pelos sistemas de detecção, não é raro que os profissionais de segurança sejam inundados com uma grande variedade de alertas, válidos ou não. Portanto, é preciso bastante atenção nas parametrizações dos limites (thresholds) dos eventos para que os disparos dos alertas sejam realizados somente quando esses limites forem excedidos.

