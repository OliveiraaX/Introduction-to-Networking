### Redes Sem Fio

Redes sem fio são redes de computadores que utilizam conexões de dados sem fio entre nós da rede. Essas redes permitem que dispositivos como laptops, smartphones e tablets se comuniquem entre si e com a Internet sem a necessidade de conexões físicas, como cabos.

As redes sem fio usam tecnologia de radiofrequência (RF) para transmitir dados entre dispositivos. Cada dispositivo em uma rede sem fio possui um adaptador sem fio que converte dados em sinais de RF e os envia pelo ar. Outros dispositivos na rede recebem esses sinais com seus próprios adaptadores sem fio, e os dados são então convertidos de volta em uma forma utilizável. As redes sem fio podem operar em vários alcances, dependendo da tecnologia usada. Por exemplo, uma rede local (LAN) que cobre uma pequena área, como uma casa ou pequeno escritório, pode usar uma tecnologia sem fio chamada WiFi, que tem um alcance de algumas centenas de pés. Por outro lado, uma rede de área ampla sem fio (WWAN) pode usar tecnologia de telecomunicação móvel, como dados celulares (3G, 4G LTE, 5G), que podem cobrir uma área muito maior, como uma cidade inteira ou região.

Portanto, para conectar-se a uma rede sem fio, um dispositivo deve estar dentro do alcance da rede e configurado com as configurações de rede corretas, como o nome da rede e a senha. Uma vez conectado, os dispositivos podem se comunicar entre si e com a Internet, permitindo que os usuários acessem recursos online e troquem dados.

A comunicação entre dispositivos ocorre via RF nas bandas de 2,4 GHz ou 5 GHz em uma rede WiFi. Quando um dispositivo, como um laptop, deseja enviar dados pela rede, ele primeiro se comunica com o Ponto de Acesso Sem Fio (WAP) para solicitar permissão para transmitir. O WAP é um dispositivo central, como um roteador, que conecta a rede sem fio a uma rede com fio e controla o acesso à rede. Uma vez que o WAP concede permissão, o dispositivo transmissor envia os dados como sinais de RF, que são recebidos pelos adaptadores sem fio de outros dispositivos na rede. Os dados são então convertidos de volta em uma forma utilizável e passados para o aplicativo ou sistema apropriado.

A força do sinal de RF e a distância que ele pode percorrer são influenciadas por fatores como a potência do transmissor, a presença de obstáculos e a densidade de ruído RF no ambiente. Portanto, para garantir uma comunicação confiável, as redes WiFi usam técnicas como transmissão de espectro espalhado e correção de erros para superar esses desafios.

#### Conexão WiFi

O dispositivo também deve ser configurado com as configurações de rede corretas, como o nome da rede / Identificador de Conjunto de Serviço (SSID) e a senha. Para conectar-se ao roteador, o laptop usa um protocolo de rede sem fio chamado IEEE 802.11. Este protocolo define os detalhes técnicos de como os dispositivos sem fio se comunicam entre si e com os WAPs. Quando um dispositivo deseja se juntar a uma rede WiFi, ele envia uma solicitação ao WAP para iniciar o processo de conexão. Essa solicitação é conhecida como quadro de solicitação de conexão ou solicitação de associação e é enviada usando o protocolo de rede sem fio IEEE 802.11. O quadro de solicitação de conexão contém vários campos de informações, incluindo, mas não se limitando a:

- **Endereço MAC:** Um identificador exclusivo para o adaptador sem fio do dispositivo.
- **SSID:** O nome da rede, também conhecido como Identificador de Conjunto de Serviço da rede WiFi.
- **Taxas de dados suportadas:** Uma lista das taxas de dados que o dispositivo pode se comunicar.
- **Canais suportados:** Uma lista dos canais (frequências) nos quais o dispositivo pode se comunicar.
- **Protocolos de segurança suportados:** Uma lista dos protocolos de segurança que o dispositivo é capaz de usar, como WPA2/WPA3.

