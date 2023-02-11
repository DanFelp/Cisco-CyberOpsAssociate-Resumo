## Módulo 2 - Soldados na guerra contra o crime digital

### Objetivo desse módulo é explicar como se preparar para uma carreira em operações de segurança cibernética.

* SOC - Oferece desde monitoramento e gerenciamento até soluções abrangentes de segurança personalizada.
  * Pode ser interno ou contratado por fornecedores de segurança.

#### Pessoas no SOC

* Analista de alerta 1 - Monitora alerta recebido e envia para o nível 2
* Respondente a incidentes de nível 2 - Investigação aprofundada e aconselha a correção ou ação a ser tomada
* Caçador de ameaças de nível 3 - Habilidades de nível especializado em rede, endpoint, inteligência e engenharia reversa.
  * Busca de ameaças e detecção no sistema.
* Gerente de SOC - Gerencia todos os recursos do SOC.

#### Processo no SOC

* Um sistema de emissão de tíquetes é frequentemente usado para atribuir alertas a uma fila para que um analista investigue.
* O analista verifica se o alerta é verdadeiro ou falso.
* Quando a verificação for estabelecida, o incidente pode ser encaminhado aos investigadores ou outro pessoal para ser tratado.
  * Caso não, será descartado como um alarme falso.

Se o ticket não puder ser resolvido, será encaminhado para um analista de incidente nivel 2, se este também não puder resolver, será encaminhado para o pessoal do nível 3



![image-20230210115618633]([Cisco-CyberOpsAssociate-Resumo/CyberOps/Módulo 02/img/image-20230210115618633.png](https://github.com/DanFelp/Cisco-CyberOpsAssociate-Resumo/blob/main/M%C3%B3dulo%2002/img/image-20230210115618633.png))



### Tecnologias no SOC: SIEM

* **SIEM** - Security Information and Event Management System (sistema de gerenciamento de eventos e informações de segurança)
  * O SIEM recebe dados gerados por firewalls, dispositivos de rede, sistemas de detecção de intrusões e outros dispositivos
  * Os sistemas de SIEM são usados para coletar e filtrar dados, detectar e classificar ameaças e analisar e investigar ameaças.
    * Coleta, correção e análise de eventos
    * Monitoramento de segurança
    * Controle de Segurança
    * Gerenciamento de logs
    * Avaliação de vulnerabilidade
    * Controle de vulnerabilidades
    * Inteligência de ameaças

![image-20230210115959724](Cisco-CyberOpsAssociate-Resumo\CyberOps\Módulo 02\img\image-20230210115959724.png)



### Tecnologias no SOC: SOAR

SIEM e orquestração de segurança, automação e resposta (SOAR) normalmente são colocados juntos pois possuem ferramentas que se complementam.

* SecOps utilizam ambas ferramentas para otimizar o SOC.

**SOAR** é integrado com sistema de inteligência contra ameaças e automatiza os fluxos de trabalho e investigação e resposta de incidentes, com base em manuais desenvolvidos pela equipe de segurança.

![image-20230210120249803](Cisco-CyberOpsAssociate-Resumo\CyberOps\Módulo 02\img\image-20230210120249803.png)

Plataformas de segurança SOAR:

* Reunir dados de alarme de cada componente do sistema
* Ferramentas para pesquisar os dados
* Integrar e automatizar fluxos para respostas mais rápidas
* Incluir playbooks predefinidos que permitem a resposta automática a ameaças específicas.



Devido a automação, o SOAR libera a equipe para cuidar de assuntos mais urgentes.



### Métricas SOC



Muitas métricas ou indicadores chave de desempenho (KPI) podem ser projetadas para medir diferentes aspectos específicos do desempenho do SOC.

* Tempo de permanência - 
* Tempo médio para detectar (MTTD) - 
* Tempo médio para responder (MTTR) - 
* Tempo médio para conter (MTTC) - 
* Tempo de controle - 



### Segurança corporativa e gerenciada

A Cisco oferece serviços como:

- Serviço Cisco Smart Net Total Care para Resolução Rápida de Problemas;
- Equipe de resposta a incidentes de segurança do produto (PSIRT) da Cisco;
- Equipe de resposta a incidentes de segurança de computadores da Cisco (CSIRT);
- Serviços Gerenciados Cisco;
- Operações Táticas Cisco (TacOps);
- Programa de Segurança Física e Segurança da Cisco.



### Segurança versus disponibilidade

Cada empresa ou setor tem uma tolerância limitada para o tempo de inatividade da rede.

O tempo de atividade preferencial geralmente é medido no número de minutos de inatividade em um ano

![image-20230210120842455](Cisco-CyberOpsAssociate-Resumo\CyberOps\Módulo 02\img\image-20230210120842455.png)



Deve existir um equilíbrio entre a segurança e a possibilidade dos funcionários trabalharem.
