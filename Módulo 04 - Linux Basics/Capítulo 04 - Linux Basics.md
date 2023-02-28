# Capítulo 04 - Linux Basics

Uma distribuição Linux é o termo usado para descrever pacotes criador por diferentes organizações. Distribuições Linux (ou distros) incluem o kernel Linux com ferramentas personalizadas e pacotes de software.

## O valor do Linux

O SOC geralmente escolhe o Linux, pelos seguintes motivos:



- **Linux é open source** - Qualquer pessoa pode adquirir Linux gratuitamente e modificá-lo para atender a necessidades 
  específicas. Essa flexibilidade permite que analistas e administradores 
  criem um sistema operacional especificamente para análise de segurança.
- **A CLI do Linux é muito poderosa** - Embora uma GUI torne muitas tarefas mais fáceis de executar, ela adiciona complexidade e requer mais recursos de computador para executar. A CLI (Command Line Interface) Linux é extremamente poderosa e permite que os analistas executem tarefas não apenas diretamente em um terminal, mas também remotamente.
- **O usuário tem mais controle sobre o sistema operacional** - O usuário administrador no Linux, conhecido como o usuário root, ou 
  superusuário, tem poder absoluto sobre o computador. Ao contrário de 
  outros sistemas operacionais, o usuário raiz pode modificar qualquer 
  aspecto do computador com algumas teclas pressionadas. Essa capacidade é  especialmente valiosa quando se trabalha com funções de baixo nível, como a pilha de rede. Ele permite que o usuário raiz tenha controle preciso sobre a maneira como os pacotes de rede são manipulados pelo sistema operacional.
- **Ele permite um melhor controle de comunicação de rede** - Controle é uma parte inerente do Linux. Como o sistema operacional pode ser ajustado em praticamente todos os aspectos, é uma ótima plataforma para a criação de aplicativos de rede. Esta é a mesma razão pela qual muitas grandes ferramentas de software baseadas em rede estão disponíveis apenas para Linux.



## ### Linux no SOC



Devido a flexibilidade do Linux, é possível criar um sistema que se encaixe perfeitamente nas necessidades do SOC.



**Security Onion** é um conjunto de ferramentas de código aberto que trabalham juntas para análise de segurança de rede.



Algumas ferramentas normalmente encontradas em SOC:



| **Ferramenta SOC**                                              | **Descrição**                                                                                                                                                                                                                                         |
| --------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Software de captura de pacotes de rede**                      | - Uma ferramenta crucial para um analista de SOC, pois permite observar e entender cada detalhe de uma transação de rede.<br>- Wireshark é uma ferramenta popular de captura de pacotes.                                                              |
| **Ferramentas de análise de malware**                           | Essas<br> ferramentas permitem que os analistas executem e observem com segurança<br> a execução de malware sem o risco de comprometer o sistema subjacente.                                                                                          |
| **Sistemas de detecção de intrusão (IDSs)**                     | - Essas ferramentas são usadas para monitoramento e inspeção de tráfego em tempo real.<br>- Se<br>   qualquer aspecto do tráfego atualmente em fluxo corresponder a qualquer<br>   uma das regras estabelecidas, uma ação predefinida será executada. |
| **Firewalls**                                                   | Este<br> software é usado para especificar, com base em regras predefinidas, se o<br> tráfego tem permissão para entrar ou sair de uma rede ou dispositivo.                                                                                           |
| **Gerenciadores de log**                                        | - Os arquivos de log são usados para registrar eventos.<br>- Como<br>   uma rede pode gerar um número muito grande de entradas de log, o <br>  software do gerenciador de logs é empregado para facilitar o <br>  monitoramento de log.               |
| **Segurança das informações e gerenciamento de eventos (SIEM)** | Os SIEMs fornecem análise em tempo real de alertas e entradas de log geradas por dispositivos de rede, como IDSs e firewalls.                                                                                                                         |
| **Sistemas de emissão de bilhetes**                             | A<br> atribuição de tíquetes de tarefa, edição e gravação é feita através de <br>um sistema de gerenciamento de tíquetes. Os alertas de segurança são <br>frequentemente atribuídos a analistas por meio de um sistema de emissão <br>de bilhetes.    |