O dispositivo então usa essas informações para configurar seu adaptador sem fio e conectar-se ao WAP. Uma vez estabelecida a conexão, o dispositivo pode se comunicar com o WAP e outros dispositivos na rede. Ele também pode acessar a Internet e outros recursos online por meio do WAP, que atua como um gateway para a rede com fio. No entanto, o SSID pode ser ocultado desativando a transmissão. Isso significa que dispositivos que procuram por aquele WAP específico não poderão identificar seu SSID. No entanto, o SSID ainda pode ser encontrado no pacote de autenticação.

Além do protocolo IEEE 802.11, outros protocolos e tecnologias de rede também podem ser usados, como TCP/IP, DHCP e WPA2, em uma rede WiFi para realizar tarefas como atribuição de endereços IP aos dispositivos, roteamento de tráfego entre dispositivos e fornecimento de segurança.

#### Desafio-Resposta WEP

O handshake de desafio-resposta é um processo para estabelecer uma conexão segura entre um WAP e um dispositivo cliente em uma rede sem fio que usa o protocolo de segurança WEP. Isso envolve a troca de pacotes entre o WAP e o dispositivo cliente para autenticar o dispositivo e estabelecer uma conexão segura.

| Etapa | Quem    | Descrição                                                             |
|-------|---------|----------------------------------------------------------------------|
| 1     | Cliente | Envia um pacote de solicitação de associação ao WAP, solicitando acesso. |
| 2     | WAP     | Responde com um pacote de resposta de associação ao cliente, que inclui uma string de desafio. |
| 3     | Cliente | Calcula uma resposta à string de desafio e uma chave secreta compartilhada e a envia de volta ao WAP. |
| 4     | WAP     | Calcula a resposta esperada ao desafio com a mesma chave secreta compartilhada e envia um pacote de resposta de autenticação ao cliente. |

No entanto, alguns pacotes podem se perder, então a chamada soma de verificação CRC foi integrada. O Cyclic Redundancy Check (CRC) é um mecanismo de detecção de erros usado no protocolo WEP para proteger contra corrupção de dados em comunicações sem fio. Um valor CRC é calculado para cada pacote transmitido na rede sem fio com base nos dados do pacote. Ele é usado para verificar a integridade dos dados. Quando o dispositivo de destino recebe o pacote, o valor CRC é recalculado e comparado ao valor original. Se os valores corresponderem, os dados foram transmitidos com sucesso sem erros. No entanto, se os valores não corresponderem, os dados foram corrompidos e precisam ser retransmitidos.

O design do mecanismo CRC tem uma falha que permite a nós decifrar um único pacote sem conhecer a chave de criptografia. Isso ocorre porque o valor CRC é calculado usando os dados em texto claro no pacote, em vez dos dados criptografados. No WEP, o valor CRC é incluído no cabeçalho do pacote junto com os dados criptografados. Quando o dispositivo de destino recebe o pacote, o valor CRC é recalculado e comparado ao original para garantir que os dados foram transmitidos com sucesso sem erros. No entanto, podemos usar o CRC para determinar os dados em texto claro no pacote, mesmo que os dados estejam criptografados.

#### Recursos de Segurança

As redes WiFi têm vários recursos de segurança para proteger contra o acesso não autorizado e garantir a privacidade e a integridade dos dados transmitidos na rede. Alguns dos principais recursos de segurança incluem, mas não se limitam a:

- **Criptografia**
- **Controle de Acesso**
- **Firewall**

**Criptografia**

Podemos usar vários algoritmos de criptografia para proteger a confidencialidade dos dados transmitidos nas redes sem fio. Os algoritmos de criptografia mais comuns nas redes WiFi são Wired Equivalent Privacy (WEP), WiFi Protected Access 2 (WPA2) e WiFi Protected Access 3 (WPA3).

**Controle de Acesso**

As redes WiFi são configuradas por padrão para permitir que dispositivos autorizados se conectem à rede usando métodos específicos de autenticação. No entanto, esses métodos podem ser alterados para exigir uma senha ou um identificador exclusivo (como um endereço MAC) para identificar dispositivos autorizados.

**Firewall**

Um firewall é um sistema de segurança que controla o tráfego de rede de entrada e saída com base em regras de segurança predefinidas. Por exemplo, os roteadores WiFi frequentemente possuem firewalls integrados que podem bloquear o tráfego de entrada da Internet e proteger contra vários tipos de ameaças cibernéticas.

