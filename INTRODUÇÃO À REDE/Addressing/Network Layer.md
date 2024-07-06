# Camada de Rede (Layer 3)

## Introdução

A camada de rede (Layer 3) do modelo OSI controla a troca de pacotes de dados, já que estes não podem ser roteados diretamente ao receptor e, portanto, precisam ser encaminhados por nós de roteamento. Os pacotes de dados são transferidos de nó em nó até alcançarem seu destino. A camada de rede identifica os nós da rede, configura e libera canais de conexão, e cuida do roteamento e controle de fluxo de dados.

## Funções Principais

- **Endereçamento Lógico (Logical Addressing):** Identificação dos nós individuais da rede.
- **Roteamento (Routing):** Encaminhamento dos pacotes de dados através da rede, de nó em nó, até o destino final.

## Protocolos na Camada de Rede

Os protocolos são conjuntos de regras para comunicação na respectiva camada e são transparentes para os protocolos das camadas superiores ou inferiores. Alguns protocolos cumprem funções de várias camadas e se estendem por duas ou mais camadas. Os protocolos mais utilizados nesta camada são:

- **IPv4 / IPv6:** Protocolo de Internet versão 4 e 6, respectivamente.
- **IPsec:** Protocolo de segurança para IP.
- **ICMP:** Protocolo de Mensagens de Controle da Internet.
- **IGMP:** Protocolo de Gerenciamento de Grupo na Internet.
- **RIP:** Protocolo de Informação de Roteamento.
- **OSPF:** Primeiro Algoritmo de Caminho Aberto.

## Funcionalidade

A camada de rede garante o roteamento de pacotes da fonte ao destino, dentro ou fora de uma sub-rede. Estas sub-redes podem ter esquemas de endereçamento diferentes ou tipos de endereçamento incompatíveis. Em ambos os casos, a transmissão de dados passa por toda a rede de comunicação e inclui o roteamento entre os nós da rede.

Devido às diferentes sub-redes, a comunicação direta entre o remetente e o receptor nem sempre é possível, então os pacotes devem ser encaminhados por nós (roteadores) no caminho. Os pacotes encaminhados não alcançam as camadas superiores, mas recebem um novo destino intermediário e são enviados ao próximo nó.

