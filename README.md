# BadNet
## Internet RealTime Monitor

O usuário final de internet está sujeito a falhas de comunicação muitas vezes sutis, às vezes momentâneas, mas que podem interromper uma comunicação estabelecida, podendo causar encerramento e/ou atrasos em um processo importante, como: envio de arquivos, comunicação com órgãos públicos, consumo de APIs, etc.

**Sob alguns aspectos, a aplicação proposta pode:**
- Aspecto 1: informar ao usuário que detectou problemas de comunicação com a internet, ainda que sutis.
Cenário onde já foi confirmado que **não** houve falha de comunicação com roteador/gateway.

- Aspecto 2: informar ao usuário que detectou problemas de comunicação com o roteador/gateway;
Cenário onde já foi confirmado que **não** houve interrupção do sinal de rede (cabo desconectado, por exemplo)

- Aspecto 3: informar ao usuário que detectou problemas de comunicação com um terceiro host. 

- Aspecto 4: informar ao usuário que detectou problemas de comunicação (ainda que sutis) em nível de hardware.
Indício de problemas no adaptador de rede ou cabo desconectado, por exemplo.

###### O **BadNet** pode trazer informações de:
- estatísticas de **estabilidade** de conexão, comparativas , inclusive, com outros usuários possuidores de conexões semelhantes (provedor, região, etc);
- amostragem de qualidade da conexão (falhas ou estabilidade) em um intervalo de horas;
- identificação do nó com falha, facilitando o diagnóstico e correção até mesmo pelo usuário final.

###### Resultados:
Diante dessas condições, o **BadNet** torna-se útil para identificar em qual nó pode estrar a falha:

1. Nível 1 de falha: 
Somente a internet apresenta falhas. Outros indicadores estão alcancáveis e estáveis?

###### Falha HOST ↔ Internet: PODE haver problemas entre o host e (um, mais de um, ou todos): 
a) internet ou com o provedor de internet;
b) roteador/gateway (validar HOST ↔ roteador/gateway);
c) switch (validar HOST ↔ terceiro terminal);
d) adaptador de rede ou conexão wifi (validação específica de hardware). 

2. Nível 2 de falha: 
O roteador ou gateway apresenta falhas. Outros indicadores abaixo da internet estão alcancáveis e estáveis?

###### Falha HOST ↔ Roteador/gateway: PODE haver problemas (um, mais de um, ou todos):
a) no roteador/gateway;
b) no switch (validar HOST ↔ terceiro terminal);
c) adaptador de rede ou conexão wifi (validação específica de hardware).

3. Nível 3 de falha: 
A comunicação com o terceiro terminal falhas. Outros indicadores abaixo do roteador/gateway estão alcancáveis e estáveis?

###### Falha HOST ↔ Terceiro terminal: PODE haver problemas (um, mais de um, ou todos):
a) no switch (validar HOST ↔ terceiro terminal);
b) adaptador de rede ou conexão wifi (validação específica de hardware).

4. Nível 4 de falha: 
Não há comunicação alguma. 
Problemas com adaptador de rede? Wifi desconectada? Cabo desconectado?

###### Falha de hardware ou conexão wifi
a) problema local, inerente ao próprio host.

A partir do diagnóstico, ações podem ser sugeridas, baseado em configurações realizadas previamente, pelo usuário, por **exemplo**:

**Usuário configurou local físico do roteador/gateway, adicionou foto do local.**
Uma ação poderia ser, caso tenha sido diagnosticado problemas no roteador/gateway:
1. Dirija-se à sala 5-CPD, rack 3, bandeja 1 proceda:
    - garanta que o roteador esteja ligado: verifique luzes dele e de outros dispositivos próximos, se há energia na tomada onde ele está conectado, etc.;
    - desligue o roteador, aguarde 10 segundos e ligue-o novamente. Aguarde cerca de 2 minutos para testar sua internet;
    - verifique se os cabos de rede estão bem firmes, nas duas extremidades.
Caso não consiga identificar, reporte o problema ao administrador da rede.