### Ferramentas Linux



Computadores linux que são usados no SOC, geralmente contêm ferramentas de teste de penetração. Geradores de pacotes, scanners de porta e exploração de prova de conceito são exemplos de pentesting



**Kali Linux** é uma distribuição Linux que agrupa muitas ferramentas de penetração juntas em uma única distribuição Linux.





## Trabalhando no Linux Shell



### Comandos básicos do Linux



O comando **man** para obter documentação sobre comandos

- Exemmplo "man ls" fornece documentação sobre o ls comando a partir do manual do usuário.



O shell encontra o comando no disco antes de executa-lo. O shell procurará comandos digitados pelo usuário em diretórios específicos e tentará executá-los.

- A lista de diretórios verificados pelo shell é chamada de **caminho**
  
  - O caminho possui muitos diretórios comumente usados para armazenar comandos.

- Se um comando não estiver no caminho, o usuário deve especificar sua localização, ou o shell não será capaz de encontrá-lo. Os usuários podem adicionar facilmente diretórios ao caminho.



| **Comando**   | **Descrição**                                                                                                                                                                                                                                                                                                                        |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **mv**        | Move ou renomeia arquivos e diretórios                                                                                                                                                                                                                                                                                               |
| **chmod**     | Modifica as permissões de arquivos                                                                                                                                                                                                                                                                                                   |
| **chown**     | Altera o dono de um arquivo                                                                                                                                                                                                                                                                                                          |
| **dd**        | Copia os dados de uma entrada para uma saída                                                                                                                                                                                                                                                                                         |
| **pwd**       | Exibe o nome do diretório atual                                                                                                                                                                                                                                                                                                      |
| **ps**        | Lista os processos que estão atualmente em execução no sistema                                                                                                                                                                                                                                                                       |
| **su**        | Simula um login como outro usuário ou para se tornar um superusuário                                                                                                                                                                                                                                                                 |
| **sudo**      | Executa um comando como um superusuário, por padrão, ou outro usuário nomeado                                                                                                                                                                                                                                                        |
| **grep**      | Usado<br> para pesquisar cadeias de caracteres específicas em um arquivo ou <br>outras saídas de comando. Para pesquisar através da saída de um comando <br>anterior, **grep** deve ser canalizado no final do comando anterior.                                                                                                     |
| **ifconfig**  | Usado para exibir ou configurar informações relacionadas à placa de rede. Se emitido sem parâmetros, o **ifconfig** exibirá a configuração atual da (s) placa (s) de rede. Observação: <br>Embora ainda esteja amplamente em uso, esse comando está obsoleto. Use o<br> endereço **IP** em vez disso.                                |
| **apt-obter** | Usado para instalar, configurar e remover pacotes no Debian e seus derivados. Nota: **apt-get** é um front-end de linha de comando amigável para o **dpkg**, o gerenciador de pacotes do Debian. O combo **dpkg** e **apt-get** é o sistema de gerenciador de pacotes padrão em todas as derivadas Debian Linux, incluindo Raspbian. |
| **iwconfig**  | Usado para exibir ou configurar informações relacionadas à placa de rede sem fio. Semelhante ao **ifconfig**, o **iwconfig** exibirá informações sem fio quando emitido sem parâmetros.                                                                                                                                              |
| **shutdown**  | Desliga o sistema, o **desligamento** pode ser instruído a executar uma série de tarefas relacionadas ao <br>encerramento, incluindo reiniciar, parar, colocar em suspensão ou <br>expulsar todos os usuários conectados no momento.                                                                                                 |
| **passwd**    | Usado para alterar a senha. Se nenhum parâmetro for fornecido, **passwd** altera a senha do usuário atual.                                                                                                                                                                                                                           |
| **cat**       | Usado para listar o conteúdo de um arquivo e espera o nome do arquivo como parâmetro. O **comando** cat geralmente é usado em arquivos de texto.                                                                                                                                                                                     |
| **man**       | Usado para exibir a documentação de um comando específico.                                                                                                                                                                                                                                                                           |



### Comandos de arquivo e diretório



Alguns dos comandos mais comuns relacionados a arquivos e diretórios.



