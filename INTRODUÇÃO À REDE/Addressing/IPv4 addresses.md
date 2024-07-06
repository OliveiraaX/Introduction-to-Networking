# Endereços IP

## Introdução

Cada host na rede pode ser identificado pelo chamado endereço Media Access Control (MAC). No entanto, para estabelecer uma conexão com um host remoto em outra rede, o conhecimento do endereço MAC não é suficiente. O endereçamento na Internet é feito via endereço IPv4 e/ou IPv6, que é composto pelo endereço de rede e pelo endereço do host.

### Comparação de Endereços

- **IPv4 / IPv6:** Descreve o endereço postal único e o distrito do edifício do receptor.
- **MAC:** Descreve o andar exato e o apartamento do receptor.

## Estrutura do IPv4

O método mais comum de atribuição de endereços IP é o IPv4, que consiste em um número binário de 32 bits combinado em 4 bytes, consistindo em grupos de 8 bits (octetos) variando de 0-255. Estes são convertidos em números decimais mais legíveis, separados por pontos e representados como notação decimal pontuada.

### Exemplo de Notação

- **Binário:** 0111 1111.0000 0000.0000 0000.0000 0001
- **Decimal:** 127.0.0.1

Cada interface de rede (placas de rede, impressoras de rede ou roteadores) é atribuída a um endereço IP único.

### Estrutura de Classe IPv4

No passado, os blocos de rede IP foram divididos em classes A - E. As diferentes classes se diferenciam nos respectivos comprimentos das partes de host e de rede.

| Classe | Endereço de Rede | Primeiro Endereço | Último Endereço      | Máscara de Sub-rede | CIDR | Sub-redes | IPs            |
|--------|------------------|-------------------|----------------------|---------------------|------|-----------|----------------|
| A      | 1.0.0.0          | 1.0.0.1           | 127.255.255.255      | 255.0.0.0           | /8   | 127       | 16,777,214 + 2 |
| B      | 128.0.0.0        | 128.0.0.1         | 191.255.255.255      | 255.255.0.0         | /16  | 16,384    | 65,534 + 2     |
| C      | 192.0.0.0        | 192.0.0.1         | 223.255.255.255      | 255.255.255.0       | /24  | 2,097,152 | 254 + 2        |
| D      | 224.0.0.0        | 224.0.0.1         | 239.255.255.255      | Multicast           | Multicast | Multicast | Multicast |
| E      | 240.0.0.0        | 240.0.0.1         | 255.255.255.255      | reservado           | reservado | reservado | reservado |

## Máscara de Sub-rede

A separação adicional dessas classes em redes menores é feita com a ajuda do subnetting. Essa separação é feita usando as máscaras de rede, que têm o mesmo comprimento de um endereço IPv4. Assim como nas classes, descreve quais posições de bits dentro do endereço IP atuam como parte de rede ou parte de host.

### Exemplos de Máscaras de Sub-rede

| Classe | Endereço de Rede | Primeiro Endereço | Último Endereço      | Máscara de Sub-rede | CIDR | Sub-redes | IPs            |
|--------|------------------|-------------------|----------------------|---------------------|------|-----------|----------------|
| A      | 1.0.0.0          | 1.0.0.1           | 127.255.255.255      | 255.0.0.0           | /8   | 127       | 16,777,214 + 2 |
| B      | 128.0.0.0        | 128.0.0.1         | 191.255.255.255      | 255.255.0.0         | /16  | 16,384    | 65,534 + 2     |
| C      | 192.0.0.0        | 192.0.0.1         | 223.255.255.255      | 255.255.255.0       | /24  | 2,097,152 | 254 + 2        |
| D      | 224.0.0.0        | 224.0.0.1         | 239.255.255.255      | Multicast           | Multicast | Multicast | Multicast |
| E      | 240.0.0.0        | 240.0.0.1         | 255.255.255.255      | reservado           | reservado | reservado | reservado |

## Endereços de Rede e Gateway

Os dois IPs adicionais na coluna de IPs são reservados para o chamado endereço de rede e o endereço de broadcast. Outro papel importante é desempenhado pelo gateway padrão, que é o nome do endereço IPv4 do roteador que conecta redes e sistemas com diferentes protocolos e gerencia endereços e métodos de transmissão.

### Exemplo de Endereços de Rede e Gateway

