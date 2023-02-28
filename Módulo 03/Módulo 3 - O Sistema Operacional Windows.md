## Módulo 3 - O Sistema Operacional Windows

### O Objetivo do módulo é explicar os recursos de segurança do sistema operacional Windows.



* Laboratório para identificar processos em execução utilizando o Windows Sysinternals Suite



### Sistema Operacional de Disco



O sistema operacional de disco (DOS) é um sistema operacional que o computador usa para habilitar esses dispositivos de armazenamento de dados para ler e gravar arquivos.

* DOS fornece um sistema de arquivos que organiza os arquivos de uma forma específica no disco. 
  * A microsoft comprou o DOS e criou o MS-DOS

Um sistema operacional moderno como o Windows 10 não é considerado um sistema operacional de disco. Ele é construído no Windows NT, que significa “Novas Tecnologias”. O próprio sistema operacional está no controle direto do computador e seu hardware.

* NT é um sistema operacional com suporte para vários processos de usuário. 
  * Isso é muito diferente do MS-DOS de um único processo e de usuário único.



| **Comando MS-DOS**              | **Descrição**                                                |
| :------------------------------ | :----------------------------------------------------------- |
| **dir**                         | Mostra uma lista de todos os arquivos no diretório atual (pasta) |
| **cd** *diretório*              | Altera o diretório para o diretório indicado                 |
| **cd ..**                       | Muda o diretório para o diretório acima do diretório atual   |
| **cd **\                        | Muda o diretório para o diretório raiz (geralmente C:)       |
| **copy** *fonte de destino*     | Copia arquivos para outro local                              |
| **del** *nome do arquivo*       | Exclui um ou mais arquivos.                                  |
| **find**                        | Procura texto em arquivos                                    |
| **mkdir** *diretório*           | Cria um novo diretório.                                      |
| **ren** *nome_antigo nome_novo* | Renomeia um arquivo                                          |
| **help**                        | Exibe todos os comandos que podem ser usados, com uma breve descrição |
| **help** *comando*              | Exibe a ajuda extensa para o comando indicado                |



## Versões do Windows

A maioria das versões do Windows desde 1993 utilizadas pelo público utiliza o Sistema Operacional NT, devido à segurança de arquivos oferecida pelo sistema.

* A partir do Windows XP, uma edição de 64 bits estava disponível. 
* Quando o sistema operacional e o hardware suportam a operação de 64 bits, conjuntos de dados extremamente grandes podem ser usados. 
  * Esses grandes conjuntos de dados incluem bancos de dados muito grandes, computação científica e manipulação de vídeo digital de alta definição com efeitos especiais.
* Computadores e sistemas operacionais de 64 bits são compatíveis com programas mais antigos de 32 bits, mas programas de 64 bits não podem ser executados em hardware mais antigo de 32 bits.



Versões do Windows:



| **SO**                       | **Versões**                                                  |
| :--------------------------- | :----------------------------------------------------------- |
| **Windows 7**                | Starter, Home Basic, Home Premium, Professional, Enterprise, Ultimate |
| **Windows Server 2008 R2**   | Foundation, Standard, Enterprise, Datacenter, Web Server, HPC Server, Itanium-Based Systems |
| **Windows Home Server 2011** | Nenhum                                                       |
| **Windows 8**                | Windows 8, Windows 8 Pro, Windows 8 Enterprise, Windows RT   |
| **Windows Server 2012**      | Foundation, Essentials, Standard, Datacenter                 |
| **Windows 8.1**              | Windows 8.1, Windows 8.1 Pro, Windows 8.1 Enterprise, Windows RT 8.1 |
| **Windows Server 2012 R2**   | Foundation, Essentials, Standard, Datacenter                 |
| **Windows 10**               | Home, Pro, Pro Education, Enterprise, Education, loT Core, Mobile, Mobile Enterprise |
| **Windows Server 2016**      | Essentials, Standard, Datacenter, Multipoint Premium Server, Storage Server, Hyper-V Server |



## Vulnerabilidades do Sistema Operacional

Uma **vulnerabilidade** é alguma falha ou fraqueza que pode ser explorada por um invasor para reduzir a viabilidade das informações de um computador.

* Para tirar proveito de uma vulnerabilidade do sistema operacional, o invasor deve usar uma técnica ou uma ferramenta para explorar a vulnerabilidade.

Algumas recomendações comuns de Segurança do Windows:

| **Recomendação**                              | **Descrição**                                                |
| :-------------------------------------------- | :----------------------------------------------------------- |
| **Proteção contra vírus ou malware**          | Por padrão, o Windows usa o Windows Defender para proteção contra malware.O Windows Defender fornece um conjunto de ferramentas de proteção incorporadas ao sistema.Se o Windows Defender estiver desativado, o sistema ficará mais vulnerável a ataques e malware. |
| **Serviços desconhecidos ou não gerenciados** | Há muitos serviços que funcionam nos bastidores.É importante certificar-se de que cada serviço é identificável e seguro.Com um serviço desconhecido em execução em segundo plano, o computador pode ficar vulnerável a ataques. |
| **Criptografia**                              | Quando os dados não são criptografados, eles podem ser facilmente coletados e explorados.Isso não é importante apenas para computadores desktop, mas especialmente dispositivos móveis. |
| **Política de segurança**                     | Uma boa política de segurança deve ser configurada e seguida.Muitas configurações no controle de Diretiva de Segurança do Windows podem impedir ataques. |
| **Firewall**                                  | Por padrão, o Windows usa o Firewall do Windows para limitar a comunicação com dispositivos na rede.Com o tempo, as regras podem não se aplicar mais.Por exemplo, uma porta pode ser deixada aberta que não deve mais estar prontamente disponível.É importante revisar periodicamente as configurações do firewall para garantir que as regras ainda são aplicáveis e remover as que não se aplicam mais |
| **Permissões de arquivo e compartilhamento**  | Essas permissões devem ser definidas corretamente. É fácil dar ao grupo “Todos” Controle Total, mas isso permite que todas as pessoas façam o que quiserem a todos os arquivos. É melhor fornecer a cada usuário ou grupo as permissões mínimas necessárias para todos os arquivos e pastas. |
| **Senha fraca ou sem senha**                  | Muitas pessoas escolhem senhas fracas ou não usam nenhuma senha.É especialmente importante certificar-se de que todas as contas, especialmente a conta de Administrador, têm uma senha muito forte. |
| **Login como Administrador**                  | Quando um usuário faz logon como administrador, qualquer programa executado terá os privilégios dessa conta.É melhor fazer login como um Usuário Padrão e usar apenas a senha de administrador para realizar determinadas tarefas. |



## Arquitetura e operações do Windows



### Camada de Abstração de Hardware

