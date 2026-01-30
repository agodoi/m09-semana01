# Introdução às Redes de Computadores

Nessa instrução, você verá teorias importantes para evitar o hardware hacking e boas práticas de montagem de cabo que garantem estabilidade na comunicação de sistemas, evitando brechas de ataques como engenharia social do falso técnico.

Hardware hacking é o processo de modificar ou explorar dispositivos físicos para alterar sua funcionalidade, ampliar seu uso ou explorar vulnerabilidades. 

Isso pode incluir desmontar dispositivos, reprogramar componentes, explorar falhas ou interfaces mal protegidas, ou criar novos usos para um hardware existente. 

Os hackers de hardware podem realizar essas modificações para fins legítimos, como personalizar ou consertar dispositivos, mas também podem buscar explorar brechas para comprometer a segurança de um sistema, como em ataques a dispositivos de IoT ou sistemas embarcados. 

Em cibersegurança, o hardware hacking pode ser uma técnica usada para demonstrar vulnerabilidades em dispositivos físicos, ajudando a melhorar a proteção dos sistemas contra ameaças.

É sobre essa melhoria na proteção que vamos explorar hoje.

## (1) Topologias de Rede

Topologia de Rede é a maneira como os elementos de uma rede estão organizados e interligados. Ela pode ser classificada em duas categorias: **topologia física** e **topologia lógica**. 

### (1.1) Topologia Física

A **topologia física** se refere à disposição real e física dos cabos, dispositivos e outros componentes da rede. É a maneira como os cabos e equipamentos, como switches e roteadores, estão fisicamente conectados uns aos outros. Os hosts podem ser organizados em algum tipo de topologia a seguir:

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/SubRedes/blob/main/imgs/network-topology.png">
   <img alt="Topologias de Redes" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/SubRedes/blob/main/imgs/network-topology.png)">
</picture>

Para o padrão Ethernet, adota-se **Estrela** que também pode ser estendido para **Estrela Estendida** quando uma estrela dá origem para outra estrela.

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/SubRedes/blob/main/imgs/estrela_extendida.png">
   <img alt="Estrela Estendida" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/SubRedes/blob/main/imgs/estrela_extendida.png)">
</picture>

#### [SÁBADO] Montaremos essa topologia no Packet Tracer.

### (1.2) Topologia Lógica

A **topologia lógica** descreve como os dados se movem dentro da rede, ou seja, o caminho que as informações seguem independentemente da disposição física dos cabos e dispositivos. O fluxo de dados entre os dispositivos, que nem sempre segue a topologia física. Por exemplo, em uma rede fisicamente em estrela, os dados podem se comportar como se estivessem em uma topologia em barramento, dependendo de como os pacotes de dados são transmitidos entre os dispositivos.

---

## (2) Tipos de Meios de Transmissão

   Os meios de transmissão são os canais pelos quais os dados se movem de um dispositivo para outro em uma rede. Eles podem ser classificados em três grandes categorias: par metálico, óptico e eletromagnético. Cada um desses meios tem características próprias que influenciam sua velocidade, capacidade e alcance.

### (2.1) Par metálico

   O **par metálico** é um dos meios mais comuns e tradicionais usados para transmissão de dados, especialmente em redes locais e de telefonia. Ele utiliza cabos de cobre ou outro material metálico condutor para transmitir sinais elétricos. Existem dois tipos principais:

* Cabo coaxial: um condutor central de cobre cercado por uma malha metálica, usado principalmente em TV a cabo e redes antigas de dados.
* Cabo de par trançado (UTP/STP): 8 fios de cobre trançados entre si, que ajudam a reduzir interferências eletromagnéticas. Esse é o tipo mais comum em redes de computadores, especialmente em conexões Ethernet.
* Vantagens: baixo custo, facilidade de instalação e flexibilidade.
* Desvantagens: menor alcance e susceptibilidade a interferências em comparação com outros meios.


### (2.2) BOAS PRÁTICAS [SÁBADO-30min] Crimpagem do cabo UTP e Teste

Crimpar um cabo UTP (Unshielded Twisted Pair) Cat 5 exige atenção a alguns detalhes para garantir uma conexão eficiente e estável, livre de problemas, engenharia social e consequentemente, ataques. Sua missão é crimpar um cabo UTP CAT 5 com um conector RJ45 em cada ponta e passar no teste de condutividade. Usar o padrão 568A nas duas pontas. Você também pode optar pelo 568B nas duas pontas. Aqui estão as boas práticas para esse processo:

**a)** Escolha do Cabo e Conectores Corretos
   - Verifique se o cabo é compatível com o padrão Cat 5.
   - Utilize conectores RJ-45 adequados para cabos Cat 5 (ou Cat 5e).
   
