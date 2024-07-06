# Subnetting

A divisão de um intervalo de endereços IPv4 em vários intervalos menores é chamada de subnetting. Uma sub-rede é um segmento lógico de uma rede que usa endereços IP com o mesmo endereço de rede.

## Subnetting de um Endereço IPv4 e Máscara de Sub-rede

Vamos usar o seguinte endereço IPv4 e máscara de sub-rede como exemplo:

- **Endereço IPv4:** 192.168.12.160
- **Máscara de Sub-rede:** 255.255.255.192
- **CIDR:** 192.168.12.160/26

### Partes do Endereço IPv4

**Parte de Rede:**

| Detalhes    | 1º Octeto  | 2º Octeto  | 3º Octeto  | 4º Octeto  | Decimal              |
|-------------|------------|------------|------------|------------|----------------------|
| IPv4        | 1100 0000  | 1010 1000  | 0000 1100  | 1010 0000  | 192.168.12.160/26    |
| Máscara     | 1111 1111  | 1111 1111  | 1111 1111  | 1100 0000  | 255.255.255.192      |
| Bits        | /8         | /16        | /24        | /32        |                      |

**Parte do Host:**

| Detalhes    | 1º Octeto  | 2º Octeto  | 3º Octeto  | 4º Octeto  | Decimal              |
|-------------|------------|------------|------------|------------|----------------------|
| IPv4        | 1100 0000  | 1010 1000  | 0000 1100  | 1010 0000  | 192.168.12.160/26    |
| Máscara     | 1111 1111  | 1111 1111  | 1111 1111  | 1100 0000  | 255.255.255.192      |
| Bits        | /8         | /16        | /24        | /32        |                      |

### Endereço de Rede e Broadcast

**Endereço de Rede:** Define o início da sub-rede, com todos os bits do host configurados como 0.

| Detalhes    | 1º Octeto  | 2º Octeto  | 3º Octeto  | 4º Octeto  | Decimal              |
|-------------|------------|------------|------------|------------|----------------------|
| IPv4        | 1100 0000  | 1010 1000  | 0000 1100  | 10|00 0000 | 192.168.12.128/26    |
| Máscara     | 1111 1111  | 1111 1111  | 1111 1111  | 11|00 0000 | 255.255.255.192      |
| Bits        | /8         | /16        | /24        | /32        |                      |

**Endereço de Broadcast:** Define o final da sub-rede, com todos os bits do host configurados como 1.

| Detalhes    | 1º Octeto  | 2º Octeto  | 3º Octeto  | 4º Octeto  | Decimal              |
|-------------|------------|------------|------------|------------|----------------------|
| IPv4        | 1100 0000  | 1010 1000  | 0000 1100  | 10|11 1111 | 192.168.12.191/26    |
| Máscara     | 1111 1111  | 1111 1111  | 1111 1111  | 11|00 0000 | 255.255.255.192      |
| Bits        | /8         | /16        | /24        | /32        |                      |

### Intervalo de Hosts

Dentro de uma sub-rede, os endereços de host variam entre o endereço de rede e o de broadcast. Para a sub-rede 192.168.12.128/26:

| Detalhes         | Endereço IPv4            |
|------------------|--------------------------|
| Endereço de Rede | 192.168.12.128           |
| Primeiro Host    | 192.168.12.129           |
| Último Host      | 192.168.12.190           |
| Endereço de Broadcast | 192.168.12.191       |
| Total de Hosts   | 62                       |

## Subnetting em Redes Menores

Vamos dividir a sub-rede 192.168.12.128/26 em 4 sub-redes menores:

### Subnetting em 4 Sub-redes

- **Sub-rede Inicial:** 192.168.12.128/26
- **Sub-redes Requeridas:** 4
- **Nova Máscara de Sub-rede:** /28 (255.255.255.240)

Cada sub-rede terá 16 endereços:

| Sub-rede | Endereço de Rede  | Primeiro Host   | Último Host    | Endereço de Broadcast | CIDR             |
|----------|-------------------|-----------------|----------------|-----------------------|------------------|
| 1        | 192.168.12.128    | 192.168.12.129  | 192.168.12.142 | 192.168.12.143        | 192.168.12.128/28|
| 2        | 192.168.12.144    | 192.168.12.145  | 192.168.12.158 | 192.168.12.159        | 192.168.12.144/28|
| 3        | 192.168.12.160    | 192.168.12.161  | 192.168.12.174 | 192.168.12.175        | 192.168.12.160/28|
| 4        | 192.168.12.176    | 192.168.12.177  | 192.168.12.190 | 192.168.12.191        | 192.168.12.176/28|

## Subnetting Mental

Subnetting envolve muita matemática, mas com prática, pode se tornar um cálculo instantâneo. Identifique o octeto que muda e use a operação de módulo para determinar o tamanho da sub-rede.

### Exemplo

Para o endereço de rede 192.168.1.1/25:

- **Octeto que Muda:** Quarto octeto.
- **Operação Módulo:** 25 % 8 = 1.
- **Tamanho da Sub-rede:** 2^(8-1) = 128.
- **Intervalo de IPs:** 192.168.1.0-127 (rede), 192.168.1.1-126 (utilizável), 192.168.1.128-255 (broadcast).

### Tabela de Exponentes

| Resto | Número | Forma Exponencial | Forma de Divisão |
|-------|--------|-------------------|------------------|
| 0     | 256    | 2^8               | 256              |
| 1     | 128    | 2^7               | 256/2            |
| 2     | 64     | 2^6               | 256/2/2          |
| 3     | 32     | 2^5               | 256/2/2/2        |
| 4     | 16     | 2^4               | 256/2/2/2/2      |
| 5     | 8      | 2^3               | 256/2/2/2/2/2    |
| 6     | 4      | 2^2               | 256/2/2/2/2/2/2  |
| 7     | 2      | 2^1               | 256/2/2/2/2/2/2/2|

Lembre-se dos poderes de dois até oito para cálculos rápidos.

### Exemplo de Intervalo de IP

Para a sub-rede /25 com 128 endereços IP:

- **Primeiro Intervalo:** 192.168.1.0-127 (0 é rede, 127 é broadcast).
- **Usável:** 192.168.1.1-126.

Se o IP estiver acima de 128:

- **Segundo Intervalo:** 192.168.1.128-255 (128 é rede, 255 é broadcast).
- **Usável:** 192.168.1.129-254.


