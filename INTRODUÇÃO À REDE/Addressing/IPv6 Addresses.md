# Endereços IPv6

IPv6 é o sucessor do IPv4. Em contraste com o IPv4, o endereço IPv6 tem 128 bits de comprimento. O prefixo identifica as partes do host e da rede. A Internet Assigned Numbers Authority (**IANA**) é responsável por atribuir endereços IPv4 e IPv6 e suas respectivas porções de rede. A longo prazo, espera-se que o IPv6 substitua completamente o IPv4, que ainda é predominantemente usado na Internet. No entanto, o IPv4 e o IPv6 podem ser disponibilizados simultaneamente (Dual Stack).

O IPv6 segue consistentemente o princípio de fim a fim e fornece endereços IP publicamente acessíveis para qualquer dispositivo final sem a necessidade de NAT. Consequentemente, uma interface pode ter vários endereços IPv6, e existem endereços IPv6 especiais aos quais várias interfaces são atribuídas.

IPv6 é um protocolo com muitos novos recursos, que também tem muitas outras vantagens sobre o IPv4:

- Espaço de endereço maior
- Autoconfiguração de endereços (SLAAC)
- Vários endereços IPv6 por interface
- Roteamento mais rápido
- Criptografia de ponta a ponta (IPsec)
- Pacotes de dados de até 4 GBytes

| Recursos                  | IPv4       | IPv6       |
|---------------------------|------------|------------|
| Comprimento do bit        | 32-bit     | 128-bit    |
| Camada OSI                | Camada de Rede | Camada de Rede |
| Alcance de endereçamento  | ~ 4.3 bilhões | ~ 340 undecilhões |
| Representação             | Binário    | Hexadecimal|
| Notação de prefixo        | 10.10.10.0/24 | fe80::dd80:b1a9:6687:2d3b/64 |
| Endereçamento dinâmico    | DHCP       | SLAAC / DHCPv6 |
| IPsec                     | Opcional   | Obrigatório |

Existem quatro tipos diferentes de endereços IPv6:

| Tipo      | Descrição                                                                 |
|-----------|---------------------------------------------------------------------------|
| Unicast   | Endereços para uma única interface.                                       |
| Anycast   | Endereços para várias interfaces, onde apenas uma delas recebe o pacote.  |
| Multicast | Endereços para várias interfaces, onde todas recebem o mesmo pacote.      |
| Broadcast | Não existem e são realizados com endereços multicast.                     |

## Sistema Hexadecimal

O sistema hexadecimal (hex) é usado para tornar a representação binária mais legível e compreensível. Podemos mostrar apenas 10 estados (0-9) com o sistema decimal e 2 estados (0/1) com o sistema binário usando um único caractere. Em contraste com os sistemas binário e decimal, podemos usar o sistema hexadecimal para mostrar 16 estados (0-F) com um único caractere.

| Decimal | Hex | Binário |
|---------|-----|---------|
| 1       | 1   | 0001    |
| 2       | 2   | 0010    |
| 3       | 3   | 0011    |
| 4       | 4   | 0100    |
| 5       | 5   | 0101    |
| 6       | 6   | 0110    |
| 7       | 7   | 0111    |
| 8       | 8   | 1000    |
| 9       | 9   | 1001    |
| 10      | A   | 1010    |
| 11      | B   | 1011    |
| 12      | C   | 1100    |
| 13      | D   | 1101    |
| 14      | E   | 1110    |
| 15      | F   | 1111    |

Vamos ver um exemplo com um endereço IPv4 e como o endereço IPv4 (192.168.12.160) ficaria na representação hexadecimal.

| Representação | 1º Octeto | 2º Octeto | 3º Octeto | 4º Octeto |
|---------------|-----------|-----------|-----------|-----------|
| Binário       | 1100 0000 | 1010 1000 | 0000 1100 | 1010 0000 |
| Hex           | C0        | A8        | 0C        | A0        |
| Decimal       | 192       | 168       | 12        | 160       |

## Representação de Endereços IPv6

No total, o endereço IPv6 consiste em 16 bytes. Devido ao seu comprimento, um endereço IPv6 é representado em notação hexadecimal. Portanto, os 128 bits são divididos em 8 blocos multiplicados por 16 bits (ou 4 números hexadecimais). Todos os quatro números hexadecimais são agrupados e separados por dois pontos (:) em vez de um simples ponto (.) como no IPv4. Para simplificar a notação, omitimos pelo menos 4 zeros à esquerda nos blocos e podemos substituí-los por dois pontos (::).

Um endereço IPv6 pode ser assim:

- IPv6 completo: fe80:0000:0000:0000:dd80:b1a9:6687:2d3b/64
- IPv6 curto: fe80::dd80:b1a9:6687:2d3b/64

Um endereço IPv6 consiste em duas partes:

- Prefixo de Rede (parte da rede)
- Identificador de Interface, também chamado de Sufixo (parte do host)

O Prefixo de Rede identifica a rede, sub-rede ou intervalo de endereços. O Identificador de Interface é formado a partir do endereço MAC de 48 bits (que discutiremos mais tarde) da interface e é convertido em um endereço de 64 bits no processo. O comprimento de prefixo padrão é /64. No entanto, outros prefixos típicos são /32, /48 e /56. Se quisermos usar nossas redes, obtemos um prefixo mais curto (por exemplo, /56) do que /64 do nosso provedor.

No RFC 5952, a notação de endereço IPv6 mencionada foi definida:

- Todos os caracteres alfabéticos são sempre escritos em minúsculas.
- Todos os zeros à esquerda de um bloco são sempre omitidos.
- Um ou mais blocos consecutivos de 4 zeros (hex) são encurtados por dois pontos (::).
- O encurtamento para dois pontos (::) só pode ser realizado uma vez, começando da esquerda.