**b)** Corte Limpo do Cabo
   - Utilize uma ferramenta de corte para garantir que o cabo seja cortado de forma reta e precisa, evitando fios desalinhados que podem dificultar a conexão.

**c)** Desencape o Cabo Com Cuidado
   - Ao remover a capa externa do cabo, deixe expostos cerca de 2,5 cm (1 polegada) dos pares trançados internos.
   - Não desencape, ou corte ou danifique os fios internos no momento de desencapar a capa externa.

**d)** Desenrolar e Organizar os Fios
   - Separe os pares de fios e os alinhe de acordo com o padrão escolhido (T568A ou T568B).
   - Certifique-se de que os fios estão alinhados e retos antes de inserir no conector.
   - Não desenrole demais os fios; mantenha a torção o mais próximo possível do conector, pois isso ajuda a minimizar interferências.

**e)** Escolha do Padrão Correto
   - Decida entre o padrão **T568A** ou **T568B** e certifique-se de seguir o mesmo padrão em ambas as extremidades do cabo, especialmente se estiver fazendo um cabo patch.
   - As combinações de cores para o padrão T568A são:
     - pino (1) Verde/Branco
     - pino (2) Verde
     - pino (3) Laranja/Branco
     - pino (4) Azul
     - pino (5) Azul/Branco
     - pino (6) Laranja
     - pino (7) Marrom/Branco
     - pino (8) Marrom
   - Para o padrão T568B (mais usado em redes residenciais):
     - pino (1) Laranja/Branco
     - pino (2) Laranja
     - pino (3) Verde/Branco
     - pino (4) Azul
     - pino (5) Azul/Branco
     - pino (6) Verde
     - pino (7) Marrom/Branco
     - pino (8) Marrom

#### Atenção: 

* Cabo Direto: sempre use cabo direto (568A - 568A ou 568B - 568B) quando estiver conectando dispositivos diferentes entre si.

* Cabo Cruzado: sempre use cabo cruzado (568A - 568B) quando estive conentando o mesmo tipo de equipamento.

* Sempre usamos as portas **Fast Ethernet** para conexão do RJ45 + cabo UTP de PC e **Giga Ethernet** para Switches e Roteadores.


**f)** Inserção Correta dos Fios no Conector
   - Certifique-se de que os fios estão perfeitamente alinhados e nivelados antes de inserir no conector RJ-45.
   - Pressione firmemente os fios dentro do conector até que cada um toque seu respectivo pino de metal.
   - O cabo externo (capa) deve estar preso dentro do conector para maior resistência e durabilidade.

**g)** Uso da Ferramenta de Crimpagem
   - Posicione o conector no alicate de crimpagem e aperte firmemente para fixar os contatos metálicos nos fios.
   - Certifique-se de que o conector está totalmente inserido no alicate antes de crimpar para evitar crimpar mal e danificar o conector.

**h)** Teste o Cabo
   - Após crimpar, utilize um **testador de cabos** para garantir que todos os fios estão corretamente conectados e o cabo está funcionando corretamente.
   - Verifique se todos os pares estão funcionando e se não há fios cruzados ou mal conectados.

---

### (2.3) BOAS PRÁTICA [SÁBADO-20min] Emendas de Cabos de Dados

Fazer emendas de cabos coaxiais exige cuidado para garantir que o sinal seja transmitido corretamente, sem ataques, sem perda de qualidade e sem interferência. As boas práticas ao realizar esse tipo de emenda são:

**a)** Utilize Conectores e Ferramentas de Qualidade

   - Use conectores coaxiais de boa qualidade, compatíveis com o tipo de cabo (RG6, RG59, etc.).
   - Ferramentas adequadas, como alicates decapadores e crimpatrizes, são essenciais para garantir uma emenda firme e sem danos ao cabo.

**b)** Corte Limpo e Reto do Cabo

   - Ao cortar o cabo coaxial, utilize uma ferramenta apropriada para garantir que o corte seja reto e uniforme. Alicates cegos deixam rebarbas que podem fechar curto.
   - Um corte torto pode causar problemas de conexão ou dificuldade ao fixar os conectores.

**c)** Desencape o Cabo com Cuidado
 
   - Utilize uma ferramenta decapadora para remover a camada externa do cabo coaxial. É importante remover a quantidade correta da capa + malha sem danificar o condutor central.
   - Deixe expostos o condutor central (fio de cobre ou alumínio).
   - Certifique-se que a malha metálica não está encostando no fio central.
   - Alguns conectores de coaxial exigem que a malha seja preservada dobrando-a cuidadosamente para trás para evitar que entre em contato com o condutor central.

**d)** Não Deixe Exposta a Blindagem
   
   - A malha de proteção e o condutor central nunca devem se tocar, pois isso pode causar curtos-circuitos e perda de sinal.
   - Após desencapar, certifique-se de que a malha está dobrada e organizada, e o condutor central está isolado.

