# Visão Geral de Rede e Práticas de Segurança

## Introdução à Rede

Uma rede permite a comunicação entre computadores usando várias topologias (mesh, tree, star), meios de comunicação (ethernet, fiber, coaxial, wireless) e protocolos (TCP, UDP, IPX). É fundamental para profissionais de segurança compreenderem redes, pois falhas podem ser sutis e despercebidas.

## Segurança e Segmentação de Rede

Configurar uma rede grande e plana é operacionalmente simples, mas menos seguro. Ao criar redes menores e segmentadas, com Listas de Controle de Acesso (ACLs), adicionamos camadas de defesa. Isso é comparável a colocar cercas ao redor de propriedades para limitar pontos de entrada suspeitos. Por exemplo, por que uma impressora está se comunicando com servidores por HTTP?

Documentar e mapear o propósito de cada rede é essencial, funcionando como luzes ao redor da propriedade para monitorar atividades. Isso ajuda a identificar comportamentos anômalos, como uma rede de impressoras acessando a internet sem autorização.

Sistemas de detecção de intrusão (IDS), como Suricata ou Snort, são como arbustos nas janelas, desencorajando varreduras de rede maliciosas. Por exemplo, detectar uma varredura de porta originada da rede da impressora pode indicar uma tentativa de intrusão.

## Exemplo de Erro Comum em Testes de Penetração

Um erro comum é configurar incorretamente máscaras de sub-rede, como usar /24 quando /25 seria mais apropriado. Isso limita a comunicação entre dispositivos e pode levar a conclusões equivocadas, como considerar um controlador de domínio offline quando ele está em uma rede diferente.

## Práticas de Segurança na Rede

- **DMZ para Servidores:** Isolar servidores web em DMZ protege contra comprometimento por clientes da internet.
  
- **Segmentação de Workstations:** Cada workstation deve ter regras de firewall para evitar ataques de spoofing ou man-in-the-middle.

- **Rede de Administração:** Isolar switches e roteadores impede bisbilhotagem entre dispositivos, evitando ataques como OSPF spoofing.

- **Redes Separadas para Dispositivos Específicos:**
  - **Telefones IP:** Evitar espionagem e gerenciar latência prioritária.
  - **Impressoras:** Proteger contra ataques de senha NTLMv2 e vazamento de informações.

## Exemplo de Configuração de Rede

Um diagrama de configuração de rede mostra redes separadas para diferentes tipos de dispositivos, garantindo segurança e eficiência operacional.

## História Divertida

Durante a COVID-19, um teste de penetração físico usou uma impressora comprometida para acessar credenciais de administração, destacando a importância da segurança em redes bem projetadas.

