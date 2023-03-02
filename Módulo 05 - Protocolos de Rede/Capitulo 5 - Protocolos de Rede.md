# Capitulo 5 - Protocolos de Rede

## Poceso de comunicação de rede



### Redes de Vários Tamanhos



**SOHO** - Redes de pequeno escritório e escritório doméstico



### Comunicação cliente-servidor



**Hosts** - Todos os computadores que estão conectados a uma rede e participam diretamente da comunicação em rede, também podem ser chamados de dispositivos finais, terminais ou nós.

- Grande parte da interação entre dispositivos é o tráfego cliente-servidor



**Servidores** são computadores com software especializado.

- Este software permite que os servidores forneçam informações a outros dispositivos na rede.

- Um servidor pode ser de **propósito único** ou **multiuso**.



- **Servidor de arquivos** - o servidor de arquivos armazena arquivos corporativos e de usuários em um local central.
- **Servidor Web** - O servidor web executa software de servidor web que permite que muitos computadores acessem páginas da web.
- **Servidor de e-mail** - O servidor de e-mail executa o software de servidor de e-mail que permite que os e-mails sejam enviados e recebidos.
  
  
  
  ![RedeClienteServidor01.png](/home/felipe/Documentos/Estudo/CiscoCyberOps/Capitulo%205/img/RedeClienteServidor01.png)



1 - O servidor de arquivos armazena arquivos corporativos e de usuários em um local central. Os dispositivos clientes acessam esses arquivos com softwares clientes, como Windows Explorer

2 - O servidor da Web executa um sofware de servidor da Web e os clientes usam seu software de navegador, como o Windows Microsoft Edge, para acessar páginas da Web no servidor

3 - O servidor de e-mail executa o software do servidor de e-mail. Os clientes usam o software de cliente de e-mails no servidor.



### Traçando o Caminho



Cabos se conectam instalações de telecomunicações e provedores de serviços de internet (ISP) que são distribuidos em todo o mundo. Esses ISPs globais de Nível 1 e Nível 2 conectam partes da Internet, geralmente por meio de um Ponto de Troca de Internet (IXP). Redes maiores se conectarão a redes Nível 2 por meio de um Ponto de Presena (PoP), que geralmente é um local no edifício onde as conexões físicas com o ISP são feitas. Os ISPs de Nível 3 conectam residências e empresas à internet.



Devido aos diversos caminhos que um pacote pode trafegar até chegar ao destino, é importante que os analistas de segurança cibernética sejam capazes de determinar a origem do tráfego que entra na rede e o destino do tráfego que a deixa.



![TraçandooCaminho2.png](/home/felipe/Documentos/Estudo/CiscoCyberOps/Capitulo%205/img/TraçandooCaminho2.png)



## Protocolos de comunicação



### O que são protocolos?



A comunicação, seja cara a cara ou em rede, é governada por regras chamadas de **protocolos**.

- Esses protocolos são específicos para o tipo de método de comunicação em questão.



![Protocolos03.png](/home/felipe/Documentos/Estudo/CiscoCyberOps/Capitulo%205/img/Protocolos03.png)





## Protocolos de rede.



Os protocolos de rede fornecem os meios para que os computadores se comuniquem em redes.

- Protocolos determinam as opções de codificaão, formatação, encapsulamentom tamanho, tempo e entrega da mensagem.

- Definem um conjunto de regras comuns para a troca de mensagens entre dispositivos.
  
  - Alguns protocolos comuns: Hypertext Transfer Protocol (HTTP), Transmission Control Protocol (TCP) e Internet Protocol (IP).



### Conjunto de protocolos TCP/IP



![Protocolos04.png](/home/felipe/Documentos/Estudo/CiscoCyberOps/Capitulo%205/img/Protocolos04.png)



**TCP/IP** é o conjunto de protocolos usado pela internet e as redes hoje. O TCP/IP tem dois aspectos impotentes para fornecedores e fabricantes:



- **Conjunto de Protocolos de padão aberto **- Isso significa que está disponível gratuidamente ao público e pode ser usado por qualquer fornecedor em seu hardware ou software.

- **Conjunto de Protocolos com base em padrões** - Isso significa que foi endossado pela indústria de rede e aprovado por uma organizaão de padrões. Isso garante que produtos de diferentes fabricantes possam interoperar com êxito.



