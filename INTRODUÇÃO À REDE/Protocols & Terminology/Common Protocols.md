### Protocolos Comuns

**Protocolos de Internet** são regras padronizadas definidas em RFCs que especificam como os dispositivos em uma rede devem se comunicar. Eles garantem a troca consistente e confiável de informações, independentemente do hardware e software. Os dispositivos comunicam-se usando protocolos padronizados por meio de uma conexão com ou sem fio. Os dois principais tipos de conexões são o Protocolo de Controle de Transmissão (TCP) e o Protocolo de Datagrama de Usuário (UDP).

Precisamos conhecer vários protocolos comumente usados para gerenciar efetivamente as comunicações de rede. Abaixo estão alguns protocolos-chave que encontramos com frequência:

#### Protocolo de Controle de Transmissão (TCP)
O TCP é um protocolo orientado à conexão que estabelece uma conexão virtual antes da transmissão de dados, usando um Three-Way-Handshake. Essa conexão é mantida até a conclusão da transferência de dados.

Por exemplo, ao inserir um URL em um navegador da web, uma solicitação HTTP é enviada usando TCP. O servidor responde com o código HTML do site via TCP, que o navegador usa para renderizar o site. O TCP é confiável, mas mais lento devido à sobrecarga de estabelecimento de conexão.

**Protocolos TCP Comuns:**
| Protocolo                             | Acrônimo | Porta   | Descrição                                |
|---------------------------------------|----------|---------|------------------------------------------|
| Telnet                                | Telnet   | 23      | Serviço de login remoto                  |
| Secure Shell                          | SSH      | 22      | Serviço de login remoto seguro           |
| Simple Network Management Protocol    | SNMP     | 161-162 | Gerenciamento de dispositivos de rede    |
| Hyper Text Transfer Protocol          | HTTP     | 80      | Transferência de páginas web             |
| Hyper Text Transfer Protocol Secure   | HTTPS    | 443     | Transferência de páginas web seguras     |
| Domain Name System                    | DNS      | 53      | Resolução de nomes de domínio            |
| File Transfer Protocol                | FTP      | 20-21   | Transferência de arquivos                |
| Trivial File Transfer Protocol        | TFTP     | 69      | Transferência de arquivos simplificada   |
| Network Time Protocol                 | NTP      | 123     | Sincronização de relógios de computadores|
| Simple Mail Transfer Protocol         | SMTP     | 25      | Transferência de emails                  |
| Post Office Protocol                  | POP3     | 110     | Recuperação de emails                    |
| Internet Message Access Protocol      | IMAP     | 143     | Acesso a emails                          |
| Server Message Block                  | SMB      | 445     | Transferência de arquivos e impressão    |
| Network File System                   | NFS      | 111, 2049 | Montagem de sistemas remotos             |
| Bootstrap Protocol                    | BOOTP    | 67, 68  | Inicialização de computadores            |
| Kerberos                              | Kerberos | 88      | Autenticação e autorização               |
| Lightweight Directory Access Protocol | LDAP     | 389     | Serviços de diretório                    |
| Remote Authentication Dial-In User Service | RADIUS | 1812, 1813 | Autenticação e autorização          |
| Dynamic Host Configuration Protocol   | DHCP     | 67, 68  | Configuração de endereços IP             |
| Remote Desktop Protocol               | RDP      | 3389    | Acesso remoto à área de trabalho         |
| Network News Transfer Protocol        | NNTP     | 119     | Acesso a grupos de notícias              |
| Remote Procedure Call                 | RPC      | 135, 137-139 | Chamada de procedimentos remotos     |
| Identification Protocol               | Ident    | 113     | Identificação de processos de usuários   |
| Internet Control Message Protocol     | ICMP     | 0-255   | Solução de problemas de rede             |
| Internet Group Management Protocol    | IGMP     | 0-255   | Multicast de rede                        |
| Oracle DB (Default/Alternative) Listener | oracle-tns | 1521/1526 | Serviço de banco de dados Oracle      |
| Ingres Lock                           | ingreslock | 1524  | Gerenciamento de banco de dados Ingres   |
| Squid Web Proxy                       | http-proxy | 3128  | Proxy web Squid                          |
| Secure Copy Protocol                  | SCP      | 22      | Cópia segura de arquivos entre sistemas  |
| Session Initiation Protocol           | SIP      | 5060    | Sessões VoIP                             |
| Simple Object Access Protocol         | SOAP     | 80, 443 | Serviços web                             |
| Secure Socket Layer                   | SSL      | 443     | Transferência segura de arquivos         |
| TCP Wrappers                          | TCPW     | 113     | Controle de acesso                       |
| Internet Security Association and Key Management Protocol | ISAKMP | 500 | Conexões VPN                      |
| Microsoft SQL Server                  | ms-sql-s | 1433    | Conexões cliente para Microsoft SQL Server |
| Kerberized Internet Negotiation of Keys | KINK | 892  | Autenticação e autorização               |
| Open Shortest Path First              | OSPF     | 89      | Roteamento                               |
| Point-to-Point Tunneling Protocol     | PPTP     | 1723    | Criação de VPNs                          |
| Remote Execution                      | REXEC    | 512     | Execução de comandos remotos             |
| Remote Login                          | RLOGIN   | 513     | Sessão de shell interativo remoto        |
| X Window System                       | X11      | 6000    | Interface gráfica de usuário para sistemas em rede |
| Relational Database Management System | DB2      | 50000   | Gerenciamento de banco de dados          |