| Classe | Endereço de Rede | Primeiro Endereço | Último Endereço      | Máscara de Sub-rede | CIDR | Sub-redes | IPs            |
|--------|------------------|-------------------|----------------------|---------------------|------|-----------|----------------|
| A      | 1.0.0.0          | 1.0.0.1           | 127.255.255.255      | 255.0.0.0           | /8   | 127       | 16,777,214 + 2 |
| B      | 128.0.0.0        | 128.0.0.1         | 191.255.255.255      | 255.255.0.0         | /16  | 16,384    | 65,534 + 2     |
| C      | 192.0.0.0        | 192.0.0.1         | 223.255.255.255      | 255.255.255.0       | /24  | 2,097,152 | 254 + 2        |
| D      | 224.0.0.0        | 224.0.0.1         | 239.255.255.255      | Multicast           | Multicast | Multicast | Multicast |
| E      | 240.0.0.0        | 240.0.0.1         | 255.255.255.255      | reservado           | reservado | reservado | reservado |

## Endereço de Broadcast

O endereço de broadcast conecta todos os dispositivos em uma rede entre si. O broadcast em uma rede é uma mensagem que é transmitida a todos os participantes de uma rede e não requer resposta. Em redes IPv4, o endereço de broadcast é o último endereço IPv4 utilizável em uma sub-rede.

### Exemplo de Endereço de Broadcast

| Classe | Endereço de Rede | Primeiro Endereço | Último Endereço      | Máscara de Sub-rede | CIDR | Sub-redes | IPs            |
|--------|------------------|-------------------|----------------------|---------------------|------|-----------|----------------|
| A      | 1.0.0.0          | 1.0.0.1           | 127.255.255.255      | 255.0.0.0           | /8   | 127       | 16,777,214 + 2 |
| B      | 128.0.0.0        | 128.0.0.1         | 191.255.255.255      | 255.255.0.0         | /16  | 16,384    | 65,534 + 2     |
| C      | 192.0.0.0        | 192.0.0.1         | 223.255.255.255      | 255.255.255.0       | /24  | 2,097,152 | 254 + 2        |
| D      | 224.0.0.0        | 224.0.0.1         | 239.255.255.255      | Multicast           | Multicast | Multicast | Multicast |
| E      | 240.0.0.0        | 240.0.0.1         | 255.255.255.255      | reservado           | reservado | reservado | reservado |

## Sistema Binário

O sistema binário é um sistema de numeração que usa apenas dois estados diferentes, representados por dois números (0 e 1) em oposição ao sistema decimal (0 a 9).

Um endereço IPv4 é dividido em 4 octetos, cada um composto por 8 bits. Cada posição de um bit em um octeto tem um valor decimal específico.

### Exemplo de Conversão Binária para Decimal

Endereço IPv4: 192.168.10.39

1º Octeto - Valor: 192

- Valores: 128 64 32 16 8 4 2 1
- Binário: 1 1 0 0 0 0 0 0

### Soma dos Valores de Cada Octeto

| Octeto | Valores                      | Soma |
|--------|------------------------------|------|
| 1º     | 128 + 64 + 0 + 0 + 0 + 0 + 0 + 0 | 192  |
| 2º     | 128 + 0 + 32 + 0 + 8 + 0 + 0 + 0 | 168  |
| 3º     | 0 + 0 + 0 + 0 + 8 + 0 + 2 + 0    | 10   |
| 4º     | 0 + 0 + 32 + 0 + 0 + 4 + 2 + 1   | 39   |

A representação completa de binário para decimal seria:

- **Binário:** 1100 0000 . 1010 1000 . 0000 1010 . 0010 0111
- **Decimal:** 192 . 168 . 10 . 39

### Máscara de Sub-rede (255.255.255.0)

A máscara de sub-rede é calculada da mesma forma.

- **Binário:** 1111 1111 . 1111 1111 . 1111 1111 . 0000 0000
- **Decimal:** 255 . 255 . 255 . 0

## CIDR (Classless Inter-Domain Routing)

CIDR é um método de representação que substitui a atribuição fixa entre endereço IPv4 e classes de rede (A, B, C, D, E). A divisão é baseada na máscara de sub-rede ou no sufixo CIDR, que permite a divisão bit a bit do espaço de endereços IPv4 e, portanto, em sub-redes de qualquer tamanho. O sufixo CIDR indica quantos bits desde o início do endereço IPv4 pertencem à rede.

### Exemplo de CIDR

Endereço IPv4: 192.168.10.39
Máscara de sub-rede: 255.255.255.0
CIDR: 192.168.10.39/24

O sufixo CIDR é a soma de todos os bits 1 na máscara de sub-rede.

- **Binário:** 1111 1111 . 1111 1111 . 1111 1111 . 0000 0000 (/24)
- **Decimal:** 255 . 255 . 255 . 0