#### Camada de Aplicação



Sistema de nomes

- **DNS** - Sistema de nomes de domínio. Converte nomes de domínio, como cisco.com, em endereços IP.



Configuração de hosts

- **DHCPv4** - Protocolo 
  de configuração de host dinâmico para IPv4. Um servidor DHCPv4 atribui 
  dinamicamente informações de endereçamento IPv4 aos clientes DHCPv4 na 
  inicialização e permite que os endereços sejam reutilizados quando não 
  forem mais necessários.
- **DHCPv6** - Protocolo de 
  Configuração do Host Dinâmico para IPv6. DHCPv6 é semelhante ao DHCPv4. 
  Um servidor DHCPv6 atribui dinamicamente informações de endereçamento 
  IPv6 aos clientes DHCPv6 na inicialização.
- **SLAAC** - Configuração automática de endereço sem estado. Um método que permite
   que um dispositivo obtenha suas informações de endereçamento IPv6 sem 
  usar um servidor DHCPv6.

E-mail

- **SMTP** -Protocolo de transferência de correio simples. Permite que os 
  clientes enviem e-mails para um servidor de e-mail e permite que os 
  servidores enviem e-mails para outros servidores.
- **POP3** - Post Office Protocol versão 3. Permite que os clientes recuperem 
  e-mails de um servidor de e-mail e baixem o e-mail para o aplicativo de 
  e-mail local do cliente.
- **IMAP** - Protocolo de 
  Acesso à Mensagem na Internet. Permite que os clientes acessem o e-mail 
  armazenado em um servidor de e-mail e também mantenham o e-mail no 
  servidor.

Transferência de arquivos

- **FTP** - Protocolo de transferência de arquivos. Define as regras que 
  permitem que um usuário em um host acesse e transfira arquivos para e de  outro host em uma rede. O FTP é um protocolo de entrega de arquivos confiável, orientado a conexão e reconhecido.
- **SFTP** - Protocolo de transferência de arquivos SSH. Como uma extensão do protocolo Secure Shell (SSH), o SFTP pode ser usado para estabelecer uma  sessão segura de transferência de arquivos na qual a transferência é  criptografada. SSH é um método para login remoto seguro que normalmente é  usado para acessar a linha de comando de um dispositivo.
- **TFTP** - Protocolo de Transferência de Arquivos Trivial. Um protocolo de 
  transferência de arquivos simples e sem conexão com entrega de arquivos não confirmada e de melhor esforço. Ele usa menos sobrecarga que o FTP.

Web e serviço Web

- **HTTP** - Protocolo de transferência de hipertexto. Um conjunto de regras para a troca de texto, imagens gráficas, som, vídeo e outros arquivos 
  multimídia na World Wide Web.
- **HTTPS** - HTTP seguro. Uma forma segura de HTTP que criptografa os dados que são trocados pela World Wide Web.
- **REST** - Representational State Transfer. Um serviço Web que utiliza 
  interfaces de programação de aplicações (APIs) e pedidos HTTP para criar  aplicações Web.



#### Camada de transporte



Conexão orientada

- **TCP** - Protocolo de 
  controle de transmissão. Permite a comunicação confiável entre processos
   executados em hosts separados e fornece transmissões confiáveis e 
  reconhecidas que confirmam a entrega bem-sucedida.

Sem Conexão

- **UDP** - Protocolo de datagrama do usuário. Permite que um processo em 
  execução em um host envie pacotes para um processo em execução em outro 
  host. No entanto, o UDP não confirma a transmissão bem-sucedida do 
  datagrama.



#### Camada de internet

 Protocolo IP (Internet Protocol)

- **IPv4** - Protocolo da Internet versão 4. Recebe segmentos de mensagem da camada de transporte, empacota mensagens em pacotes e endereça pacotes para entrega de ponta a ponta através de uma rede. O IPv4 usa um endereço de 32 bits.
- **IPv6** - IP versão 6. Semelhante ao IPv4, mas usa um endereço de 128 bits.
- **NAT** - Tradução de endereços de rede. Converte endereços IPv4 de uma rede privada em endereços IPv4 públicos globalmente exclusivos.

Mensagens

