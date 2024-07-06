# Modelo OSI

## Introdução

O objetivo na definição do padrão ISO/OSI era criar um modelo de referência que permitisse a comunicação de diferentes sistemas técnicos por meio de vários dispositivos e tecnologias, proporcionando compatibilidade. **O modelo OSI usa sete camadas diferentes**, hierarquicamente baseadas umas nas outras, para atingir esse objetivo. Essas camadas representam fases no estabelecimento de cada conexão pela qual os pacotes enviados passam. Dessa forma, o padrão foi criado para rastrear visualmente como uma conexão é estruturada e estabelecida.

## Camadas do Modelo OSI

### Camada 7: Aplicação (Application Layer)

- **Função:** Controla a entrada e saída de dados e fornece as funções do aplicativo.
- **Exemplo:** Protocolos como HTTP, FTP, SMTP.

### Camada 6: Apresentação (Presentation Layer)

- **Função:** Transforma a apresentação de dados dependente do sistema para um formato independente do aplicativo.
- **Exemplo:** Criptografia, compressão de dados.

### Camada 5: Sessão (Session Layer)

- **Função:** Controla a conexão lógica entre dois sistemas e evita interrupções de conexão.
- **Exemplo:** Estabelecimento e gerenciamento de sessões.

### Camada 4: Transporte (Transport Layer)

- **Função:** Controle de ponta a ponta dos dados transferidos, detecta e evita congestionamentos, segmenta fluxos de dados.
- **Exemplo:** Protocolos como TCP, UDP.

### Camada 3: Rede (Network Layer)

- **Função:** Estabelece conexões em redes comutadas por circuitos e encaminha pacotes de dados em redes comutadas por pacotes.
- **Exemplo:** Roteamento, endereçamento IP.

### Camada 2: Enlace de Dados (Data Link Layer)

- **Função:** Habilita transmissões confiáveis e livres de erros no respectivo meio, dividindo bitstreams em blocos ou frames.
- **Exemplo:** Ethernet, MAC addresses.

### Camada 1: Física (Physical Layer)

- **Função:** Transmissão de sinais elétricos, ópticos ou ondas eletromagnéticas em linhas de transmissão com ou sem fio.
- **Exemplo:** Cabos, hubs, repetidores.

## Orientações das Camadas

- **Camadas 2-4:** Orientadas ao transporte (transport-oriented).
- **Camadas 5-7:** Orientadas à aplicação (application-oriented).

Cada camada executa tarefas definidas com precisão e descreve interfaces para as camadas vizinhas. Cada camada oferece serviços para a camada diretamente acima dela e usa os serviços da camada abaixo para executar suas tarefas.

## Comunicação entre Sistemas

Quando dois sistemas se comunicam, todas as sete camadas do modelo OSI são percorridas pelo menos duas vezes, uma vez pelo remetente e outra pelo destinatário. Isso garante a segurança, confiabilidade e desempenho da comunicação.

- **Envio de Pacotes:** O sistema remetente trabalha da camada 7 para a camada 1.
- **Recepção de Pacotes:** O sistema receptor descompacta o pacote recebido da camada 1 para a camada 7.

