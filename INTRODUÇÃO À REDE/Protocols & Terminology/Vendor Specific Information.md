# Resumo de Tecnologias de Rede

## Cisco IOS

O Cisco IOS é o sistema operacional utilizado em dispositivos de rede Cisco, como roteadores e switches. Ele oferece suporte a uma variedade de recursos essenciais para operações de rede modernas, incluindo:

- Suporte para IPv6
- Qualidade de Serviço (QoS)
- Recursos de segurança, como criptografia e autenticação
- Recursos de virtualização, como VPLS e VRF
- Suporte a diferentes protocolos de rede, como OSPF, BGP, VTP, e DHCP

O Cisco IOS pode ser gerenciado via CLI ou GUI e suporta configuração de senhas para controle de acesso, como senha de usuário, senha de ativação, segredo e segredo de ativação.

## VLANs

As VLANs são agrupamentos lógicos de dispositivos de rede que permitem segmentação baseada em funções, departamentos, ou aplicações. Cada VLAN é um domínio de broadcast separado, aumentando a segurança e o desempenho da rede. Benefícios incluem:

- Melhor organização e segurança
- Administração simplificada e desempenho aumentado

As portas em switches podem ser configuradas como portas de acesso ou tronco, com as portas de tronco transportando múltiplas VLANs através de métodos de trunking como ISL e 802.1Q.

## Segurança VLAN

Embora VLANs melhorem a segurança, ataques como VLAN hopping e VLAN double-tagging podem ser explorados por invasores para acessar informações de outras VLANs.

- VLAN Hopping: Explora o protocolo DTP para acessar outras VLANs em um switch.
- Double-Tagging: Injeta uma segunda tag VLAN para enganar switches e acessar uma VLAN diferente.

## VXLAN

Para escalar redes além das limitações de VLANs tradicionais, VXLAN é usado em data centers. Ele oferece segmentação eficiente e elimina os problemas do STP ao permitir redes virtualizadas em ambientes distribuídos.

## Tshark

Tshark é uma ferramenta para analisar tráfego de rede marcado por VLANs, útil para diagnóstico e segurança.

## PowerShell e Linux

No Windows e Linux, é possível configurar VLANs em adaptadores de rede física usando PowerShell e comandos como `ip` e `vconfig` no Linux.