**e)** Use Conectores F (ou outros conectores apropriados)
   
   - Utilize conectores F, BNC ou outros apropriados para o tipo de cabo coaxial que está sendo utilizado. Os conectores devem ser crimpos ou rosqueados corretamente para garantir boa conexão.
   - Conectores F exigem que o condutor central passe pelo orifício no centro do conector, e a malha fique em contato com o corpo metálico do conector para fazer a blindagem adequada.

**f)** Uso de Adaptadores de Emenda
   
   - Para emendas diretas entre dois cabos coaxiais, utilize adaptadores de emenda específicos (barril de emenda coaxial). Eles garantem uma emenda estável e minimizam a perda de sinal.
   - Evite emendas improvisadas (como fitas isolantes), que podem prejudicar a qualidade do sinal e a durabilidade da conexão.

**g)** Verificação da Impedância
  
   - Verifique se os conectores e cabos utilizados são compatíveis em termos de impedância. Cabos coaxiais são normalmente de 50 ou 75 ohms, e é importante manter a mesma impedância ao longo de toda a conexão para evitar perda de sinal ou reflexões.

**h)** Dobras e passagens

   - Jamais faça dobras de 90º no cabo coaxial, pois isso danifica internamente a estrutura do material dielétrico que separa o condutor central da malha metálica, causando reflexões do sinal e perdas do dBm.

**i)** Isolamento Adequado

   - Certifique-se de que o condutor central e a malha estão bem isolados para evitar interferências e curto-circuitos.
   - Para isso, use um multímetro na escala ôhmica e um terminal de 75 ohms conectado na outra ponta do cabo coaxial.
   - Após conectar o cabo coaxial em um conector, isole a emenda adequadamente com **fita isolante de autofusão** fazendo uma camada de ida e outra camada de volta partindo do lado do cabo e cobrindo até o conector metálico em um comprimento equivalente a um conector sobre a capa e a emenda. Sobreposição de 50%.
   - Após fazer a camada de ida e volta com a fita de autofusão, faça outra 2 camadas de ida e volta usando fita isolante. Sobreposição de 50%.
   - Finalize a emenda com uma fita tipo Hellerman travando as pontas da fita isolante para não se soltar no calor.
   
**j)** Teste Final da Conexão

 - Após a emenda, teste a qualidade do sinal usando um multimetro e o terminal de carga de 75 ohms. O valor marcado no multímetro deve o mais próximo de 75 ohms.
 - Verifique a integridade da conexão e, se necessário, refaça a crimpagem ou substitua os conectores.

---

### (2.4) Óptico

   O meio óptico utiliza fibras ópticas feitas de vidro ou plástico para transmitir dados por meio de pulsos de luz, em vez de sinais elétricos. A fibra óptica é capaz de transportar grandes quantidades de dados a altas velocidades por longas distâncias com mínima perda de sinal.

* Fibra monomodo: Ideal para transmissões de longa distância, geralmente em WANs, devido à baixa atenuação e alta capacidade.
* Fibra multimodo: Usada em curtas distâncias, como dentro de prédios ou campus, oferecendo também alta capacidade, mas com mais perda de sinal.
* Vantagens: Alta velocidade, grande capacidade de dados e imunidade a interferências eletromagnéticas.
* Desvantagens: custo mais alto e maior complexidade de instalação e manutenção.

---

### (2.5) Eletromagnético

   O meio eletromagnético envolve a transmissão de dados por ondas de rádio, micro-ondas, ou infravermelho através do ar, sem a necessidade de cabos físicos. Esse tipo de transmissão é amplamente utilizado em redes sem fio (wireless).

* Ondas de rádio: usadas em redes Wi-Fi, comunicações de satélite e redes de longa distância (LTE/5G).
* Micro-ondas: usadas para transmissões de longa distância em linhas de visão direta, como em comunicações entre torres de transmissão.
* Infravermelho: Utilizado em comunicações de curta distância, como controles remotos ou em alguns dispositivos IoT.
* Vantagens: flexibilidade e mobilidade, já que não depende de cabos.
* Desvantagens: susceptibilidade a interferências, obstáculos físicos e limitações de alcance e largura de banda.

---

## (3) Antenas

Uma antena é um dispositivo usado para transmitir e receber ondas eletromagnéticas. Ela se comporta como um corpo resistivo numa dada frequência de operação.
   
   * Em termos simples, uma antena transmissora converte um pequeno sinal elétrico que passa em sua estrutra em ondas de rádio.
   * Uma antena receptora, faz o contrário, isto é, detecta uma onda de rádio e tranforma numa pequena corrente elétrica.
   