- **ICMPv4** - Protocolo de mensagens de controle da Internet para IPv4. Fornece feedback de um host de destino para um host de origem sobre erros na entrega de pacotes.
- **ICMPv6** - ICMP para IPv6. Funcionalidade semelhante ao ICMPv4, mas é usada para pacotes IPv6.
- **ICMPv6 ND** - descoberta de vizinho ICMPv6. Inclui quatro mensagens de protocolo que são usadas para resolução de endereço e detecção de endereço duplicado.

Protocolos de roteamento

- **OSPF** - Abrir o caminho mais curto primeiro. Protocolo de roteamento de estado de link que usa um experimento hierárquico baseado em áreas. OSPF é um protocolo de roteamento interno padrão aberto.
- **EIGRP** - Protocolo de roteamento de gateway interno aprimorado. Um protocolo de roteamento de padrão aberto desenvolvido pela Cisco que usa uma métrica composta com base na largura de banda, atraso, carga e confiabilidade.
- **BGP** - Protocolo de gateway de 
  fronteira. Um protocolo de roteamento de gateway externo padrão aberto usado entre os Internet Service Providers (ISPs). O BGP também é comumente usado entre os ISPs e seus grandes clientes particulares para trocar informações de roteamento.



#### Camada de acesso à rede



Resolução de endereços

- **ARP** - Protocolo de Resolução de Endereço. Fornece mapeamento de endereço  dinâmico entre um endereço IPv4 e um endereço de hardware.
  
  **Observação**:
   Você pode ver outro estado de documentação que o ARP opera na Camada da  Internet (Camada OSI 3). No entanto, neste curso, afirmamos que o ARP  opera na camada de Acesso à Rede (OSI Camada 2) porque seu objetivo  principal é descobrir o endereço MAC do destino. Um endereço MAC é um endereço da camada 2.

Protocolos de link de dados

- **Ethernet** - define as regras para os padrões de fiação e sinalização da camada de acesso à rede.
- **WLAN** - Rede local sem fio. Define as regras para sinalização sem fio nas frequências de rádio de 2,4 GHz e 5 GHz.



### Formatação e Encapsulamento de Mensagens



#### Analogia



Um exemplo comum de exigir o formato correto nas comunicações humanas  é ao enviar uma carta. Clique em Reproduzir na figura para exibir uma animação de formatação e encapsulamento de uma letra.

Um envelope tem o endereço do remetente e do destinatário, cada um localizado no local apropriado no envelope. Se o endereço destino e a formatação não estiverem corretos, a carta não será entregue.

O processo de colocar um formato de mensagem (a carta) em outro formato de mensagem (o  envelope) é chamado encapsulamento. O desencapsulamento ocorre quando o  processo é invertido pelo destinatário e a carta é retirada do envelope.



#### Rede



Semelhante ao envio de uma carta, uma mensagem enviada por uma rede de  computadores segue regras específicas de formato para que ela seja 
entregue e processada.

Internet Protocol (IP) é um protocolo com uma função semelhante ao exemplo de envelope. Na figura, os campos do pacote IPv6 (Internet Protocol versão 6) identificam a origem do pacote e seu destino. IP é responsável por enviar uma mensagem da origem da mensagem para o destino através de uma ou mais redes.

**Nota**: Os campos do pacote IPv6 são discutidos em detalhes em outro módulo.



![Protocolos5.png](/home/felipe/Documentos/Estudo/CiscoCyberOps/Capitulo%205/img/Protocolos5.png)

### Tamanho da Mensagem



#### Analogia

Quando as pessoas se comunicam entre si, as mensagens que enviam 
geralmente são quebradas em partes ou sentenças menores. Essas sentenças  são limitadas em tamanho ao que a pessoa receptora pode processar de uma só vez, conforme mostrado na figura. Também torna mais fácil para o receptor ler e compreender.



#### Rede



Do mesmo modo, quando uma mensagem longa é enviada de um host a outro em uma rede, é necessário dividir a mensagem em partes menores. As regras que regem o tamanho das partes, ou quadros, transmitidos pela rede são muito rígidas. Também podem diferir, 
dependendo do canal usado. Os quadros que são muito longos ou muito 
curtos não são entregues.

As restrições de tamanho dos quadros exigem que o host origem divida uma mensagem longa em pedaços individuais que atendam aos requisitos de tamanho mínimo e máximo. A mensagem longa será enviada em quadros separados, e cada um contém uma parte da mensagem original. Cada quadro também terá suas próprias informações de endereço. No host destino, as partes individuais da mensagem são reconstruídas na mensagem original



