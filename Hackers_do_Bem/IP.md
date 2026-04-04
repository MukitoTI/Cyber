# IP

Para acesso a internet precisamos de:

1. Acesso a rede mundial (Física)
2. Endereço de rede (Lógica)


Rede Locais Domésticas:
  * Computadores:
  * Câmeras de monitoramentos;
  * Dispositivos móveis;
  * "Coisas" (Internet das Coisas - IoT)


Redes Locais corporativas:
  * Computadores;
  * Servidores;
  * Cameras de Monitoramento;
  * Dispositivos móveis;
  * "Coisas" (IoT)


**LANs** = Endereços privados
**WANs** = Emdereços públicos

**Privados / Local / Internos**
  - 192.168.1.1

**Públicos / Externos**
  - 82.129.80.111

Documentação RFCs
`https://www.ietf.org/process/rfcs/`

**Request for Comments** <br>
RFC 1918 - IPs Privados <br>
RFC 2460 - IPv6 <br>
RFC 2131 - DHCP <br>
RFC 1945 - HTTP <br>
RFC 1321 - MD5 <br>
RFC 4251 - SSH <br>

----------------------------------------------------------

**Private Address Space**<br>
 * 10.0.0.0      -  10.255.255.255 (10/8 prefix) <br>
 * 172.16.0.0    -  172.31.255.255 (172.16/12 prefix) <br>
 * 192.168.0.0   -  192.165.255.255 (192.168/16 prefix) <br>


<img width="1280" height="502" alt="image" src="https://github.com/user-attachments/assets/e6ecba9c-b4bc-487e-a35d-569d96ec8979" />

<br>
<br>

| IP PRIVADO | IP PÚBLICO |
| :--- | :--- |
| LANs | WANs |
| Usado internamente, endereço pode repetir em outras redes locais | Globalmente único |
| Atribuído pelo adm. de rede local | Atribuído pelo provedor de internet (a IANA controla distribuição global) |
| Gratuito | Tem custo |
| Não esgota pois pode ser repetido em outras LANs | Esgotado |
| `10.0.0.0/8`, `172.16.0.0/12`, `192.168.0.0/16` | `1.0.0.0` a `223.255.255.255` |


------------------------------------------------------
REDE
192.168.0.0 <br>
255.255.255.0 <br>
<br>
<br>
00000000 = 8<br>
2⁸ = 256 -2 = 254<br>
<br>
0000000 = 7<br>
2⁷ = 128 -2 = 126<br>
<br>
255.255.255.128<br>


-------------------------------------------------------

Para o prefixo /22, a máscara de rede correta no formato de quatro octetos (decimal pontuado) é 255.255.252.0.

**Como chegar a esse resultado:**
A máscara `/22` indica que os primeiros 22 bits (de um total de 32) estão "ligados" (valor 1). Ao preenchermos os octetos, temos:

 1. **1º Octeto**: 8 bits ligados (11111111) = 255
 2. **2º Octeto**: 8 bits ligados (11111111) = 255
 3. **3º Octeto**: 6 bits ligados (11111100) = 252
 4. **4º Octeto**: 0 bits ligados (00000000) = 0


-------------------------------------------------------
Tabela de Comparação (Formato GitHub)
| Notação CIDR | Máscara Decimal | Total de IPs | Hosts Úteis | 
| :--- | :--- | :--- | :--- | 
| /21 | 255.255.248.0 | 2048 | 2046 | 
| /22 | **255.255.252.0** | 1024 | 1022 | 
| /23 | 255.255.254.0 | 512 | 510 | 
| /24 | 255.255.255.0 | 256 | 254 | 


### Dica para o cálculo rápido:
Como cada octeto vale 256 endereços no total, uma rede `/22` engloba o equivalente a quatro redes `/24` ($256 \times 4 = 1024$ endereços). 
Para achar o valor do terceiro octeto, você também pode subtrair a quantidade de blocos de 256:$256 - 4 = 252$.

# Referencias
TECNOLOGIAS e protocolos de redes. Cisco, [s.d.]. Disponível em: https://www.cisco.com/c/pt_br/tech/index.html Acesso em: set. 2023