Qualquer antena recebe ou emite sinais, mas sua eficiência fica melhor se sua estrutura metálica tiver um tamanho proporcional à sua frequência de operação. Por exemplo, antenas Wi-Fi operam em frequências de 2,4 GHz ou 5 GHz e por issom possuem pequenos tamanhos. Antenas de rádio AM e FM operam em frequências baixas menores, e por isso, possuem tamanhos maiores.

---

### 3.1 Antena Dipolo
   
#### Descrição:
A antena dipolo é uma das antenas mais simples e comuns, composta por dois condutores retos alinhados de maneira colinear. Geralmente é utilizada para transmissões em VHF e UHF.

#### Aplicações:
- Radiodifusão (rádio AM/FM)
- Comunicações de rádio e TV
- Redes de comunicação sem fio em curta distância (Wi-Fi)

#### Vantagens:
- Fácil de construir e implementar
- Funciona bem em ambientes de linha de visão
- Custo baixo

#### Desvantagens:
- Ganho relativamente baixo
- Sensível a interferências e ruídos em áreas urbanas

---

### 3.2 **Antena Yagi-Uda**

#### Descrição:
A antena Yagi consiste em um dipolo ativo e uma série de elementos direcionais que melhoram o ganho em uma direção específica. É uma antena direcional bastante utilizada para sinais de TV e rádio.

#### Aplicações:
- Recepção de TV
- Comunicações ponto-a-ponto de rádio
- Sistemas de transmissão e recepção de sinais em VHF e UHF

#### Vantagens:
- Alto ganho direcional
- Boa para distâncias médias e longas em ambientes de linha de visão
- Menor interferência por ser direcional

#### Desvantagens:
- Direcional, requer alinhamento preciso
- Eficiência reduzida fora da linha de visão

---

### 3.3 Antena Parabólica

#### Descrição:
A antena parabólica utiliza uma superfície em formato de prato parabólico para refletir as ondas de rádio em direção a um ponto focal, onde o receptor ou transmissor está localizado.

#### Aplicações:
- Telecomunicações via satélite
- Antenas de televisão por satélite
- Comunicações ponto-a-ponto de longa distância

#### Vantagens:
- Muito alto ganho
- Ótima para comunicações de longa distância
- Direcionalidade precisa, reduzindo interferências

#### Desvantagens:
- Exige alinhamento muito preciso
- Grande tamanho e estrutura complexa
- Funciona melhor apenas em linha de visão

---

### 3.4 Antena Log-Periódica

#### Descrição:
Uma antena log-periódica é composta por vários elementos de tamanhos variáveis dispostos de maneira sequencial. Ela é projetada para operar em uma ampla faixa de frequências.

#### Aplicações:
- Antenas de TV multibanda
- Sistemas de comunicação que exigem múltiplas frequências
- Monitoramento de espectro de rádio

#### Vantagens:
- Larga faixa de frequências
- Direcionalidade moderada
- Boa para situações que exigem flexibilidade de banda

#### Desvantagens:
- Ganho moderado comparado a outras antenas direcionais
- Mais complexa de construir

---

### 3.5 Antena Omnidirecional

#### Descrição:
As antenas omnidirecionais transmitem e recebem sinais em todas as direções no plano horizontal, sendo ideais para cobrir grandes áreas ao redor do ponto de emissão.

#### Aplicações:
- Redes Wi-Fi (roteadores)
- Comunicações móveis (torres de celular)
- Redes de comunicação de curto alcance

#### Vantagens:
- Cobertura ampla em todas as direções
- Ideal para áreas onde os receptores estão distribuídos ao redor da antena
- Fácil instalação e uso

#### Desvantagens:
- Ganho mais baixo comparado às antenas direcionais
- Menos eficiente para comunicações de longa distância

---

### 3.6 Antena de Patch (Microstrip)

#### Descrição:
Antenas de patch, ou microstrip, são compostas por uma pequena superfície metálica plana que emite ou recebe sinais. Elas são comumente integradas a superfícies e são compactas.

#### Aplicações:
- Comunicações via satélite
- Redes móveis e Wi-Fi
- Dispositivos portáteis (antenas embutidas em celulares)

#### Vantagens:
- Muito compacta e leve
- Fácil de integrar em superfícies planas
- Boa para aplicações móveis e portáteis

#### Desvantagens:
- Ganho relativamente baixo
- Faixa de frequência limitada

---

### 3.7 Antena de Loop 

#### Descrição:
Antenas de loop consistem em um fio condutor em formato de círculo ou elipse. Elas podem ser pequenas (loop magnético) ou grandes, dependendo da aplicação.

#### Aplicações:
- Radiodifusão AM
- Comunicações militares e submarinas (loop magnético)
- Monitoramento de espectro de rádio

#### Vantagens:
- Pequeno tamanho para frequências baixas
- Boa resistência à interferência eletromagnética
- Utilizável em ambientes com espaço restrito

#### Desvantagens:
- Ganho menor em comparação com outras antenas
- Direcionalidade limitada