![image-20230210125001734](https://github.com/DanFelp/Cisco-CyberOpsAssociate-Resumo/blob/main/M%C3%B3dulo%2003/img/image-20230210125001734.png)



Uma **camada de abstração de hardware (HAL)** é um software que lida com toda a comunicação entre o hardware e o kernel.

O **kernel** é o núcleo do sistema operacional e tem controle sobre todo o computador. 

* Ele lida com todas as solicitações de entrada e saída, memória e todos os periféricos conectados ao computador.

Em alguns casos, o kernel ainda se comunica diretamente com o hardware, portanto não é completamente independente do HAL.

* O HAL também precisa do kernel para executar algumas funções.



### Modo de usuário e modo kernel

Existem dois modos diferentes em que uma CPU opera quando o computador tem o Windows instalado: **o modo de usuário** e o **modo kernel**.

![image-20230210125154280](https://github.com/DanFelp/Cisco-CyberOpsAssociate-Resumo/blob/main/M%C3%B3dulo%2003/img/image-20230210125154280.png)

Os aplicativos instalados são executados no modo de usuário e o código do sistema operacional é executado no modo kernel.

* O código que está sendo executado no modo kernel tem acesso irrestrito ao hardware subjacente e é capaz de executar qualquer instrução de CPU. 
* O código do modo kernel também pode referenciar qualquer endereço de memória diretamente.
  * **Falhas no código em execução no modo kernel param a operação de todo o computador**.



Por outro lado, aplicativos de usuário são executados em modo usuário e não tem contato direto com o hardware ou memória.

* O código do modo usuário passa pelo Sistema Operacional para acessara memória.
* Devido a esse isolamento, falhas no modo usuário são restritas apenas ao aplicativo e são recuperáveis.
  * A maioria dos programas do windows são executados em modo usuário.
    * Drivers são executados em modo kernel ou usuário, dependendo do driver.



Todo o código que é executado no modo kernel usa o mesmo espaço de endereço.

* Os drivers de modo kernel não têm isolamento do sistema operacional.
  * Se ocorrer um erro em um driver em execução no modo kernel e ele gravar no local errado, o sistema operacional ou outro driver pode ser afetado negativamente.
  * O driver pode falhar, fazendo com que todo o sistema operacional falhe.



Quando o código de modo de usuário é executado, ele é concedido seu próprio espaço de endereço restrito pelo kernel, juntamente com um processo criado especificamente para o aplicativo.

* O objetivo é justamente impedir que aplicativos alterem o código do sistema operacional.
* Ao ter seu próprio processo, esse aplicativo tem seu próprio espaço de endereço privado, tornando outros aplicativos incapazes de modificar os dados nele.
  * Isso ajuda evitar que o sistema operacional ou outros aplicativos falhem se o aplicativo falhar.



### Sistema de arquivos do Windows



**Sistema de arquivos** é como a informação é organizada dentro da mídia de armazenamento.



Sistema de arquivos do Windows:

| **Sistema de Arquivos Windows**                 | **Descrição**                                                |
| :---------------------------------------------- | :----------------------------------------------------------- |
| **exFAT**                                       | Este é um sistema de arquivos simples suportado por muitos sistemas operacionais diferentes.O FAT tem limitações para o número de partições, tamanhos de partições e tamanhos de arquivo que pode resolver, portanto, não é mais usado para discos rígidos (HDs) ou unidades de estado sólido (SSDs).Tanto o FAT16 quanto o FAT32 estão disponíveis para uso, sendo o FAT32 o mais comum porque tem muito menos restrições do que o FAT16. |
| **Sistema de Arquivos Hierárquico Plus (HFS+)** | Este sistema de arquivos é usado em computadores MAC OS X e permite nomes de arquivos, tamanhos de arquivo e tamanhos de partição muito mais longos do que os sistemas de arquivos anteriores.Embora não seja suportado pelo Windows sem software especial, o Windows é capaz de ler dados de partições HFS+. |
| **Sistema de arquivos estendido (EXT)**         | Este sistema de arquivos é usado com computadores baseados em Linux.Embora não seja suportado pelo Windows, o Windows é capaz de ler dados de partições EXT com software especial. |
| **New Technology File System (NTFS)**           | Este é o sistema de arquivos mais comumente usado ao instalar o Windows. Todas as versões do Windows e Linux suportam NTFS.Computadores Mac-OS X só podem ler uma partição NTFS. Eles são capazes de gravar em uma partição NTFS depois de instalar drivers especiais. |



O NTFS é o sistema de arquivos mais utilizado para windows

* Suporta arquivos e partições grandes
* Compatível com outros sistemas operacionais
* Confiável e tem suporte a recursos de recuperação
* Suporta muitos recursos de segurança
* O acesso aos dados é obtido através de **descritores de segurança**
  * Esse descritor contém permissões e propriedades do arquivo
* Também controla carimbos de data/hora para controle do arquivo, também chamado de MACE
  * **MACE** > Access, Create e Entry Modified
* Também suporta criptografia.





Antes que um dispositivo de armazenamento possa ser usado, ele deve ser formatado com um sistema de arquivos.

* Antes de ser formatado, precisa ser particionado
  * O disco rígido é dividido em partições.
    * Cada partição é uma unidade lógica de armazenamento
* Normalmente o próprio Sistema operacional já formada com o sistema de arquivos NTFS.



A formatação em NTFS cria estruturas importantes:

* **Setor de inicialização de partição** - Primeiro 16 setores de unidade. Contém o local da tabela de arquivos mestre (MFT). Os últimos 16 setores contêm uma cópia do setor de inicialização.

* **Tabela de arquivos mestre (MFT)**  - Contêm os locais de todos os arquivos e diretórios na partição (carimbo, atributos e informações de segurança)

* **Arquivos de sistema** - Arquivos ocultos com informações sobre valores e atributos

* **Área de arquivo** - Área principal onde os arquivos e diretórios são armazenados.



**OBS:** Ao formatar uma partição, os dados podem ser recuperados, por que nem todos os dados são completamente removidos.

* É importante realizar um apagamento seguro em uma unidade que está sendo reutilizada
  * O **apagamento seguro** grava dados várias vezes em toda unidade para garantir que não há dados restantes.



### Fluxos de dados alternativos



NTFS armazena arquivos como uma série de atributos.

* Os dados que o arquivo possui são armazenados no atributo **$DATA**, conhecido como **fluxo de dados**

* Utilizando NTFS é possível conectar fluxo de dados alternativos (ADSs) ao arquivo.

  * As vezes é utilizado por aplicativos que estão armazenando informações adicionais sobre o arquivo.

  * ADS é um fator importante quando se trata de malwares.

    * Ocorre por ser fácil ocultar dados em um ADS

    * Um invasor pode armazenar dados dentro de um ADS que pode ser chamado por um arquivo diferente.

      

* Em um NFTS, um arquivo ADS é identificado por ADS após dois pontos: Testfile.txt:ADS



### Processo de Inicialização do Windows



Processo de inicialização do windows:



![image-20230210153217181](https://github.com/DanFelp/Cisco-CyberOpsAssociate-Resumo/blob/main/M%C3%B3dulo%2003/img/image-20230210153217181.png)



Existem dois tipos de firmware de computador:

* **Sistema básico de entrada-saída (BIOS)** - Criado no início da década de 1980, já nao suporta todos os novos recursos solicitados pelos usuários.
* **UEFI (Unified Extensible Firmware Interface)** - Projetado para substituir a BIOS e suportar novos recursos

Na BIOS, o processo começa com a fase de inicialização da BIOS

* Ocorre quando os dispositivos são inicializados e um POST (Power On Self-Test) é executado para garantir que todos os dispositivos estejam se comunicando.
  * Quando o disco do sistema é descoberto, o POST termina.
  * A última instrução do POST é procurar o registro mestre de inicialização (MBR)
* A MBR possui um programa responsável por localizar e carregar o Sistema Operacional



O firmware UEFI tem mais visibilidade sobre o processo de inicialização.

* Começa carregando arquivos de programa EFI, armazenados como arquivos.efi em uma partição de disco especial, conhecida como EFI System Partition (ESP).

**Nota**: Um computador que usa UEFI armazena o código de inicialização no firmware.

* Ajuda a aumentar a segurança do computador pois o computador entra em modo protegido



Depois que uma instalação válida do Windows é detectada o arquivo **Bootmgr.exe** é executado.

* **Bootmgr.exe** alterna o sistema do modo real para o modo protegido para que toda a memória do sistema possa ser usada.
* **Bootmgr.exe** lê o Banco de Dados de Configuração de Inicialização (BCD).
  * O BCD contém qualquer código adicional necessário para iniciar o computador, bem como informa se o computador está saindo de hibernação ou arranque frio.
  * Se o computador estiver saindo da hibernação, o processo de inicialização continuará com **Winresume.exe**.
    * Isso permite que o computador leia o arquivo **Hiberfil.sys** que contém o estado em que o computador parou.
  * Se for início frio, o arquivo **Winload.exe** será carregado.
    * O arquivo **Winload.exe** cria um registro da configuração de hardware no registro.
      * O registro é um registro de todas as configurações, opções, hardware e software do computador.
    * **Winload.exe** também usa o Kernel Mode Code Signing (KMCS) para garantir que todos os drivers sejam assinados digitalmente.
      * Isso garante que os drivers sejam seguros para iniciar.



Depois que os drivers forem examinados, o winload.exe executado, Ntoskrnl.exe iniciado o kernel, o subsistema do Gestor de Sessões (SMSS) lê o registo para criar o ambiente do utilizador, iniciar o serviço Winlogon e preparar a área de trabalho.



### Inicialização do Windows



Há dois itens importantes em registro utilizados para iniciar automaticamente aplicativos e serviços:

* **HKEY\ _LOCAL\ _MACHINE** - configurações do Windows, incluindo informações sobre serviços que começar na inicialização.
* **HKEY\ _CURRENT\ _USER** - Aspectos do usuário conectado, incluindo serviços que só iniciar com o logon.



Entradas diferentes informam como os serviços e aplicativos serão iniciados.

* Esses tipos incluem Run, RunOnce, RunServices, RunServicesOnce e Userinit.
  * Essas entradas podem ser inseridas manualmente mas é melhor utilizar o **msconfig.exe**
    * Essa ferramenta é usada para alterar as opções de inicialização do PC.
      * Existem 5 guias: 
        * Geral
        * Inicialização do Sistema
        * Serviços
        * Startup



### Desligamento do Windows



O computador precisa de tempo para fechar cada aplicativo, desligar cada serviço e registrar quaisquer alterações de configuração antes de qualquer desligamento, para não perder as configuraçções de serviços e aplicativos.



No desligamento, primeiro são fechados os programas do usuário, seguido pelo kernel.

* Se as aplicações do modo usuário demorarem, aparecerá uma janela para aguardar ou forçar encerramento.
* Se as aplicações do kernel não responderem, o desligamento irá travar e talvez será necessário desligar o computador no botão.



O Windows pode ser desligado com o comando **shutdown** ou pelo **Ctrl+Alt+Delete**



### Processos, Threads e Serviços

Processo** - É qualquer programa em execução no momento.

- Cada processo que é executado é composto de pelo menos uma **Thread**
  
  - Uma **Thread** é uma parte do processo que pode ser executado.
  - O **Procesador** executa cálculos na thread.
    - Todos os threads dedicados a m processo estão contidos no mesmo espaço de endereço.
      - Essas therads podem não acessar o espaço de endereço de qualquer outro processo, evitando corrupção de outros processo.

**Serviços** - São programas que são executados em segundo plano para suportar o sistema operacional e as aplicações

## Alocação e identificadores de memória

O computador armazena instruções na RAM até que a CPU os processe.

**Espaço virtual** é o conjunto de endereços virtuais que o processo pode usar.

- O endereço virtual não é o local físico real na memória, mas uma entrada em uma tabela de página que é usada para traduzir o endereço virtual para o físico.
- Windows 32 bits suporta endereço virtual de até 4 gigabytes
- Windows 64 bits suporta endereço virtual até 8 terabytes.

Cada processo de espaço do usuário é executado em um espaço de endereço privado, separado dos outros usuários.

- Quando o processo precisa acessar rercursos do kernel, deve usar um **identificado de processo**
  
  - O processo de espaço do usuário nao tem permissão para acessar diretamente os recursos do kernel.
    - O identificador do processo fornece acesso necessário para o processo de espaço do usuário sem uma conexão direta com mele.

**RRAMMap** é uma ferramenta poderosa para visualizar alocação de memória

- Faz parte do Windows Sysinternals.

## Registro do Windows

**Registro** É onde o Windows armazena todas as informações sobre hardware, aplicativos, usuários e configurações do sistema.

- O registro é um banco de dados hierárquico onde o nível mais alto é conhecido como um **ramo**

Os valores armazenam dados e são armazenados nas chaves e subchaves.

- Uma chave de registro pode ter até 512 níveis de profundidade.

| **Seção (Hive) do Registro** | **Descrição** |
| --- | --- |
| **HKEY_CURRENT_USER (HKCU)** | Contém informações sobre o usuário conectado no momento. |
| **HKEY_USERS (HKU)** | Contém informações relativas a todas as contas de usuário no host. |
| **HKEY_CLASSES_ROOT (HKCR**) | Contém informações sobre registros OLE (vinculação e incorporação de objetos). OLE permite que os usuários incorporem objetos de outros aplicativos (como uma planilha) em um único documento (como um documento do Word). |
| **HKEY_LOCAL_MACHINE (HKLM)** | Contém informações relacionadas ao sistema. |
| **HKEY_CURRENT_CONFIG (HKCC)** | Contém informações sobre o perfil de hardware atual. |

A ferramenta **regedit.exe** é usada para modificar o registro.

- A barra invertida (\ ) é usada para diferenciar a hierarquia do banco de dados.
  

As chaves do Registro podem conter uma subchave ou um valor.

- **REG\ _BINARY** - Números ou valores booleanos
- **REG\ _DWORD** - Números maiores que 32 bits ou dados brutos
- **REG\ _SZ** - Valores de cadeia

É importante revisar os locais de inicialização do aplicativo no rergistro para garantir que cada item seja conhecido e seguro para ser executado.

No registro também é possível ver as atividades que um usuário executa durante o uso diário norma do computador.

- Histório de dispositivos de hardware, quais usuários abriram algum programa.
  

## Configuração e monitoramento do Windows

### Executado como Administrador

Pode ser executado como usuário administrador ou pelo prompt de comando como administrador, através da linha de código.

### Usuários e Domínios Locais.

O usuário local contém todas as configurações e personalizações, permissões de acesso, locais de arquivo, dentre outros. Há também duas ourtas contas presentes, o convidado e o administrador. Ambas são desativadas por padrão.

- A conta convidado não deve ser ativada, pois não possui senha associada, toda vez que essa conta é iniciada, um ambiente padrão é fornecido a ele com privilégios limitados.
  

Um grupo terá um nome e um conjunto específico de permissões associadas a ele.

- Quando um usuário é colocado em um grupo, as permissões do grupo são dadas a esse usuário.
  
  - Um usuário pode estar em vários grupos diferentes para várias permissões diferentes.
    
- Usuários e grupos locais são gerenciados com o miniaplicativo do lusrmgr.msc painel de controle.
  

O windows também pode usar domínios para definir permissões.

**Domínio** é um tipo de serviçoç de rede onde todos os usuários, grupos, computadores, periféricos e configurações de segurança são armazenados e controlados por um banco de dados.

- Esse banco de dados é armazenado em grupos de computadores chamados de **controladores de domínio (DCs)**
  
  - Cada utilizados e computador no domínio precisa se autenticar contra o controlador de domínio para iniciar sessão e acessar os recurrsos de rede
    
  - As configurações de segurana para cada usuário e cada computador são definidas pelo controlador de domínio para cada sessão.
    
  - Qualquer configuração fornecida pelo controlador de domínio padrão para o computador local ou configuração de conta de usuário.
    
  

### CLI e PowerShell

A interface de linha de comando (CLI) pode ser usada para executar programas, navegar, etc.

Arquivos batch podem ser criados para executar vários comandos sucessivamente.

Para abrir o CLI, basta ir no cmd.exe.

Observações ao usar o CLI:

- Não se diferenciam maiúsculas de minúsculas
  
- O local é separado por barra invertida.
  
- Comandos com opções especiais usam a barra normal para delinear entre o comando e a opção.
  
- é possível usar a tecla tab para completar automaticamente um comando.
  
- O windows mantém um histórico de comandos inseridos durante uma sessão da CLI. seta pra cima e pra baixo.
  
- Para alternar entre dispositivos de armazenamento, digite a letra seguida de dois pontos e pressione enter.
  

O **Power Shell** é um programa integrado no Windows. Pode executar essse comandos:

- **cmdlets** - Esses comandos executam uma ação e retornam uma saída ou objeto para o próximo comando que será executado.
- **Scripts do PowerShell** - São arquivos com uma extensão **.ps1** que contêm comandos do PowerShell executados.
- **Funções do PowerShell** - São partes de código que podem ser referenciadas em um script.

Há quatro níveis de ajuda no Power Shell:

- **get-help** *PS command* - Exibe a ajuda básica para um comando
- **get-help** *PS command*\ [*\ -examples*] - Exibe a ajuda básica para um comando com exemplos
- **get-help** *PS command*\ [*\ -detailed*] - Exibe ajuda detalhada para um comando com exemplos
- **get-help** *PS command*\ [*\ -full*] - Exibe todas as informações de ajuda de um comando com exemplos em maior profundidade

### Instrumentação de Gerenciamento do Windows

**A Instrumentação de Gerenciamento do Windows (WMI)** é usada para gerenciar computadores remotos. É possível monitorar a integridade de computadores, recuperar informações sobre componentes e estatísticas de hardware.

Essas são as quatro guias do WMI:

- **Geral** - Informações resumidas sobre o computador local e o WMI
- **Backup/Restore** - Permite backup manual de estatísticas coletadas pelo WMI
- **Segurança** - Configurações para configurar quem tem acesso a diferentes estatísticas WMI
- **Avançado** - Configurações para configurar o namespace padrão para WMI

Alguns ataques atuais usam o WMI para se conectar a sistemas remotos, modificar o registro e executar comandos.

- Se torna difícil a detecção pois ser tráfego comum, na maioria das vezes, confiável pelos dispositivos de segurança de rede e os comandos WMI geralmente não deixam evidênncias no host remoto.
  
  - O acesso ao WMI deve ser estritamente limitado.
    

### O comando net

O comando **net** é usado na administração e manutenção do sistema operacional.

- O comando net suporta diversos subcomandos que podem ser combinados para saídas específicas.
  
  - Para ver ajuda detalhada sobre qualquer um dos comandos net, digite C:/> net help
    

A seguinte tabela mostra alguns comandos comuns:

| **omando** | **Descrição** |
| --- | --- |
| **net accounts** | Define os requisitos de senha e logon para usuários |
| **net session** | Lista ou desconecta sessões entre um computador e outros computadores na rede |
| **net share** | Cria, remove ou gerencia recursos compartilhados |
| **net start** | Inicia um serviço de rede ou lista os serviços de rede em execução |
| **net stop** | Para um serviço de rede |
| **net use** | Conecta, desconecta e exibe informações sobre recursos de rede compartilhados |
| **net view** | Mostra uma lista de computadores e dispositivos de rede na rede |

### Gerenciador de tarefas e Monitor de recursos

Duas ferramentas importantes para compreender os vários aplicativos, serviços e processos. Fornece informações sobre o desempenho do computador como CPU,, memória e uso de rede.

**Gerenciador de tarefas** fornece informações de software e desempenho geral do computador.

| **Guias do gerenciador de tarefas** | **Descrição** |
| --- | --- |
| **Processos** | - Lista todos os programas e processos que estão em execução no momento.<br>- Exibe a utilização da CPU, da memória, do disco e da rede de cada processo.<br>- As<br> propriedades de um processo podem ser examinadas ou encerradas se ele <br> não estiver se comportando corretamente ou tiver parado. |
| **Desempenho** | - Uma exibição de todas as estatísticas de desempenho fornece uma visão geral útil do desempenho da CPU, memória, disco e rede.<br>- Clicar em cada item no painel esquerdo irá mostrar estatísticas detalhadas desse item no painel direito. |
| **Histórico de aplicativos** | - O<br> uso de recursos por aplicativo ao longo do tempo fornece informações <br> sobre aplicativos que estão consumindo mais recursos do que deveriam.<br>- Clique em **Opções** e **Mostrar histórico de todos os processos** para ver o histórico de todos os processos executados desde que o computador foi iniciado. |
| **Inicializar** | - Todos os aplicativos e serviços que iniciam quando o computador é inicializado são mostrados nesta guia.<br>- Para desativar o início de um programa na inicialização, **clique com** o botão direito do mouse no item e escolha **Desativar**. |
| **Usuários** | - Todos os usuários que estão conectados ao computador são mostrados nesta guia.<br>- Também são mostrados todos os recursos que os aplicativos e processos de cada usuário estão usando.<br>- Nesta guia, um administrador pode desconectar um usuário do computador. |
| **Detalhes** | - Semelhante<br> à guia Processos, essa guia fornece opções de gerenciamento adicionais <br> para processos, como definir uma prioridade para que o processador <br> dedique mais ou menos tempo a um processo.<br>- A afinidade da CPU também pode ser definida, o que determina qual núcleo ou CPU um programa usará.<br>- Além<br> disso, um recurso útil chamado Analisar cadeia de espera mostra <br> qualquer processo para o qual outro processo está aguardando.<br>- Esse recurso ajuda a determinar se um processo está simplesmente aguardando ou está parado. |
| **Serviços** | - Todos os serviços que são carregados são mostrados nesta guia.<br>- O ID do processo (PID) e uma breve descrição também são mostrados juntamente com o status de Executando ou Parado.<br>- Na parte inferior, há um botão para abrir o console Serviços que fornece gerenciamento adicional de serviços. |

**Monitor de Recursos** é usado para informações mais detalhadas. Segue as cinco guias do monitor de recursos:

| **Guias do Monitor de Recursos** | **Descrição** |
| --- | --- |
| **Visão geral** | - A guia exibe o uso geral de cada recurso.<br>- Se você selecionar um único processo, ele será filtrado em todas as guias para mostrar somente as estatísticas desse processo. |
| --- | --- |
| **CPU** | - O PID, o número de threads, qual CPU o processo está usando e o uso médio da CPU de cada processo é mostrado.<br>- Informações<br> adicionais sobre quaisquer serviços em que o processo se baseia e os <br> identificadores e módulos associados podem ser vistas expandindo as <br> linhas inferiores. |
| **Memória** | - Todas as informações estatísticas sobre como cada processo usa memória são mostradas nesta guia.<br>- Além disso, uma visão geral do uso de toda a RAM é mostrada abaixo da linha Processos. |
| **Disco** | Todos<br> os processos que estão usando um disco são mostrados nesta guia, com <br>estatísticas de leitura/gravação e uma visão geral de cada dispositivo <br>de armazenamento. |
| **Rede** | - Todos os processos que estão usando a rede são mostrados nesta guia, com estatísticas de leitura/gravação.<br>- Mais importante ainda, as conexões TCP atuais são mostradas, juntamente com todas as portas que estão escutando.<br>- Esta guia é muito útil ao tentar determinar quais aplicativos e processos estão se comunicando pela rede.<br>- Permite<br> saber se um processo não autorizado está acessando a rede, ouvindo uma <br> comunicação e o endereço com o qual está se comunicando. |

### Redes

Use o **Centro de Rede e Compartilhamento** para verificar ou criar conexões de rede, configurar o compartilhamento de rede e alterar as configurações do adaptador de rede.

Use o comando **nslookup** para testar o DNS. Se o endereçoç for retornado após um teste exemplo nslookup cisco.com, o DNS está funcionando.

Digite **netstat** para ver detalhes das conexões de rede ativas.

### Acessando recursos de rede

Criado pela IBM e a Microsoft, o protocolo **SMB (Server Message Clock)** é utilizado para compartilhar recursos de rede, para acessar arquivos de hosts remotos.

O formado **UNC(Universal Naming Convention)** é usado para se conectar a recursos:

**\\ nome_do_servidor\ nome_do_compartilhamento\arquivo**

- No UNC, nome_do_servidor é o servidor que está hospedando o recurso.
  
  - Pode ser um nome DNS, um nome NetBIOS ou simplesmente um endereço IP.
    
  - O nome do compartilhamento é a raiz da pasta no sistema de arquivos no host remoto
    
  - O arquivo é o recurso que o host local está tentando encontrar.
    
    - O arquivo pode estar mais profundo dentro do sistema de arquivos e essa hierarquia precisa ser indicada.
      

Ao compartilhar recursos na rede, a área do sistema de arquivos que será compartilhada precisará ser identificada.

Controle de acesso pode ser aplicado às pastas para restingir usuários e grupos.

**Compartilhamento administrativo** é identificado pelo $ que é criado pelo próprio Windows, que são compartilhamentos especiais.

- Apenas usuários com privilégios administrativos podem acessas esses compartihamentos.
  
  - A maneira mais facil de se conectar é digitar o UNC do compartilhamento no Explorador de Arquivos do Windows.
    
    - As credenciais precisam ser do computador remoto, e não do local.
      
- Também é possível fazer login no host remoto para manipular o computador
  
  - No Windows, utiliza-se o protocolo RDP
    

Como o RDP permite controlar hosts individuais, é um alvo natural para os atores de ameaças.

    Deve-se ter cuidado para limitar a exposição do RDP à internet, e abordagens de segurança e políticas de controle de acesso, como Zero Trust.

## Servidor Windows

Esses são alguns serviços que o Windows Server oferece:

- **Serviços de Rede** - DNS, DHCP, Serviços de Terminal, Controlador de Rede e Virtualização de Rede Hyper-V
- **Serviços de Arquivo** - SMB, NFS e DFS
- **Serviços Web** - FTP, HTTP e HTTPS
- **Gerenciamento** - Diretiva de grupo e controle de serviços de domínio do Active Directory

## Segurança do Windows

### O Comando netstat

O comando **netstat** pode ser usado para procurar conexões de entrada ou saída que não estão autorizadas.

- Usado por conta própria, irá exibir todas as conexões TCP ativas.
  
  - Examinando essas conexões é possível determinar quais programas estão escutando conexões que não estão autorizadas.
    

Para facilitar o processo, é possível vincular as conexões aos processos em execução que as criaram no Gerenciador de Tarefas.

- Basta digitar **netstat -abno** no prompt de comando, com privilégios administrativos.
  
  - É necessário examinar para detectar se há algum programa suspeito que esteja escutando conexões de entrada no host.
    
    - Pode haver mais de um processo listado com o mesmo nome, se for o caso, use o **PID** para encontrar o processo correto.
      
      - Botão direito no cabeçalho da tabela e selecione PID
        

### Visualizador de Eventos

O **Visualizador de Eventos do Windows** registra ohistórico de eventos de aplicativos, segurança e sistema.

- Ffornecem informações para identificar um problema.
  

O Windows inclui duas catagorias de logs de eventos:

- Logs do Windows
  
- Logss de Aplicativos e Serviços
  

Os eventos exibidos nesses logs têm um nível: informações, aviso, erro ou crítico. Também possuem data e hora que o evento ocorreu, juntamente com a origem do evento e um ID que se relaciona com o evento.

- É possível criar uma visualização personalizada.
  

Há uma exibição personalizada interna chamada Eventos administrativos que mostra todos os eventos críticos, de erro e de aviso de todos os logs administrativos.

Os logs de eventos de segurança são encontrados em Logs do Windows.

### Configuraões do Windows Update

**Patches** são atualizaões de código que os fabricantes fornecem para evitar que um víus ou worm recém-descoberto façam um ataque bem sucedido.

- Os fabricantes combinam atualizações em um service pack
  

### Ferramenta de Política de Segurança Local

Uma **política de segurança** é um conjunto de objetivos que garante a segurança de uma rede.

- É um documento em constante desenvolvimento, baseado nas mudanças do negócio e nas necessidades dos funcionários.
  

O Active Directory é configurado com domínios em um servidor Windows. Computadores Windows ingressam no domínio. O administrador configura uma Política de Segurança de Domínio que se aplica a todos os computadores que ingressam no domínio.

- As políticas de conta são definidas automaticamente quando um usuário efetua login em um computador que é membro de um domínio.
  

Senhas são importantes e ajudam a confirmar registro de eventos.

- A política de senha é encontrada em Políticas de Conta.
  
  - Use a Diretiva de Bloqueio de Conta em Diretiva de Conta para impedir tentativas de login por força bruta
    
- A política também pode defirnir um tempo para bloquear o PC apartir de quando a proteção de tela for iniciada.
  
- Se a política de seguranaç local em cada PC for a mesma, basta utilizar o recurso de Exportar política
  

O miniaplicativo Diretiva de Segurança Local contém muitas outras configurações de segurança que se aplicam ao computador local

- É possível configurar Direitos de Usuário, Regras de Firewall e até capacidade para restringir os arquivos que os usuários ou grupos têm permissão para executar com o AppLocker.
  

### Windows Defender

Alguns tipos de proteção:

- **Proteção antivírus** - Este programa monitora 
  continuamente a existência de vírus. Quando um vírus é detectado, o 
  usuário é avisado e o programa tenta colocar o vírus em quarentena ou 
  excluí-lo.
- **Proteção de adware** - Este programa procura continuamente programas que exibem anúncios em seu computador.
- **Proteção contra phishing** - este programa bloqueia os endereços IP de sites de phishing conhecidos e avisa o usuário sobre sites suspeitos.
- **Proteção contra spyware** - este programa verifica a existência de keyloggers e outros spywares.
- **Fontes confiáveis / não confiáveis** - Este programa avisa sobre programas inseguros prestes a serem instalados ou sites inseguros antes de serem visitados.

### Firewall do Windows Defender

O **Firewall** nega, seletivamentem o tráfego a um computador ou a um segmento de rede. Os firewall trabalham abrindo e fechando as portas usasdas por vários aplicativos.

- Ao abrir apenas portas necessárias em um firewall, será aplicada uma política de segurança restritiva.
  
  - Qualquer pacote não explicitamente permitido é negado.
    
- Uma política de segurança permissiva permite acesso por todas as portas, exceto aquelas explicitamente negadas.