### Teporização de Mensagem



A temporização de rede é importante, inclui o seguinte:



- Controle de fluxo - é o processo de gerenciamento da taxa de transmissão de dados. Define quanta informação pode ser enviada e a velocidade.

- Tempo limite de resposta - Hosts de rede usam protocolos de rede que especificam quanto tempo esperar pelas respostas e que ação executar se ocorrer um tempo limite de respota

- Método de acesso - Determinar quando alguém pode enviar uma mensagem. Um exemplo é quando um dispositivo deseja transmitir em uma LAN sem fio, é necessário que a placa de interface de rede (NIC) da WLAN determine se a mídia sem fio está disponível.



### Unicast, broadcast ou multicast



**Unicast** - há um único destino para a mensagem

**Multicast** - O host precisa enviar mensagens por meio de uma opção de entrega um para muitos.

**Broadcast** - Representa a entrega de mensagem de um para todos.



### Benefícios de usar um modelo de camadas.



- Auxiliar no projeto de protocolo porque os protocolos que operam
   em uma camada específica têm informações definidas sobre as quais eles 
  atuam e uma interface definida para as camadas acima e abaixo
- Estimular a competição porque os produtos de diferentes fornecedores podem trabalhar em conjunto.
- Impedir que mudanças de tecnologia ou capacidade em uma camada afetem outras camadas acima e abaixo.
- Fornecer um idioma comum para descrever funções e capacidades de rede.



Existem dois modelos em camadass que são usados para descrever operações de rede:



- Modelo de referência OSI (Open System Interconnection)
- Modelo de referência TCP/IP



![ProtocolodeRede6.png](/home/felipe/Documentos/Estudo/CiscoCyberOps/Capitulo%205/img/ProtocolodeRede6.png)



### O Modelo de Referência OSI



| **Camada de modelo OSI** | **Descrição**                                                                                                                                                                                                               |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **7 - Aplicação**        | A camada de aplicação contém protocolos usados para comunicações processo a processo.                                                                                                                                       |
| **6 - Apresentação**     | A camada de apresentação fornece a representação comum de dados transferidos entre serviços da camada de aplicação.                                                                                                         |
| **5 - Sessão**           | A camada de sessão fornece serviços à camada de apresentação para organizar o diálogo e gerenciar a troca de dados.                                                                                                         |
| **4 - Transporte**       | A camada de transporte define serviços para segmentar, transferir e <br>reagrupar os dados para comunicações individuais entre os dispositivos <br>finais.                                                                  |
| **3 - Rede**             | A camada de rede fornece serviços para trocar partes individuais de dados na rede entre dispositivos finais identificados.                                                                                                  |
| **2 - Link** de dados    | Os protocolos da camada de enlace descrevem métodos para a troca de quadros de dados entre dispositivos em uma mídia comum                                                                                                  |
| **1 - Físico**           | Os protocolos da camada física descrevem os meios mecânicos, elétricos,<br> funcionais e procedimentais para ativar, manter e desativar conexões <br>físicas para uma transmissão de bits de e para um dispositivo de rede. |



**OBS:** As camadas do modelo OSI são mais frequentemente referenciadas pelo número do que pelo nome.



### Modelo de Protocolo TCP/IP



Esse tipo de modelo corresponde à estrutura de um conjunto de protocolos específico. O TCP/IP é um modelo de protocolo porque descreve as funões que ocorrem em cada camada de protocolos dentro da suíte TCP/IP.

- TCP/IP também é usado como um modelo de referência



| **Camada do modelo TCP/IP** | **Descrição**                                                                  |
| --------------------------- | ------------------------------------------------------------------------------ |
| **4 - Aplicação**           | Representa dados para o usuário, além do controle de codificação e de diálogo. |
| **3 - Transporte**          | Permite a comunicação entre vários dispositivos diferentes em redes distintas. |
| **2 - Internet**            | Determina o melhor caminho pela rede.                                          |
| **1 - Acesso à Rede**       | Controla os dispositivos de hardware e o meio físico que formam a rede.        |



As definições do padrão e dos protocolos TCP/IP são discutidas emm um fórum público e definidas em um conjunto publicamente disponível de documentos de solicitação de comentário (RFC) da IETF.