---

### 3.8 Antena Slot

#### Descrição:
A antena slot é uma abertura feita em uma superfície condutora, como uma folha de metal, que irradia sinais de rádio. Ela pode ser usada em várias formas e é aplicada principalmente em micro-ondas.

#### Aplicações:
- Antenas de radar
- Comunicações de micro-ondas
- Sistemas de navegação aérea

#### Vantagens:
- Compacta e discreta
- Boa para frequências de micro-ondas
- Direcionalidade moderada

#### Desvantagens:
- Ganho moderado
- Pode ser complexa de construir para aplicações de alta potência

---

### 3.9 Antena Helicoidal

#### Descrição:
Uma antena helicoidal é formada por um fio enrolado em forma de hélice e é utilizada para frequências que vão desde VHF até micro-ondas.

#### Aplicações:
- Comunicações via satélite
- Antenas para receptores GPS
- Sistemas de transmissão em frequências elevadas

#### Vantagens:
- Boa para frequências elevadas
- Compacta para sua faixa de operação
- Capacidade de operar em polarização circular

#### Desvantagens:
- Ganho relativamente baixo para comunicações de longa distância
- Direcionalidade limitada

---

### 3.10 Antena de Chifre (Horn Antenna)

#### Descrição:
As antenas de chifre utilizam uma abertura em forma de cone para direcionar as ondas de rádio em frequências de micro-ondas. São geralmente usadas em conjunto com guias de onda.

#### Aplicações:
- Radar e radiotelescópios
- Comunicações de micro-ondas
- Medições de campo de antenas

#### Vantagens:
- Alto ganho em frequências de micro-ondas
- Direcionalidade precisa
- Baixa distorção de sinal

#### Desvantagens:
- Grande tamanho físico para operações de alta potência
- Difícil de fabricar e ajustar para frequências mais baixas

---

### (4) Comunicação via Satélite


A comunicação via satélite possui um importante papel nas redes de computadores, especialmente quando se trata de conectar áreas geograficamente dispersas e fornecer cobertura global. 

#### Princípio de Funcionamento da Comunicação via Satélite
A comunicação via satélite envolve a transmissão de sinais de rádio entre estações terrestres e os satélites que orbitam a Terra. Esses satélites recebem, amplificam e retransmitem os sinais de volta para a Terra, permitindo a comunicação entre locais distantes.

#### Componentes principais:
- **Estação transmissora (uplink)**: envia o sinal da Terra para o satélite.
- **Satélite**: recebe o sinal, o amplifica e retransmite para outra região da Terra.
- **Estação receptora (downlink)**: recebe o sinal do satélite e o direciona ao destino final.

#### Orbitas de Satélites
Satélites podem operar em diferentes órbitas, cada uma com suas características, dependendo da aplicação da rede de comunicação.

- **Órbita Geoestacionária (GEO)**: Satélites estão a aproximadamente 36.000 km acima do equador, mantendo uma posição fixa em relação à Terra. Usada principalmente para comunicações de longa distância e televisão por satélite.
  - *Vantagem*: Cobertura contínua de grandes áreas, incluindo a cobertura de continentes inteiros.
  - *Desvantagem*: Latência elevada (cerca de 250 ms no total para subir e descer), o que pode afetar a qualidade em aplicações de tempo real, como videoconferências.

- **Órbita Baixa da Terra (LEO)**: Satélites a altitudes entre 500 e 2.000 km, movendo-se rapidamente em torno da Terra.
  - *Vantagem*: Baixa latência (20-40 ms), ideal para serviços de internet de alta velocidade, como as constelações de satélites Starlink.
  - *Desvantagem*: Cobertura limitada, o que requer uma constelação de satélites para garantir cobertura contínua.

- **Órbita Média da Terra (MEO)**: Satélites entre 2.000 e 36.000 km, usados para comunicações de alcance intermediário.
  - *Vantagem*: Latência moderada (60-80 ms) com cobertura maior que os satélites LEO.
  - *Desvantagem*: Menor cobertura e maior latência que os satélites GEO.

#### Frequências de Operação
A comunicação via satélite utiliza várias bandas de frequência para transmissão, dependendo da aplicação e da distância.

- **Banda C (4-8 GHz)**: Usada principalmente para transmissões de televisão e algumas comunicações de voz.
  - *Vantagem*: Alta resistência a interferências atmosféricas.
  - *Desvantagem*: Necessita de antenas maiores.

- **Banda Ku (12-18 GHz)**: Muito usada para televisão por satélite e internet via satélite.
  - *Vantagem*: Antenas menores e mais acessíveis.
  - *Desvantagem*: Vulnerável a interferências climáticas (chuvas intensas).

- **Banda Ka (26-40 GHz)**: Usada para internet de alta velocidade e novos serviços de satélites.
  - *Vantagem*: Oferece alta largura de banda.
  - *Desvantagem*: Muito sensível à interferência atmosférica, como chuva.

