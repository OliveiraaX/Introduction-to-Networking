# Endereços MAC e ARP

## Endereços MAC

Cada host em uma rede possui seu próprio endereço MAC de 48 bits (6 octetos), representado em formato hexadecimal. O endereço MAC é único para cada interface de rede física (como placas Ethernet, Bluetooth ou WLAN) e é atribuído pelo fabricante.

Exemplo de um endereço MAC: `DE:AD:BE:EF:13:37`.

### Estrutura do Endereço MAC

Um endereço MAC é dividido em duas partes:
- **OUI (Organization Unique Identifier)**: Os primeiros 3 octetos que identificam o fabricante.
- **Parte de Endereço Individual**: Os últimos 3 octetos que identificam o dispositivo específico.

### Tipos de Endereços MAC

Existem vários padrões de endereço MAC, incluindo Ethernet (IEEE 802.3), Bluetooth (IEEE 802.15) e WLAN (IEEE 802.11).

### Funções do Endereço MAC

- Facilita a entrega de pacotes na camada 2 (Ethernet), identificando fisicamente cada dispositivo na rede.
- Usado no protocolo ARP para resolver endereços IP em endereços MAC.

## ARP (Address Resolution Protocol)

O ARP é um protocolo usado para **resolver endereços IP em endereços MAC em redes locais** (LANs). Ele permite que dispositivos se comuniquem usando endereços MAC em vez de endereços IP.

### Funcionamento do ARP

1. **ARP Request**: Um dispositivo envia uma solicitação ARP para descobrir o endereço MAC de outro dispositivo na mesma rede.
2. **ARP Reply**: O dispositivo com o endereço IP correspondente responde com seu endereço MAC.

### Vulnerabilidades e Segurança

ARP é vulnerável a ataques como ARP Spoofing, que pode ser usado para interceptar ou manipular tráfego na rede.

### ARP Spoofing
Também conhecido como envenenamento de cache ARP, ARP Spoofing envolve o envio de mensagens ARP falsificadas em uma LAN. O objetivo é associar o endereço MAC do atacante com o endereço IP de um dispositivo legítimo, permitindo a interceptação do tráfego destinado ao dispositivo legítimo.

### Exemplo de ARP Spoofing
```
1   0.000000 10.129.12.100 -> 10.129.12.101 ARP 60  10.129.12.100 is at AA:AA:AA:AA:AA:AA
2   0.000015 10.129.12.100 -> 10.129.12.255 ARP 60  Who has 10.129.12.101?  Tell 10.129.12.100
3   0.000030 10.129.12.101 -> 10.129.12.100 ARP 60  10.129.12.101 is at BB:BB:BB:BB:BB:BB
4   0.000045 10.129.12.100 -> 10.129.12.101 ARP 60  10.129.12.100 is at AA:AA:AA:AA:AA:
```
As linhas 1 e 4 mostram o atacante (10.129.12.100) enviando mensagens ARP falsificadas para o alvo, associando seu endereço MAC ao endereço IP do alvo (10.129.12.101). As linhas 2 e 3 mostram o alvo enviando uma solicitação ARP e respondendo ao endereço MAC do atacante. Isso indica que o cache ARP do alvo foi envenenado e que todo o tráfego destinado ao alvo será enviado para o endereço MAC do atacante.

### Medidas de Proteção
Para se proteger contra o ARP Spoofing, é importante usar protocolos de rede seguros, como IPSec ou SSL, e implementar medidas de segurança, como firewalls e sistemas de detecção de intrusão.