## Encapsulamento de Dados



### Segmentando Mensagens



Uma abordagem ideal é dividir os dados em pedaços menores e mais gerenciáveis para o envio pela rede, pois o envio maciço pode causar problemas como interrupção de outros serviços ou a perda de dados caso a comunicação falhe.

- A segmentação é necessária devido o uso do protocolo TCP/IP para enviar dados em pacotes IP individuais.
  
  - Cada pacote é enviado separadamente.
  
  - Pacotes com segmentos para o mesmo destino poder ser enviador por caminhos diferentes.



A segmentação de mensagens tem dois benefícios principais:



- **Aumenta a velocidade** - como um grande fluxo de dados é segmentado em pacotes, grandes quantidades de dados podem ser enviadas pela rede sem obstruir um link de comunicação. Isso permite que muitas conversas diferentes sejam intercaladas na rede chamada 
  multiplexação.
- **Aumenta a eficiência** - se um único segmento não consegue alcançar seu destino devido a uma falha na rede ou congestionamento da rede, apenas esse segmento precisa ser retransmitido em vez de reenviar todo o fluxo de dados.



### Sequenciamento



Cada segmento de mensagem deve passar por um processo de sequenciamento para garantir que o pacote chegue ao destino correto e possa ser remontado no conteúdo da mensagem original.

- O TCP é responsável por sequenciar os segmentos individuais.



### Unidades de Dados de Protocolo



**Processo de encapsulamento** - Os dados da aplicação são passados pela pilha de protocolos e durante esse processo, para serem transmitidos pelo meio físico da rede, várias informaões de protocolos são adicionadas em cada nível.

- Embora o UDP PDU seja chamado de datagrama, os pacotes IP às vezes também são chamados de datagramas IP.



**Unidade de dados de protocolo (PDU)** - É o formato que uma parte de dados assume em qualuqer camada.



Durante o encapsulamento, cada camada sucessora encapsula a PDU que 
recebe da camada superior de acordo com o protocolo sendo usado.

- Em cada etapa do processo, uma PDU possui um nome diferente para refletir suas novas funções.
  
  - Embora não haja uma convenção sobre a nomenclatura, os PDUs são nomeadas de acordo com os protocolos do conjunto TCP/IP.





![PDU7.png](/home/felipe/Documentos/Estudo/CiscoCyberOps/Capitulo%205/img/PDU7.png)



- **Dados** - Termo genérico para a PDU usada na camada de aplicação

- Segmento - PDU da camada de transporte

- Pacote - PDU da camada de rede

- Quadro - PDU da camada de enlace de dados

- Bits - PDU da camada física usada ao transmitir dados fisicamente pela mídia.



**OBS:** Se o cabeçalho de transporte é TCP, então é um segmento. Se o cabeçalho Transporte é UDP, então é um datagrama.



### Três Endereços



Os protocoos de rede exigem que os endereoçs sejam usado para comunicação de rede.

- O endereço é usado pelo cliente para enviar solicitações e outros dados para um servidor.
  
  - O servidor usa o endereço do cliente para retornar os dados solicitados ao cliente que o solicitou



Todas as camadas de transporte OSI, ,rede e link de dados usam endereçamento de alguma forma.



- A camada de transporte usa endereços de protocolo na forma de números de porta para identificar aplicativos de rede que devem manipular dados de cliente e servidor. 

- A camada de rede especifica endereços que identificam as redes às quais os clientes e servidores estão conectados e os próprios clientes e servidores.

- A camada de link de dados especifica os dispositivos na LAN local que devem lidar com quadros de dados. Todos os três endereços são necessários para a comunicação cliente-servidor.



![Camadas8.png](/home/felipe/Documentos/Estudo/CiscoCyberOps/Capitulo%205/img/Camadas8.png)



### Exemplo de encapsulamento



O processo de encapsulamento funciona de cima pra baixo quando os dados estão sendo enviados na rede.

- Em cada camada, as informações da camada superior são consideradas dados encapsulaldos no protocolo.



### Exemplo de desencapsulamento



Esse processo é revertido no host de recebimento e é conhecido como **desencapsulamento**.

- É um processo por um dispositivo receptor para remover um ou mais cabeçalhos de protocolo.
  
  - Os dados são desencapsulados à medida que se movem na pilha em direção à aplicação do usuário final.