#### Latência e Considerações de Desempenho

A latência é uma questão importante na comunicação via satélite, especialmente em satélites geoestacionários (GEO). Isso se deve à grande distância que os sinais precisam percorrer. Para mitigar esse efeito, satélites de órbitas mais baixas (LEO) estão sendo utilizados para aplicações que exigem baixa latência, como jogos online e videoconferências.

#### Aplicações da Comunicação via Satélite

- **Internet via satélite**: usada em áreas rurais e remotas onde a infraestrutura terrestre de internet é limitada ou inexistente. Exemplos incluem Starlink, HughesNet, e Viasat.
- **Comunicações de emergência**: em desastres naturais ou situações em que a infraestrutura terrestre é destruída, a comunicação via satélite pode fornecer conectividade rápida e eficaz.
- **Transmissões de TV**: a televisão via satélite, como a DirecTV ou a Sky, usa satélites para enviar conteúdo diretamente para os usuários finais.
- **Sistemas de navegação**: o GPS é um exemplo de comunicação via satélite para navegação, permitindo rastreamento e posicionamento em tempo real.

#### Desafios da Comunicação via Satélite

- **Interferência atmosférica**: fenômenos meteorológicos, como chuvas fortes e tempestades, podem afetar a qualidade do sinal, especialmente nas bandas Ku e Ka.
- **Altos custos de lançamento**: colocar satélites em órbita é caro, tanto em termos de lançamento quanto de manutenção.
- **Capacidade limitada**: embora satélites modernos tenham aumentado a largura de banda disponível, a capacidade ainda é limitada em comparação com redes terrestres de fibra óptica.

#### Tecnologias Emergentes

- **Constelações de satélites de órbita baixa (LEO)**: empresas como SpaceX (Starlink) e Amazon (Project Kuiper) estão desenvolvendo grandes constelações de satélites em órbita baixa para fornecer internet de alta velocidade e baixa latência em todo o mundo.
  
- **Satélites de órbita inclinada**: satélites que cobrem regiões específicas, como áreas polares, onde satélites geoestacionários não têm cobertura direta.

#### Comparação com Outras Tecnologias de Rede

- **Vantagens**:  
  - Cobertura global, incluindo áreas remotas.
  - Alta confiabilidade em zonas de desastre ou onde a infraestrutura terrestre é limitada.

- **Desvantagens**:
  - Maior latência em comparação com redes terrestres (especialmente fibra óptica).
  - Dependência de condições climáticas para qualidade de sinal.

#### Segurança na Comunicação via Satélite

A comunicação via satélite enfrenta desafios de segurança, incluindo criptografia de dados para evitar interceptações e técnicas de mitigação de interferências, como jamming ou spoofing. Métodos modernos de segurança incluem o uso de chaves criptográficas robustas e firewalls dedicados para proteger as estações terrestres e satélites.

Uma das maiores batalhas da indústria de TV Fechada é contra a pirataria dos decodificadores de canais ou os famosos **Net a Gato**. Essa luta se arrasta há 20 anos. Praticamente, temos uma indústria de decodificadores piratas de um lado e as empresas de TV Fechada do outro.

Em 2024, a ANATEL lançou um hacktown de R$7.000,00 (sete mil reais) para o vencedor que encontrar uma solução contra a pirataria. O prejuízo anual das empresas de telecom é estimado em R$15 bilhões rsrsrs.

### (5) Conceitos de dBm e dB

O **dBm** é uma unidade de medida que expressa a potência de um sinal em **decibéis** (dB) em relação a **1 milivatt (mW)**. É uma medida logarítmica utilizada para avaliar a intensidade de um sinal de transmissão ou recepção, como o sinal de Wi-Fi em uma rede LAN. Foi criado pelo Graham Bell como forma de medir sua invensão, o sinal do telefone nas casas dos clientes.

- **dB** (decibéis) é uma medida relativa, usada para comparar níveis de potência.
- **dBm** é uma medida absoluta, referida a uma potência de 1 mW.

A fórmula para converter a potência em watts para dBm é:


![Formula](https://latex.codecogs.com/png.latex?\text{dBm}=10\cdot\log_{10}\left(\frac{P}{1\\text{mW}}\right))


Por exemplo:
- Se a potência P do sinal é de 1 mW, o valor em dBm será 0 dBm.
- Se a potência P é 10 mW, o valor será 10 dBm.

Curiosidade: a presença do 10 na fórmula apelidou de 10 Bells ou Decibel.

### (5.1) Importância do dBm na Medição de Sinal Wi-Fi

No contexto de redes LAN, particularmente para redes Wi-Fi, o **dBm** é importante para avaliar a **qualidade e a intensidade do sinal**. Ele indica o nível de potência que um dispositivo está recebendo do ponto de acesso (AP - Access Point). Como o sinal de Wi-Fi tende a se atenuar à medida que se distancia do roteador ou encontra obstáculos (como paredes), o valor de dBm ajuda a determinar a qualidade da conexão.

### (5.2) Interpretação dos Valores de dBm

Como o dBm é uma escala logarítmica, números mais negativos indicam sinais mais fracos. Veja uma escala de interpretação comum para redes Wi-Fi:

- **0 a -30 dBm**: sinal excelente. O dispositivo está muito próximo ao roteador, e a conexão será muito rápida e estável.
- **-31 a -50 dBm**: sinal muito bom. Ainda proporciona alta qualidade de conexão.
- **-51 a -60 dBm**: sinal bom. A maioria das aplicações funcionará sem problemas.
- **-61 a -70 dBm**: sinal aceitável. Pode haver alguma queda na velocidade ou na estabilidade da conexão, especialmente em ambientes congestionados.
- **-71 a -80 dBm**: sinal fraco. A conexão pode ser instável, com quedas de velocidade ou interrupções.
- **-81 dBm ou mais fraco**: sinal muito fraco ou inexistente. Provavelmente, o dispositivo não conseguirá se conectar.

### (5.3) Por que Medir o dBm em Redes Wi-Fi?

- **Otimização de Cobertura**: medir o dBm permite identificar pontos "cegos" ou áreas de sinal fraco dentro de um ambiente, como em um escritório ou residência. Isso ajuda a otimizar a localização de roteadores ou pontos de acesso.
  
- **Diagnóstico de Problemas de Conexão**: se um dispositivo estiver experimentando problemas de conexão, medir o dBm pode ajudar a diagnosticar se o problema é causado por um sinal fraco.

- **Configuração de Redes Mesh**: em redes Wi-Fi que utilizam tecnologia Mesh, a medição de dBm ajuda a posicionar os nós de forma eficiente para maximizar a cobertura e minimizar a interferência.

- **Análise de Interferência**: o dBm também pode ser utilizado para detectar interferências de outros dispositivos que operam na mesma frequência, como micro-ondas ou telefones sem fio, permitindo ajustes no canal de operação do Wi-Fi.


### (5.4) Qual a diferença entre dBm e dB?

A diferença entre **dBm** e **dB** está relacionada ao contexto de uso e à referência de medição:


### 5.4.1 dB (decibel)

- **Definição:** 
  - Uma unidade de medida relativa, que expressa a razão entre duas potências, intensidades ou amplitudes.
  - É adimensional e não tem uma referência fixa.
    
- **Fórmula:**
  - Para potências:  

   ![Equação de Potências](https://latex.codecogs.com/png.latex?\text{dB}=10\cdot\log_{10}\left(\frac{P_1}{P_2}\right))

    Onde \(P_1\) e \(P_2\) são as potências comparadas.

   - Para amplitudes (como tensões ou correntes):  

   ![Equação de Amplitudes](https://latex.codecogs.com/png.latex?\text{dB}=20\cdot\log_{10}\left(\frac{A_1}{A_2}\right))


    Onde \(A_1\) e \(A_2\) são as amplitudes comparadas.

- **Uso:**  
  - Medir ganhos, perdas ou relações relativas, como o ganho de um amplificador ou a atenuação de um sinal.
  - Não especifica valores absolutos; é sempre uma relação.

---

### 5.4.2 dBm (decibel-miliwatts)

- **Definição:**  
  - Uma unidade de medida **absoluta** que expressa a potência de um sinal **em relação a 1 miliwatt (mW)**.

- **Fórmula:**

 ![Equação dBm](https://latex.codecogs.com/png.latex?\text{dBm}=10\cdot\log_{10}\left(\frac{P}{1\\text{mW}}\right))

  Onde \(P\) é a potência medida em miliwatts.

- **Uso:**  
  - Medir a potência absoluta de sinais em sistemas de telecomunicações, rádio e redes.
  - Compara diretamente a potência a 1 mW, tornando-o útil para escalas absolutas.

---

### **Diferenças-chave**
| Característica      | dB                                | dBm                                  |
|---------------------|-----------------------------------|---------------------------------------|
| **Tipo de medida**  | Relativa (razão entre duas grandezas) | Absoluta (potência em relação a 1 mW) |
| **Referência fixa** | Não tem                          | 1 mW                                 |
| **Unidade associada** | Nenhuma (é adimensional)        | mW (potência absoluta)               |
| **Uso principal**   | Ganhos/perdas em amplificadores ou sinais | Potência absoluta em sistemas de RF e telecom |

---

### Exemplo Prático:
1. **dB (relativo):** Um amplificador aumenta a potência de um sinal de 10 mW para 100 mW. O ganho é:

   ![Equação de Ganho](https://latex.codecogs.com/png.latex?\text{Ganho%20(dB)}=10\cdot\log_{10}\left(\frac{100}{10}\right)=10\\text{dB})

2. **dBm (absoluto):** Se um sinal tem 50 mW de potência, sua medida em dBm é:

   ![Equação de Potencia](https://latex.codecogs.com/png.latex?\text{Potencia%20(dBm)}=10\cdot\log_{10}\left(\frac{50}{1}\right)=16,99\\text{dBm})
   

### (5.4) BOAS PRÁTICAS [SÁBADO-15min] Exercícios teóricos

**a)** Calcule o ganho em dB de um amplificador que excitado com 1W de sinal na entrada fornece 10W na saída:

Solução:
G = 10 . log(10/1)
G = 10 . log(10)
G = 10 . 1
G = 10dB

Ao calcular o ganho, não colocamos o W na frente do dBW.
o dBW vai aparecer quando vc disser que a PTX ou PRX é de tanto X [dBW]


**b)** Calcule o ganho em dB de um amplificador que excitado com 2W de sinal na entrada fornece 30W na saída:

**c)** Calcule o perda em dB de um amplificador que excitado com 1W de sinal na entrada fornece 0,5W na saída:

**d)** Observando a imagem abaixo, tem-se em a potência do sinal de uma ERB (Estação Rádio Base) da rede de celular. O valor da parte superior é o principal enquanto a potência do sinal da ERB vizinha é apresentada na metade de baixo da imagem. Calcule em W o valor de cada sinal. Os valores são dados em dBm.

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/inteli-pos-semana05a/blob/main/imgs/networkCellInfo-01.png">
   <img alt="Topologias de Redes" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/inteli-pos-semana05a/blob/main/imgs/networkCellInfo-01.png)">
</picture>



### (6) BOAS PRÁTICAS [SÁBADO-30min] Mapa de Calor WiFi (medição do dBm)

Nessa aula prática, vamos testar as diferenças de níveis de dBm entre posições de antenas e o uso da gaiola de faraday.

### 6.1 - Material Necessário

**a)** Celular os alunos com app X instalado (para medição do sinal WiFi em dBm);
**b)** 01 roteador caseiro de Internet;
**c)** Caixa com papel alumínio;

