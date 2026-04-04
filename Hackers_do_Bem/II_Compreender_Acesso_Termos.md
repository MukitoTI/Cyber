# TEORIA

### OSPF
O OSPF (Open Shortest Path First) é um protocolo de roteamento dinâmico de estado de enlace (link-state) amplamente utilizado em redes IP, 
conhecido por sua rápida convergência, escalabilidade e padrão aberto. Ele usa o algoritmo de Dijkstra (SPF) para encontrar o caminho mais curto, ideal para redes corporativas complexas e médias/grandes.

### O Algoritmo de Dijkstra
O algoritmo de Dijkstra (Shortest Path First - SPF) encontra o caminho de menor custo entre um nó de origem e todos os outros vértices em um grafo com pesos não negativos. 
Ele utiliza uma estratégia gulosa, selecionando o nó mais próximo não visitado e relaxando suas arestas vizinhas, garantindo a rota mais curta.

**Conceitos Principais:**
  * **Grafo Ponderado**: As arestas possuem custos (pesos).
  * **Pesos Não Negativos**: Essencial; não funciona com pesos negativos.
  * **Fila de Prioridade**: Frequentemente usada para selecionar o próximo nó com a menor distância atual.
  * **Aplicação**: Base para protocolos de roteamento de redes (OSPF) e GPS.

**Passo a Passo do Algoritmo:**
  1. **Inicialização**: Defina a distância até o nó de origem como 0 e todos os outros nós como infinito. Crie um conjunto de nós não visitados.
  2. **Seleção**: Escolha o nó **u* não visitado com a menor distância atual.
  3. **Relaxação**: Para o nó **u*, verifique todos os seus vizinhos **v*. Se a distância até **u* + custo para **v* for menor que a distância atual para **v*, atualize o custo de **v*.
  4. **Marcação**: Marque o nó **u* como visitado. Um nó visitado não será verificado novamente.
  5. **Repetição**: Repita os passos 2 a 4 até que todos os nós tenham sido visitados.

**Exemplo Prático (Resumo):**
  * **Rede**: Imagine cidades (nós) conectadas por estradas com distâncias (pesos).
  * **Objetivo**: Achar a rota mais curta da cidade A para todas as outras.
  * **Resultado**: O algoritmo gera uma árvore de caminhos mínimos (SPF Tree), indicando o melhor caminho.
**O algoritmo é amplamente utilizado devido à sua eficiência em encontrar o menor caminho, sendo fundamental em sistemas de navegação e redes de computadores.*

## Divisão de Classes IPv4
Abaixo estão os intervalos padrão para cada classe:
  * **Classe A**: 1 a 126 (Máscara padrão: 255.0.0.0)
  * **Classe B**: 128 a 191 (Máscara padrão: 255.255.0.0)
  * **Classe C**: 192 a 223 (Máscara padrão: 255.255.255.0)
  * **Classe D**: 224 a 239 (Reservada para Multicast)
  * **Classe E**: 240 a 255 (Reservada para pesquisa/experimental)

### Observações Importantes:
  1. **Endereço Privado**: Além de ser Classe C, o IP 192.168.5.78 está dentro da faixa de **IPs privados** (`192.168.0.0` a `192.168.255.255`). Isso significa que ele é usado em redes locais (como em casas ou empresas) e não é roteável diretamente na internet.
  2. **A Classe "Morreu" (CIDR)**: Embora ainda seja um conceito fundamental em provas e certificações, na prática moderna utilizamos o **CIDR** ***(Classless Inter-Domain Routing)***. No CIDR, a máscara de rede define o tamanho da rede, independentemente da classe original do IP. No caso de uma rede doméstica comum, esse IP usaria a máscara `/24`.