#### Protocolos de Criptografia

Wired Equivalent Privacy (WEP) e WiFi Protected Access (WPA) são protocolos de criptografia usados para proteger dados transmitidos em uma rede WiFi. WPA pode usar diferentes algoritmos de criptografia, incluindo Advanced Encryption Standard (AES).

**WEP**

WEP usa uma chave de 40 bits ou 104 bits para criptografar dados, enquanto o WPA usando AES usa uma chave de 128 bits. Chaves mais longas fornecem criptografia mais robusta e são mais resistentes a ataques. No entanto, é vulnerável a vários ataques que podem permitir que um invasor decifre dados transmitidos na rede. Além disso, o WEP não é compatível com dispositivos e sistemas operacionais mais novos e geralmente não é mais considerado seguro. Finalmente, o WEP usa o algoritmo de criptografia RC4, o que o torna vulnerável a ataques.

No entanto, o WEP usa uma chave compartilhada para autenticação, o que significa que a mesma chave é usada para criptografia e autenticação. Existem duas versões do protocolo WEP:

- **WEP-40/WEP-64**
- **WEP-104**

O WEP-40, também conhecido como WEP-64, usa uma chave de 40 bits (secreta), enquanto o WEP-104 usa uma chave de 104 bits. A chave é dividida em um Vetor de Inicialização (IV) e uma chave secreta.

O IV é um pequeno valor incluído no cabeçalho do pacote junto com os dados criptografados e é usado para criar a chave tanto para o WEP-40 quanto para o WEP-104 e é incluído para garantir que cada chave seja única. A chave secreta é uma série de bits aleatórios usados para criptografar os dados. No entanto, o WEP-104 tem uma chave secreta de 80 bits. Vamos observar a tabela a seguir para ver claramente as diferenças:

| Protocolo         | IV    | Chave Secreta |
|-------------------|-------|---------------|
| WEP-40/WEP-64     | 24-bit| 40-bit        |
| WEP-104           | 24-bit| 80-bit        |

No entanto, como o IV no WEP é relativamente pequeno, podemos usar força bruta para tentar todas as combinações possíveis de caracteres para ele e determinar o valor correto. Depois, podemos usá-lo para decifrar os dados no pacote. Isso nos permite acessar os dados transmitidos na rede sem fio e potencialmente comprometer a segurança da rede.

**WPA**

O WPA fornece o mais alto nível de segurança e não é suscetível aos mesmos tipos de ataques que o WEP. Além disso, o WPA usa métodos de autenticação mais seguros, como uma chave pré-compartilhada (PSK) ou um servidor de autenticação 802.1X, que oferecem proteção mais forte contra acesso não autorizado. Embora dispositivos mais antigos possam não suportar o WPA, ele é compatível com a maioria dos dispositivos e sistemas operacionais. Todas as redes sem fio, especialmente em infraestrutura crítica como escritórios, devem geralmente implementar pelo menos WPA2 ou até mesmo WPA3.

#### Protocolos de Autenticação

Lightweight Extensible Authentication Protocol (LEAP) e Protected Extensible Authentication Protocol (PEAP) são protocolos de autenticação usados para proteger redes sem fio, fornecendo um método seguro para autenticar dispositivos em uma rede sem fio e são frequentemente usados em conjunto com WEP ou WPA para fornecer uma camada adicional de segurança.

LEAP e PEAP são ambos baseados no Extensible Authentication Protocol (EAP), uma estrutura para autenticação usada em vários contextos de rede. No entanto, uma diferença fundamental entre LEAP e PEAP é a forma como eles protegem o processo de autenticação.

- **LEAP:** Usa uma chave compartilhada para autenticação, o que significa que a mesma chave é usada para criptografia e autenticação. Isso pode facilitar a obtenção de acesso à rede se a chave for comprometida.
- **PEAP:** Usa um método de autenticação mais seguro chamado tunneled Transport Layer Security (TLS). Este método estabelece uma conexão segura entre o dispositivo e o WAP usando um certificado digital, e um túnel criptografado protege o processo de autenticação. Isso oferece proteção mais robusta contra acesso não autorizado e é mais resistente a ataques.

#### TACACS+