### 6.2 - Procedimentos

**a)** Conecte seu celular ao SSID do Roteador. O professor deve lhe passar a senha;
**b)** Abra o aplicativo e comece a medir o sinal dBm;
**c)** Observe o seu comportamento da seguinte forma tomando nota do dBm medido pelo seu celular:

* Matenha o seu celular na **vertical** em relação ao chão, e a 50cm do roteador. Quantos dBm?
* Matenha o seu celular na **horizontal** em relação ao chão, e a 50cm do roteador. Quantos dBm?
* Vá para cada canto extremo da sala, deixe seu celular na horizontal e depois horizontal. Quantos dBm em cada situação?

**d)** Com base nos valores medidos, quais as conclusões?

**e)** Cubra o roteador com a caixa de alumínio. Repita os itens do item (c).

**f)** Com base nos valores medidos, quais as conclusões?

### (7) BOAS PRÁTICAS [SÁBADO-30min] Alinhamento de antena de satélites

### 7.1 - Material Necessário

**a)** Instale o aplicativo no seu celular: Bússola;
**b)** SatFinder disponível para Android e Apple. Fornecedores recomendados: Artemkaxboy ou Maciej Grzegorczyk;
**c)** Antena parabólica banda KU com suporte e base;
**d)** Dispositivo profissional de apontamento de satélites;
**e)** Receptor de sinal KU para TV.

### 7.2 Procedimentos

**a)** Após instalar o aplicativo de satélite SATFINDER (Maciej Grzegorczyk), dê um clique longo sobre o nome do satélite que carregou no início econfigure para o satélite 70ºW STAR ONE C2/C4.
**b)** Anote os dados:

* Azimute
* Elevação
* Curva LNB
* Bússola
  
**c)** Clique no botão que parece um mapa no canto superior direito (ao lado da lupa)
**d)** A linha vermelha é a posição do 70ºW STAR ONE C2/C4 e o campo verde é a sua posição. Vire o seu celular até o campo verde alinhar com a linha vermelha

Posicione a antena parabólica conforme o seu celular indica;
Ligue o apontador profissional de satélites e cuidadosamente vai girando o no azimute e elevação até ouvir um apito forte;
Aperte os parafusos horizontais e verticais;
Ligue o receptor de TV

### 7.3 Relatório

Baixar esse [relatório](https://docs.google.com/document/d/1Mzgl8fcyugrLfKelmkGGMbXlSqrKveh3RHcbc5nKrkY/edit?usp=sharing), fazer uma cópia em seu dispositvo e preenchê-lo.