| **Comando** | **Descrição**                                                                         |
| ----------- | ------------------------------------------------------------------------------------- |
| **ls**      | Exibe os arquivos dentro de um diretório                                              |
| **cd**      | Muda o diretório atual                                                                |
| **mkdir**   | Cria um diretório no diretório atual                                                  |
| **cp**      | Copia arquivos da origem para o destino                                               |
| **mv**      | Move os arquivos para um diretório diferente                                          |
| **rm**      | Remove arquivos                                                                       |
| **grep**    | Pesquisa cadeias de caracteres específicas em um arquivo ou outras saídas de comandos |
| **cat**     | Lista o conteúdo de um arquivo e espera o nome do arquivo como parâmetro              |



### Trabalhando com Arquivos de Texto



Programas de editor de texto são cruciais no Linux, um exemplo é a necessidade de acesso remoto via SSH onde a interface gráfica não está disponível, dessa forma, a única saída é utilizar um editor de texto para fazer alterações.



### A importância dos arquivos de texto no Linux



No Linux, tudo é tratado como arquivo, isso inclui a memória, os discos, o monitos e os diretórios.



Conhecidos como **arquivos de configuração**, eles geralmente são arquivos de texto usados para armazenar ajustes e configurações para aplicativos ou serviços específicos.



Usuários com níveis de permissão adequados podem utilizar editores de texto para alterar o conteúdo dos arquivos de configuração.



## Servidores e clientes Linux



### Introdução às comunicações Cliente-Servidor



**Servidores** são computadores com software instalado que lhes permite fornecer seviços aos clientes em toda a rede.



Existem muitos tipos de serviços. Alguns fornecem recursos externos, como arquivos, mensagens, e-mails, outros executam tarefas de manutenção, gerenciamento de registro, etc.





