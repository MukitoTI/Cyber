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