Em uma rede sem fio, quando um ponto de acesso sem fio (WAP) envia uma solicitação de autenticação para um servidor Terminal Access Controller Access-Control System Plus (TACACS+), é provável que todo o pacote de solicitação esteja criptografado para proteger a confidencialidade e a integridade da solicitação.

O TACACS+ é um protocolo usado para autenticar e autorizar usuários que acessam dispositivos de rede, como roteadores e switches. Quando um WAP envia uma solicitação de autenticação para um servidor TACACS+, a solicitação geralmente inclui as credenciais do usuário e outras informações sobre a sessão.

Criptografar a solicitação de autenticação ajuda a garantir que essas informações sensíveis não sejam visíveis para partes não autorizadas que possam interceptar a solicitação enquanto ela está sendo transmitida pela rede. Também ajuda a prevenir a adulteração da solicitação ou a substituição dela por uma solicitação maliciosa própria.

Vários métodos de criptografia podem ser usados para criptografar a solicitação de autenticação, como SSL/TLS ou IPSec. O método de criptografia específico usado pode depender da configuração do servidor TACACS+ e das capacidades do WAP.

#### Ataque de Dissociação

Um ataque de dissociação é um tipo de ataque a todas as redes sem fio que visa interromper a comunicação entre um WAP e seus clientes enviando quadros de dissociação para um ou mais clientes.

O WAP usa quadros de dissociação para desconectar um cliente da rede. Quando um WAP envia um quadro de dissociação para um cliente, o cliente se desconecta da rede e precisa se reconectar para continuar usando a rede.

Podemos lançar o ataque de dentro ou fora da rede, dependendo de nossa localização e das medidas de segurança da rede. O objetivo desse ataque é interromper a comunicação entre o WAP e seus clientes, fazendo com que os clientes se desconectem e possivelmente causando inconveniência ou interrupção aos usuários. Também podemos usá-lo como um precursor para outros ataques, como um ataque MITM, forçando os clientes a se reconectar à rede e potencialmente expondo-os a ataques adicionais.

#### Endurecimento de Redes Sem Fio

Existem muitas maneiras diferentes de proteger redes sem fio. No entanto, alguns exemplos devem ser considerados para aumentar dramaticamente a segurança das redes sem fio. Estes são os seguintes, mas não se limitando a:

- Desativação da transmissão
- WiFi Protected Access
- Filtragem MAC
- Implantação de EAP-TLS

**Desativação da Transmissão**

Desativar a transmissão do SSID é uma medida de segurança que pode ajudar a endurecer um WAP tornando mais difícil descobrir e conectar-se à rede. Quando o SSID é transmitido, ele é incluído em quadros de beacon regularmente transmitidos pelo WAP para anunciar a disponibilidade da rede. Ao desativar a transmissão do SSID, o WAP não transmitirá quadros de beacon, e a rede não será visível para dispositivos que não estão já conectados à rede.

**WPA**

Novamente, o WPA fornece forte criptografia e autenticação para comunicações sem fio, ajudando a proteger contra acesso não autorizado à rede e interceptação de dados confidenciais. O WPA inclui duas versões principais:

- WPA-Pessoal
- WPA-Empresarial

O WPA-Pessoal, projetado para redes domésticas e de pequenas empresas, e o WPA-Empresarial, projetado para organizações maiores e que usa um servidor de autenticação centralizado (por exemplo, RADIUS ou TACACS+) para verificar a identidade dos clientes.

**Filtragem MAC**

A filtragem MAC é uma medida de segurança que permite a um WAP aceitar ou rejeitar conexões de dispositivos específicos com base em seus endereços MAC. Configurando o WAP para aceitar conexões apenas de dispositivos com endereços MAC aprovados, é possível impedir que dispositivos não autorizados se conectem à rede.

**Implantação de EAP-TLS**

O EAP-TLS é um protocolo de segurança usado para autenticar e criptografar comunicações sem fio. Ele usa certificados digitais e PKI para verificar a identidade dos clientes e estabelecer conexões seguras. Implantar o EAP-TLS pode ajudar a endurecer um WAP, fornecendo autenticação e criptografia fortes para comunicações sem fio, o que pode proteger contra acesso não autorizado à rede e a interceptação de dados confidenciais.