![cliente-servidor.png](https://github.com/DanFelp/Cisco-CyberOpsAssociate-Resumo/blob/main/M%C3%B3dulo%2004%20-%20Linux%20Basics/img/cliente-servidor.png)





### Servidores, serviços e suas portas



Para que um omputador possa ser o servidor de vários serviços, as portas são usadas.



Uma **porta** é um recurso de rede reservado por um serviço.



Um servidor está **escutando** em uma porta quando ele se associou a esta porta.



Embora o administrador possa decidir qual porta usar com qual serviço específico, muitos clientes são configurados para usar uma porta específica por padrão.

- É prática comum deixar o serviço em sua porta comum.



Essas são as "portas bem conhecidas" 



| **Porta**   | **Descrição**                                                  |
| ----------- | -------------------------------------------------------------- |
| **20/21**   | File Transfer Protocol (FTP)                                   |
| **22**      | Secure Shell (SSH)                                             |
| **23**      | Serviço de login remoto Telnet                                 |
| **25**      | Protocolo SMTP                                                 |
| **53**      | Domain Name System (DNS)                                       |
| **67/68**   | Protocolo de Configuração Dinâmica de Host (DHCP)              |
| **69**      | Protocolo de Transferência Trivial de Arquivo (TFTP)           |
| **80**      | Protocolo HTTP                                                 |
| **110**     | Protocolo POP3 (Post Office Protocol - Protocolo dos Correios) |
| **123**     | Network Time Protocol (NTP)                                    |
| **143**     | Protocolo IMAP                                                 |
| **161/162** | Protocolo de Gerenciamento Simples de Rede (SNMP)              |
| **443**     | HTTP seguro (HTTPS)                                            |



### Clientes



Os **clientes** são programas ou aplicativos projetados para se comunicar com um tipo específico de servidor.

- Os clientes usam um protocolo bem definido para se comunicar com o servidor



Os navegadores da Web são clientes da Web que são usados para se 
comunicar com servidores Web por meio do Hyper Text Transfer Protocol 
(HTTP) na porta 80.



O cliente FTP (File Transfer Protocol) é um software usado para se comunicar com um servidor FTP.

![Cliente FTP.png](https://github.com/DanFelp/Cisco-CyberOpsAssociate-Resumo/blob/main/M%C3%B3dulo%2004%20-%20Linux%20Basics/img/Cliente%20FTP.png)



## Administração Básica do Servidor



### Arquivos de configuração de serviço



As opções comuns nos arquivos de configuração são o número da porta, a 
localização dos recursos hospedados e os detalhes da autorização do 
cliente.



Quando um serviço é iniciado, ele procura seus arquivos de configuração, carrega-os na memória e se ajusta de acordo com as configurações nos arquivos.

- Modificação do arquivo de configuração geralmente exigem a reinicialização do serviço antes que as alterações entrem em vigor.



Arquivos de configuração exigem superusuario para editar, já que os servioços precisam de privilégio para se executar.



**Nginx** é um servidor web leve para Linux.



Não há regra para um formado de arquivo de configuração; é a escolha do desenvolvedor do serviço.

- No entanto, o formato **option = value** é freqüentemente usado.



### Fortalecimento de Dispositivos (hardering)



O fortalecimento (hardering) do dispositivo envolve a implementação de 
métodos comprovados de proteção do dispositivo e proteção de seu acesso 
administrativo.



Alguns dos métodos envolvem a manutenção de senhas, configuração de recursos avançados e a implementação de login seguro com SSH.



A definição de funções administrativas em termos de acesso é outro aspecto importante da proteção dos dispositivos de infraestrutura, pois nem todo mundo deve ter o mesmo nível de acesso.



Parar serviços habilitados que não são utilizados é outra técnica de fortalecimento do dispositivos.



Também é importante atualizar o sistema.



Práticas para fortalecimento do dispositivo:



- Garantir a segurança física
- Minimizar pacotes instalados
- Desativar serviços não utilizados
- Usar SSH e desabilitar o login da conta raiz por SSH
- Manter o sistema atualizado
- Desativar a detecção automática de USB
- Aplicar senhas fortes
- Forçar mudanças de senha periódicas
- Manter os usuários de reutilizarem senhas antigas



### Logs de serviço de monitoramento



**Arquivos de log** são os registros que um computador armazena para manter o controle de eventos importantes.

- Kernel, serviços e eventos de aplicativos são todos registrados em arquivos de log.



A análise do arquivo de log permite que um administrador proteja contra problemas futuros antes que eles ocorram.



No Linux, os arquivos de log podem ser categorizados como:

- Logs de aplicativos
- Logs de eventos
- Registros de serviço
- Logs do sistema



Alguns logs contêm informações sobre daemons que estão sendo executados no sistema Linux.



Um **daemon** é um processo em segundo plano que é executado sem a necessidade de interação do usuário.

- Por exemplo, o System Security Services Daemon (SSSD) gerencia o acesso remoto e a autenticação para recursos de logon único



Esta é uma lista de alguns arquivos de log populares do Linux e suas funções:



| **Arquivo de log do Linux**                       | **Descrição**                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **/var/log/mensagens**                            | - Este diretório contém logs genéricos de atividade do computador.<br>- Ele é usado principalmente para armazenar mensagens informativas e não críticas do sistema.<br>- Em computadores baseados em Debian, o diretório /var/log/syslog serve a mesma finalidade.                                                                                                                                                                      |
| **/var/log/auth.log**                             | - Este arquivo armazena todos os eventos relacionados à autenticação em computadores Debian e Ubuntu.<br>- Qualquer coisa que envolva o mecanismo de autorização do usuário pode ser encontrada neste arquivo.                                                                                                                                                                                                                          |
| **/var/log/secure**                               | - Este diretório é usado por computadores RedHat e CentOS em vez de /var/log/auth.log.<br>- Ele também rastreia logins sudo, logins SSH e outros erros registrados pelo SSSD.                                                                                                                                                                                                                                                           |
| **/var/log/boot.log**                             | - Este<br>   arquivo armazena informações relacionadas à inicialização e mensagens <br>  registradas durante o processo de inicialização do computador.                                                                                                                                                                                                                                                                                 |
| **/var/log/dmesg**                                | - Este diretório contém mensagens de buffer do anel do kernel.<br>- Informações relacionadas a dispositivos de hardware e seus drivers são registradas aqui.<br>- É<br>   muito importante porque, devido à sua natureza de baixo nível, sistemas<br>   de registro como syslog não estão sendo executados quando esses eventos<br>   ocorrem e, portanto, muitas vezes não estão disponíveis para o <br>  administrador em tempo real. |
| **/var/log/kern.log**                             | - Este arquivo contém informações registradas pelo kernel.                                                                                                                                                                                                                                                                                                                                                                              |
| **/var/log/cron**                                 | - Cron é um serviço usado para agendar tarefas automatizadas no Linux e este diretório armazena seus eventos.<br>- Sempre<br>   que uma tarefa agendada (também chamada de trabalho cron) é executada, <br>  todas as informações relevantes, incluindo status de execução e <br>  mensagens de erro, são armazenadas aqui.                                                                                                             |
| **/var/log/mysqld.log** ou **/var/log/mysql.log** | - Este é o arquivo de log do MySQL.<br>- Todas as mensagens de depuração, falha e sucesso relacionadas ao processo mysqld e ao daemon mysqld_safe são registradas aqui.<br>- As<br>   distribuições RedHat, CentOS e Fedora Linux armazenam logs MySQL em <br>  /var/log/mysqld.log, enquanto Debian e Ubuntu mantêm o log no arquivo <br>  /var/log/mysql.log.                                                                         |



## O sistema de arquivos Linux



### Os tipos de sistema de arquivos no Linux



Essa tabela mostra alguns tipos de sistema de arquivos comumente encontrados e suportados pelo Linux



| **Sistema de arquivos Linux**                               | **Descrição**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **ext2 (segundo sistema de arquivos estendido)**            | - ext2 era o sistema de arquivos padrão em várias distribuições Linux principais até ser suplantado pelo ext3.<br>- Quase totalmente compatível com ext2, ext3 também suporta registro no diário (veja abaixo).<br>- O<br>   ext2 ainda é o sistema de arquivos escolhido para mídia de <br>  armazenamento baseada em flash porque sua falta de diário aumenta o <br>  desempenho e minimiza o número de gravações.<br>- Como os <br>  dispositivos de memória flash têm um número limitado de operações de <br>  gravação, a minimização das operações de gravação aumenta a vida útil do<br>   dispositivo.<br>- No entanto, os kernels Linux contemporâneos <br>  também suportam ext4, um sistema de arquivos ainda mais moderno, com <br>  melhor desempenho e que também pode operar em um modo sem diário. |
| **ext3 (terceiro sistema de arquivos estendido)**           | - ext3 é um sistema de arquivo registrado projetado para melhorar o sistema de arquivo ext2 existente.<br>- Um<br>   diário, o principal recurso adicionado a ext3, é uma técnica usada para<br>   minimizar o risco de danos ao sistema de arquivos no caso de perda <br>  repentina de energia.<br>- Os sistemas de arquivos mantém um registro (ou diário) de todas as alterações do sistema de arquivos prestes a ser feitas.<br>- Se<br>   o computador falhar antes da conclusão da alteração, o diário pode ser <br>  usado para restaurar ou corrigir quaisquer eventuais problemas criados <br>  pela falha.<br>- O tamanho máximo do arquivo em sistemas de arquivos ext3 é 32 TB.                                                                                                                       |
| **ext4 (quarto sistema de arquivos estendido)**             | - Projetado como um sucessor de ext3, ext4 foi criado com base em uma série de extensões para ext3.<br>- Enquanto<br>   as extensões melhoram o desempenho do ext3 e aumentam o tamanho dos <br>  arquivos suportados, os desenvolvedores do kernel Linux estavam <br>  preocupados com problemas de estabilidade e se opuseram a adicionar as <br>  extensões ao ext3 estável.<br>- O projeto ext3 foi dividido em dois;<br>   um mantido como ext3 e seu desenvolvimento normal e o outro, denominado<br>   ext4, incorporou as extensões mencionadas.                                                                                                                                                                                                                                                           |
| **NFS (Network File System)**                               | - NFS é um sistema de arquivos baseado em rede, permitindo acesso a arquivos pela rede.<br>- Do ponto de vista do usuário, não há diferença entre acessar um arquivo armazenado localmente ou em outro computador da rede.<br>- O NFS é um padrão aberto, o que permite que qualquer pessoa o implemente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **CDFS (Compact Disc File System)**                         | O CDFS foi criado especificamente para mídia de disco óptico.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Sistema de troca de arquivos**                            | - O sistema de arquivos de troca é usado pelo Linux quando fica sem RAM.<br>- Tecnicamente,<br>   é uma partição de swap que não tem um sistema de arquivos específico, <br>  mas é relevante para a discussão do sistema de arquivos.<br>- Quando isso acontece, o kernel move o conteúdo inativo da RAM para a partição de troca no disco.<br>- Embora<br>   as partições de permuta (também conhecidas como espaço de permuta) <br>  possam ser úteis para computadores Linux com uma quantidade limitada de <br>  memória, elas não devem ser consideradas como uma solução primária.<br>- A partição de permuta é armazenada no disco que tem velocidades de acesso muito mais baixas do que a RAM.                                                                                                           |
| **HFS Plus ou HFS+ (Sistema de Arquivos Hierárquico Plus)** | - Um sistema de arquivos usado pela Apple em seus computadores Macintosh.<br>- O kernel Linux inclui um módulo para montar HFS+ para operações de leitura-gravação.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **APFS (Sistema de Arquivos Apple)**                        | Um<br> sistema de arquivos atualizado que é usado por dispositivos Apple. Ele <br>fornece criptografia forte e é otimizado para unidades flash e de estado<br> sólido.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Master Boot Record (MBR)**                                | - Localizado<br>   no primeiro setor de um computador particionado, o MBR armazena todas <br>  as informações sobre a forma como o sistema de arquivos é organizado.<br>- O MBR entrega rapidamente o controle a uma função de carregamento, que carrega o sistema operacional.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



**Montagem** é o termo usado para o processo de atribuição de um diretório a uma partição.



Quando emitido sem opções, **mount** retorna a lista de sistemas de arquivos atualmente montados em um computador Linux.



O sistema de arquivos raiz é representado pelo símbulo "/" e contém todos os arquivos no computador por padrão.



Também é mostrado na saída que o sistema de arquivos raiz foi formatado como ext4 e ocupa a primeira partição da primeira unidade (/dev/sda1).



### Funções do Linux e permissões de arquivo



No Linux, a maioria das entidades do sistema são tratadas como arquivos.

- Para organizar o sistema e impor limites dentro do computador, o Linux usa permissões de arquivo.
  
  - As permissõe de arquivo são incorporadas à estrutura do sistema de arquivos e fornecem um mecanismo para definir permissões em cada arquivo.



Cada arquivo no Linux carrega suas pemrissões de arquivo, que definem as suas ações que o proprietário, o grupo e outros podem executar com o arquivo.



Os diretórios de permissão possíveis são: **Ler, Gravar e Executar**

- O comando **ls** com o **-l** parâmetro lista informações adicionais sobre o arquivo.

As permissões de arquivo são sempre exibidas na ordem **Usuário, Grupo e Outro**



Um **link rígido** cria outro arquivo com um nome diferente vinculado ao 
mesmo lugar no sistema de arquivos (chamado de inode). Isso está em 
contraste com um link simbólico, que é discutido na próxima página.



A figura mostra uma divisão das permissões de arquivo no Linux



![PermissoesLinux.png](https://github.com/DanFelp/Cisco-CyberOpsAssociate-Resumo/blob/main/M%C3%B3dulo%2004%20-%20Linux%20Basics/img/PermissoesLinux.png)





É possível utilizar valores octais para definir permissões:



| **Binário** | **Octal** | **Permissão** | **Descrição**            |
| ----------- | --------- | ------------- | ------------------------ |
| 000         | 0         | ---           | Sem acesso               |
| 001         | 1         | --x           | Executar apenas          |
| 010         | 2         | -w-           | Somente escrita          |
| 011         | 3         | -wx           | Edição e execução        |
| 100         | 4         | r--           | Somente leitura          |
| 101         | 5         | r-x           | Ler e Executar           |
| 110         | 6         | rw-           | Leitura e Escrita        |
| 111         | 7         | rwx           | Ler, escrever e executar |



O único usuário que pode substituir a permissão de arquivo em um computador Linux é o usuário root.



Como o usuário root tem o poder de substituir as permissões de arquivo, o usuário root pode gravar em qualquer arquivo.

- Como tudo é tratado como arquivo, o usuário root tem acesso total ao computador linux.



### Links rígisdos e links simbólicos



Um **link rígido** é outro arquivo que aponta para o mesmo local que o arquivo original.

- use o comando **ln** para criar um link rígido.
  
  - O primeiro arguimento é o arquivo existente e o segundo argumento é o novo arquivo.



Ambos os arquivos apontam para o mesmo local no sistema de arquivos. Se você alterar um arquivo, o outro também será alterado.



Um **link simbólico**, também chamado de link simbólico ou link suave, é 
semelhante a um link rígido em que a aplicação de alterações ao link 
simbólico também mudará o arquivo original.



Embora links simbólicos tenham um único ponto de falha (o arquivo 
subjacente), links simbólicos têm vários benefícios sobre links rígidos:



- Localizar links físicos é mais difícil. Links simbólicos mostram a localização do arquivo original no comando **ls -l**, conforme mostrado na última linha de saída no comando anterior. (**mytest.txt -> test.txt**).
  
  
- Links rígidos são limitados ao sistema de arquivos no qual eles são criados. Links simbólicos podem ser vinculados a um arquivo em outro sistema de arquivos.
  
  
- Links rígidos não podem se vincular a um diretório 
  porque o próprio sistema usa links rígidos para definir a hierarquia da 
  estrutura de diretórios. No entanto, links simbólicos podem se vincular a diretórios.



## Trabalhando com a Gui Linux



### Sistema x Window



A interface gráfica presente na maioria dos computadores Linux é baseada no **X Window System.**



O X Window System é um sistema de janelas projetado para fornecer a estrutura básica para uma GUI.

- X inclui funções para desenhar e mover janelas no dispositivo de exibição e interagir com um mouse e teclado.



X funciona como um servidor que permite que um usuário remoto use a rede para se conectar, iniciar um aplicativo gráfico e ter a janela gráfica 
aberta no terminal remoto.

- Enquanto o aplicativo em si é executado no servidor, o aspecto gráfico dele é enviado por X pela rede e exibido no computador remoto.



O X não especifica a interface do usuário, deixa para outros programas definir os componentes gráficos.



## Trabalhando em um host Linux



### Instalação e execuçção de aplicativos em um host Linux



Para ajudar no processo de instalação, o Linux inclui programas chamados **Gerenciadores de pacotes**.

- Um **pacote **é um termo usado para se referir a um programa e todos os seus arquivos de suporte.
  
  - Ao usar um gerenciador de pacotes para instalar um pacote, todos os arquivos necessários são colocados no local correto do sistema de arquivos.



Os gerenciadores de pacotes variam.

- pacman é usado pelo Arch Linux

- dpkg para pacote Debian

- apt são usados em distribuições Debian e Ubuntu Linux.



O comando **apt-get update** é usado para obter a lista de pacotes do repositŕio de pacotes e atualizar o banco de dados de pacotes local

O comando **apt-get upgrade** é usado para atualizar todos os pacotes atualmente instalados para as versões mais recentes.



### Mantendo o sistema atualizado.



A tabela a seguir compara os comandos de distribuição Arch Linux e Debian / Ubuntu Linux para realizar operações básicas do sistema de pacotes.



| **Tarefa**                                      | **Arch**        | **Debian/Ubuntu**          |
| ----------------------------------------------- | --------------- | -------------------------- |
| Instalar um pacote pelo nome                    | **pacman -S**   | **apt install**            |
| Remover um pacote pelo nome                     | **pacman -Rs**  | **apt remover**            |
| Update a local package                          | **pacman -Syy** | **apt-get update**         |
| Atualize todos os pacotes atualmente instalados | **pacman -Syu** | **atualização do apt-get** |



### Processos e Forks



Um **processo** é uma instância em execução de um programa de computador.



**Bifurcação** é um método que o kernel usa para permitir que um processo crie uma cópia de si mesmo.



Os processos precisam de uma maneira de criar novos processos em sistemas operacionais multitarefa.

- A operação bifurcação (fork) é a única maneira de fazer isso no Linux



A bifurcação (fork) é importante por muitos motivos. Um deles está relacionado à escalabilidade do processo.

- Um bom exemplo é o apache, ao se bifurcar, o Apache é capaz de atender a um grande número de solicitações com menos recursos do sistema do que um servidor baseado em processo único.



Quando um processo é bifurcado (fork), o processo do chamador se torna o processo pai, com o processo recém-criado referido como seu filho.

- Depois da bifurcação, os processos são, até certo ponto, processos independentes; eles têm IDs de processo diferentes, mas executam o mesmo código de programa.



A tabela lista três comandos usados para gerenciar processos:



| **Comando**  | **Descrição**                                                                                                                                                                                                                                                                                                                                |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ps**       | - Usado para listar os processos em execução no computador no momento em que é invocado.<br>- Ele pode ser instruído a exibir processos em execução que pertencem ao usuário atual ou a outros usuários.<br>- Embora listar processos não exija privilégios de root, eliminar ou modificar os processos de outros usuários exige.            |
| **superior** | - Usado para listar processos em execução, mas ao contrário do **ps**, **top** continua exibindo processos em execução dinamicamente.<br>- Pressione **q** para sair do topo.                                                                                                                                                                |
| **kill**     | - Usado para modificar o comportamento de um processo específico.<br>- Dependendo dos parâmetros, **kill** removerá, reiniciará ou pausará um processo.<br>- Em muitos casos, o usuário executará **ps** ou **top** antes de executar kill.<br>- Isso é feito para que o usuário possa aprender o PID de um processo antes de executar kill. |



## Malware em um host Linux



Devido a componentes de design, sistemas operacionais Linux são geralmente considerados melhor protegidos contra malware.



Um vetor de ataque Linux comum são seus serviços e processos.

- Uma versão desatualizada do servidor web Apache poderia conter uma vulnerabilidade não corrigida que pode ser explorada.



Os invasores geralmente testam portas abertas para avaliar a versão e a natureza do servidor em execução nessa porta. Com esse conhecimento, os atacantes podem pesquisas se há algum problema conhecido com essa versão específica desse servidor específico para dar suporte ao ataque.

- Atualizar o computador e fechar todos os serviços e portas não utilizados é uma boa maneira de reduzir as oportunidade de ataque em um computador.



### Verificação de Rootkit



Um rootkit é um tipo de malware projetado para aumentar os privilégios 
de um usuário não autorizado ou conceder acesso a partes do software que
 normalmente não devem ser permitidas.

- Rootkits também são frequentemente usados para proteger uma porta traseira para um computador comprometido.



O rootkit pode ser instalado de forma automatizada, ou um invasor pode instala-lo manualmente após comprometer um computador.

- O rootkit é destrutivo pois muda o código do kernel e seus módulos.
  
  - Com um nível tão profundo de comprometimento, os rootkits podem ocultar a intrusão, remover quaiser faixas de instalação e até mesmo adulterar ferramentas de diagnóstico e solução de problemas para que sua saída esconda a presença do rootkit.
    
    - A grande maioria das instalações do rootkit requer privilégio de administrador.



Os métodos de detecção típicos geralmente incluem a inicialização do computador a partir de mídica confiável, como um CD ativo do sistema operacional de diagnóstico.

- A unidade comprometida é montada e ferramentas de diagnóstico confiáveis podem ser iniciadas para inspecionar o sistema de arquivos comprometido.
  
  - Incluem métodos baseados em comportamento, varredura de assinatura, varredura de diferenças e análise de despejo de memória.



A remoção do rootkit muitas das vezes pode ser complicada e até impossível, especialmente quando se está no kernel.

- rootkits de firmware geralmente requerem substituição de hardware.



**chkrootkit **é um programa popular baseado em Linux projetado para verificar o computador em busca de rootkits.

- É um script shell que usa ferramentas comuns do Linux, como **strings** e **grep** para comparar as assinaturas de programas principais. Também procura discrepâncias à medida que atravessa o sistema de arquivos /proc comparando as assinaturas encontradas lá com a saída de **ps**



Embora útil, programas para verificar rootkits não são 100% confiáveis.



### Comandos de piping



Comandos podem ser combinados para executar tarefas mais complexas por uma técnica conhecida como **piping**.



Os comandos ls e grep podem ser usados juntos para filtrar a saída de ls, por exemplo **ls -l | grep host.**