#### Protocolo de Datagrama de Usuário (UDP)
O UDP é um protocolo sem conexão, o que significa que não estabelece uma conexão virtual antes da transmissão de dados. Em vez disso, ele envia os pacotes de dados ao destino sem verificar se foram recebidos.

Por exemplo, ao transmitir ou assistir a um vídeo em uma plataforma como o YouTube, os dados do vídeo são transmitidos usando UDP. Isso porque o vídeo pode tolerar alguma perda de dados, e a velocidade de transmissão é mais importante do que a confiabilidade. Isso torna o UDP mais rápido que o TCP, mas menos confiável.

**Protocolos UDP Comuns:**
| Protocolo                             | Acrônimo | Porta   | Descrição                                |
|---------------------------------------|----------|---------|------------------------------------------|
| Domain Name System                    | DNS      | 53      | Resolução de nomes de domínio            |
| Trivial File Transfer Protocol        | TFTP     | 69      | Transferência de arquivos simplificada   |
| Network Time Protocol                 | NTP      | 123     | Sincronização de relógios de computadores|
| Simple Network Management Protocol    | SNMP     | 161     | Gerenciamento de dispositivos de rede    |
| Routing Information Protocol          | RIP      | 520     | Troca de informações de roteamento       |
| Internet Key Exchange                 | IKE      | 500     | Troca de chaves de segurança             |
| Bootstrap Protocol                    | BOOTP    | 68      | Inicialização de hosts na rede           |
| Dynamic Host Configuration Protocol   | DHCP     | 67      | Configuração dinâmica de endereços IP    |
| Telnet                                | TELNET   | 23      | Protocolo de comunicação de acesso remoto|
| MySQL                                 | MySQL    | 3306    | Sistema de gerenciamento de banco de dados|
| Terminal Server                       | TS       | 3389    | Protocolo de acesso remoto para Microsoft Windows Terminal Services|
| NetBIOS Name                          | netbios-ns | 137    | Resolução de nomes NetBIOS em endereços IP|
| Microsoft SQL Server                  | ms-sql-m | 1434    | Serviço de navegação do Microsoft SQL Server|
| Universal Plug and Play               | UPnP     | 1900    | Protocolo de descoberta e comunicação de dispositivos na rede|
| PostgreSQL                            | PGSQL    | 5432    | Sistema de gerenciamento de banco de dados|
| Virtual Network Computing             | VNC      | 5900    | Sistema de compartilhamento de desktop gráfico|
| X Window System                       | X11      | 6000-6063 | Interface gráfica de usuário em sistemas Unix-like|
| Syslog                                | SYSLOG   | 514     | Coleta e armazenamento de mensagens de log|
| Internet Relay Chat                   | IRC      | 194     | Protocolo de comunicação em tempo real na Internet|
| OpenPGP                               | OpenPGP  | 11371   | Protocolo de criptografia e assinatura de dados e comunicações|
| Internet Protocol Security            | IPsec    | 500     | Protocolo de comunicação segura e criptografada|
| Internet Key Exchange                 | IKE      | 11371   | Protocolo de criptografia e assinatura de dados e comunicações|
| X Display Manager Control Protocol    | XDMCP    | 177     | Protocolo de login remoto para o sistema X11|

#### ICMP
O Protocolo de Mensagens de Controle da Internet (ICMP) é usado para comunicação entre dispositivos na Internet para fins diversos, incluindo relatórios de erros e informações de status. Ele envia solicitações e mensagens entre dispositivos, que podem ser usadas para relatar erros ou fornecer informações de status.

**Solicitações ICMP:**
| Tipo de Solicitação           | Descrição                                                    |
|-------------------------------|--------------------------------------------------------------|
| Echo Request                  | Solicita uma resposta do host (usado no comando `ping`)     |
| Echo Reply                    | Responde a uma solicitação de eco                           |
| Destination Unreachable       | Informa que o destino é inatingível                         |
| Source Quench                 | Solicita a redução na taxa de envio de pacotes              |
| Redirect                      | Solicita a alteração na rota de pacotes                     |
| Time Exceeded                 | Indica que o tempo limite para o pacote foi excedido        |
| Parameter Problem             | Informa um problema com os parâmetros do pacote             |
| Timestamp Request             | Solicita a marcação de tempo                                |
| Timestamp Reply               | Responde a uma solicitação de marcação de tempo             |
| Address Mask Request          | Solicita a máscara de endereço                              |
| Address Mask Reply            | Responde a uma solicitação de máscara de endereço           |

Esses são alguns dos principais protocolos que podemos encontrar em nosso trabalho com redes e comunicações. Eles desempenham papéis vitais na operação eficiente e segura das redes de computadores.
