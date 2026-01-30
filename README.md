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





# (1) Tipos de Rede

### (1.1) PAN (Personal Area Network)

Basicamente feita de dispositivos de curto alcance, em especial, os sem fio, via bluetooth;

### (1.2) LAN (Local Area Network)

Feita de cabos UTP ou STP, WiFi, conectando computadores, notebooks, TVs, projetores, Alexa, dispositivos IoT, impressores e servidores.
 
### (1.3) MAN (Metropolitan Area Network)

Feita de fibra óptica e rádio tipo minilink conectando empresas, hospitais, faculdades de diferentes endereços dentro de uma região metropolitana. Uma empresa ISP (Internet Service Provider) que alcança usuários dentro de uma cidade ou região metropolitana possui topologia física e lógica MAN.

### (1.4) WAN (Wide Area Network)

Feita de fibra óptica e satélite. A Internet se mistura com uma WAN.


## (2) Importância do Modelo OSI em Redes

Ambas as redes servem para conectar os hosts (que são end-devices numa grande rede chamada Internet).

Os hosts se comunincam usando diversos protocolos que trabalham de **camada N para camada N**.

![MODELO OSI](https://github.com/agodoi/SubRedes/blob/main/imgs/modelo_osi.png)

Alguns detaques da figura:

* O Modelo OSI (Opened Standard Interconnection) possui 7 camadas. É uma pilha de camadas totalmente abstrata, isto é, não existe essas camadas na vida real e não correspondem à nenhuma placa específica do computador;

## (2.1) Modelo OSI

* **Camada 07 - Aplicação :** cuida de tudo o que aparece na sua tela, é a aplicação;
* **Camada 06 - Apresentação :** é o tradutor com criptografia/descriptografia;
* **Camada 05 - Sessão :** é a camada de intercomunicação entre hosts. É como se fosse uma sessão de cinema que tem hora para começar e acabar, isto é, o serviço ficará disponível para você por X minutos ou horas;
* **Camada 04 - Transporte :** é a camada de transferência de dados fim a fim. É o frete de pacotes. É a cada do TCP e UDP. TCP garante a entrega, UDP transporta, mas não garante a entrega de pacotes;
* **Camada 03 - Redes :** determina o caminho e a lógica de roteamento de pacotes. É a cada do IPV4 e IPV6;
* **Camada 02 - Enlace :** é a camada que trata do endereço físico dos dispositivos de redes, isto é, o chassis da placa que trafega dados;
* **Camada 01 - Física :** é a camada dos padrões elétricos, eletrônicos e mecânicos.



## (2.2) Protocolo IPV4 vs IPV6

A figura a seguir aponta as principais diferenças. Contudo, na rede local, só se usa o IPV4.

![IP](https://github.com/agodoi/SubRedes/blob/main/imgs/ipv4_vs_ipv6.png)


## (3) Redes e Sub-redes

As redes de computadores servem para criar hierarquias de estações de trabalho dentro de numa organização. Por exemplo, numa instituição de ensino, existe a rede de alunos, a de professores e a administrativa. As redes geralmente não se conversam e há critérios de segurança entre elas.

E as sub-redes são redes menores que nascem a partir de uma rede, e para isso, precisamos do CIDR (Classes Inter-Domain Routing) para organizar essas redes dentro de redes.

A partir de agora, você entenderá como funciona o mapeamento de sub-rede, que pode ser implementado tanto numa rede Local quanto numa VPC (Virtual Private Cloud) como AWS, Azure, etc.

## Basicamente, o que você precisa saber pra dominar esse trem?

| Fazer conversão de binária para decimal.|
|-|

## Exemplo 01:

### Dado o IP 10.0.0.0/26
#### a) Qual é o endereço de rede?
#### b) Qual é o primeiro IPV4 disponível?
#### c) Qual é o endereço de broadcast na rede?
#### d) Qual é o último endereço IPV4 útil disponível?

O /26 significa que o CIDR = 26, então significa 26 bits são fixos, isto é, uma máscara de 26 bits "1" e 6 bits irrelevantes marcados por x.

Então, você pode brincar com os bits flexíveis marcados por **X**, mas não pode mudar os bits marcados por **1**.

|1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 X X X X X X |
|-|-|-|-|
| 255 | 255 | 255 | 192 |

Olhando para **10.0.0.0/26** sua missão é:

a) Qual é a máscara de rede?

b) Qual é o endereço de rede?

c) Qual é o primeiro IPV4 disponível?

d) Qual é o endereço de broadcast na rede?

e) Qual é o último endereço IPV4 útil disponível?

f) Quantos hosts cabem nessa rede?

### a) Máscara de rede

Máscara de sub-rede é um valor numérico que é usado em redes de computadores para dividir uma rede IP em sub-redes menores. Essa máscara é usada em conjunto com um endereço IP para determinar quais bits no endereço IP representam a rede e quais bits representam o host dentro dessa rede.

A parte da rede é indicada com **1**. A parte de hosts é indicada com **0** ou **X**. Vamos adotar o **X**, que significa, *irrelevante* (será uma faixa de valores e não um valor único). Para o exemplo dado **/26** teremos:

|1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 X X X X X X |
|-|-|-|-|
| 255 | 255 | 255 | 192 |


### b) Endereço de rede é o primeiro endereço da faixa (quando os bits X são só ZERO): 

Pega o IP original dado no enunciado:

| 10 | 0 | 0 | 0 |
|-|-|-|-|

Compare com a máscara e encontre os bits flexíveis **X** e não mexa com os bits marcados em **1**:

|1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 X X X X X X |
|-|-|-|-|
| 255 | 255 | 255 | 192 |

Resulta em:

| 0 0 0 0 1 0 1 0 | 0 0 0 0 0 0 0 0 | 0 0 0 0 0 0 0 0 | 0 0 X X X X X X |
|-|-|-|-|
| 10 | 0 | 0 | 0 0 X X X X X X |

Finalmente, coloque **0** no lugar dos **X** para encontrar o endereço da rede, porque endereço de rede é sempre o primeiro endereço possível:

| 10 | 0 | 0 | 0 0 0 0 0 0 0 0 |
|-|-|-|-|

Que é o mesmo que **10.0.0.0**

### c) Qual é primeiro IP útil disponível?

É sempre o primeiro após o endereço da rede. Portanto:

| 10 | 0 | 0 | 0 0 0 0 0 0 0 1 |
|-|-|-|-|
| 10 | 0 | 0 | 1 |


### d) Qual o endereço de broadcast da rede? 

Quando os **X** flexíveis são semopre **1**: 

| 10 | 0 | 0 | 0 0 1 1 1 1 1 1 |
|-|-|-|-|

Resulta em:

| 10 | 0 | 0 | 63 |
|-|-|-|-|

porque 1 1 1 1 1 1 = 63

### e) Qual é o último endereço ÚTIL da faixa?

É sempre o penúltimo endereço do broadcast.

| 10 | 0 | 0 | 62 |
|-|-|-|-|


### f) Qual é a quantidade de hosts possíveis nessa rede?

É só contar a quantidade de endereços do 1º até um antes do broadcast, que nesse caso será do 1 ao 62, portanto, 62 hosts possíveis de serem endereçados nessa rede. Em outras palavras, cabem 62 máquinas ou end-points nessa rede.

**Respostas:**
- Máscara de sub-rede: 255.255.255.192
- Endereço de rede: 10.0.0.0
- 1º endereço útil: 10.0.0.1
- Endereço de broadcast: 10.0.0.63 (último endereço)
- Último endereço útil: 10.0.0.62
- Quantidade de hosts possíveis: 62


## Exemplo 02: dado o IP 172.16.1.43/28

#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

**Respostas:**
- Máscara de sub-rede: 255.255.255.240
- Endereço de rede: 172.16.1.32
- 1º IPV4: 172.16.1.33
- Endereço de broadcast: 172.16.1.47 (último)
- Último IPV4 útil: 172.16.1.46
- Quantidade de hosts possíveis: 14


## Exemplo 03: dado o IP 10.0.8.0/21

#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

**Respostas:**
- Máscara de sub-rede: 255.255.248.0
- Endereço de rede: 10.0.8.0
- 1º IPV4: 10.0.8.1
- Endereço de broadcast: 10.0.15.255
- Último IPV4 útil: 10.0.15.254
- Quantidade de hosts possíveis: 2046


## Exemplo 04: 10.0.128.0/17

### Dado o IP
#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

**Respostas:**
- Máscara de sub-rede: 255.255.128.0
- Endereço de rede: 10.0.128.0
- 1º IPV4: 10.0.128.1
- Endereço de broadcast: 10.0.255.255
- Último IPV4 útil: 10.0.255.254
- Quantidade de hosts possíveis: 2^15 - 2 = 32.766

## Exemplo 05: 10.0.1.64/26

### Dado o IP
#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

**Respostas:**
- Máscara de sub-rede: 255.255.255.192
- Endereço de rede: 10.0.1.64
- 1º IPV4: 10.0.1.65
- Endereço de broadcast: 10.0.1.127
- Último IPV4 útil: 10.0.1.126
- Quantidade de hosts possíveis: 2^6 - 2 = 62


# Agora pense!

Considere que você colocou no seu roteador a seguinte rede principal: **192.168.0.0/22**.

### Dado o IP 192.168.0.0/22

#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

## E considerando que vocÊ criou uma sub-rede A com IP 192.168.0.0/24 e outra sub-rede B com 192.168.1.0/24

#### a) Qual é máscara de cada sub-rede?
#### b) Qual é o endereço de rede de cada sub-rede?
#### c) Qual é o primeiro IPV4 disponível de cada sub-rede?
#### d) Qual é o endereço de broadcast em cada rede-sub?
#### e) Qual é o último endereço IPV4 útil disponível em cada sub-rede?
#### f) Quantos hosts são possíveis em cada sub-rede?

### g) As sub-redes de fato estão dentro da rede principal? Justique!

A título de curiosidade, as faixas de IP gratuitas utilizadas em redes locais são:

- Faixa Classe: 10.0.0.0 a 10.255.255.255 

- Faixa Classe: 172.16.0.0 a 172.31.255.255

- Faixa Classe: 192.168.0.0 a 192.168.255.255

# Desafio. Descubra o CIDR de cada faixa endereços gratuitos abaixo:

- Faixa Classe: 10.0.0.0 a 10.255.255.255
  
- Faixa Classe: 172.16.0.0 a 172.31.255.255

- Faixa Classe: 192.168.0.0 a 192.168.255.255

## BOAS PRÁTICAS [60min] - Como configurar sub-redes usando Packet Tracer?

Nessa prática, vamos simular uma rede LAN com 2 sub-redes usando a ferramenta da Cisco chamada Packet Tracer.

Portanto, o objetivo é instalar o Packet Tracer em seu PC e fazer algumas simulações de rede e sub-redes.

### Material Necessário

a) Formar grupos em duplas;

b) Instalar o software Packet Tracer;

Atenção: para instalar o Packet Tracer, você precisa abrir uma conta no Cisco Networking Academy.

### Procedimentos

a) Abra esse link [https://www.netacad.com/pt/courses/getting-started-cisco-packet-tracer?courseLang=pt-BR](https://www.netacad.com/pt/courses/getting-started-cisco-packet-tracer?courseLang=pt-BR) e clique em **Self-Paced**

b) Se autentique clicando no botão **Google** (essa etapa abre a sua conta);

c) Encontre um botão chamado **Retornar ao curso**;

d) Logo no **Módulo 1: Baixar e Usar o Cisco Packet Tracer**, tem um link como esse [https://www.netacad.com/resources/lab-downloads](https://www.netacad.com/resources/lab-downloads) que permite você baixar o Packet Tracer de acordo com o sistema operacional do seu computador. Baixe o Packet Tracer compatível com o seu Sistema Operacional.

e) Abra o Packet Tracer, adicione os seguintes componentes:

* 02 roteadores modelo 1941 (3ª opção da esquerda para a direita);
* 02 switches modelo 2960 (1ª opção da esquerda para a direita);
* 4 PCs (end device) 

f) Monte a seguinte topologia física conforme a figura, sem ligar os cabos


![TOPOLOGIA](https://github.com/agodoi/inteli-pos-semana05b/blob/main/imgs/topologia-01.png)

g) Conecte um **cabo direto** dos PC 0 e 1 até o Switch 0 e outros **cabos diretos** dos PC 2 e 3 até o Switch 1. Use as portas **Fast Ethernet**.

h) Faça o mesmo conectando **cabo direto** entre Switch0 até o Roteador0 e do Switch1 até o Roteador1. 

i) Conecte um **cabo cruzado** entre os dois Roteadores. O uso do cabo cruzado é porque equipamentos iguais são sempre interligados por cabos cruzados (TX ligado no RX e vice-versa).

Sua montagem deve ficar igual à imagem a seguir.

![TOPOLOGIA1](https://github.com/agodoi/inteli-pos-semana05b/blob/main/imgs/topologia-02.png)

E na imagem a seguir, você encontra os nomes das portas de cada dispositivo para conferir se fez igual.

![TOPOLOGIA2](https://github.com/agodoi/inteli-pos-semana05b/blob/main/imgs/topologia-02b.png)

j) Agora pare e pense! Faça os cálculos dos IP e máscaras para você montar 3 sub-redes e com 64 endereços em cada sub-rede.

* Não é possível fazer 3 sub-redes, porque 3 não é múltiplo de 2. Então, você terá que mirar em 4 sub-redes e usar 3.
* Para ter 4 sub-redes, congele 2 bits mais significativos do 4º octeto. Portanto você terá um **CIDR = /26**. Observe os passos para entender:

  |Passos| 1º octeto | 2º octeto | 3º octeto | 4º octeto | Observação|
  |-|-|-|-|-|-|
  |1|? ? ? ? ? ? ? ?|? ? ? ? ? ? ? ?|? ? ? ? ? ? ? ?|? ? ? ? ? ? ? ?|Formato do IP|
  |2|? ? ? ? ? ? ? ?|? ? ? ? ? ? ? ?|? ? ? ? ? ? ? ?|congela congela x x x x x x|Demanda do projeto|
  |3|8 bits congelados|8 bits congelados|8 bits congelados|1 1 x x x x x x|Aplicando máscara 192|
  |4|1 1 1 1 1 1 1 1|1 1 1 1 1 1 1 1|1 1 1 1 1 1 1 1|1 1 x x x x x x|Bits congelados (1) e livres (x)|
  |5|255|255|255|192|Cálculo realizado|
  
  
* Suas sub-redes serão:
  
  | Sub-rede A | Sub-rede B | Sub-rede C | Sub-rede D |
  |-|-|-|-|
  |192.168.0.0 /192| 192.168.0.64 /192 | 192.168.0.128 /192 | 192.168.0.192 /192 |
  |PC0 + PC1 + SW0 + R0 | R0 + R1 | PC2 + PC3 + SW1 + R1| Não usado |

* Quais os endereços de cada Sub-rede?

  |Sub-Rede |End. Rede | 1º End. Útil | Último End. Útil | End. Broadcast |Máscara |
  |-|-|-|-|-|-|
  |A|192.168.0.0|192.168.0.1|192.168.0.62|192.168.0.63|255.255.255.192|
  |B|192.168.0.64|192.168.0.65|192.168.0.126|192.168.0.127|255.255.255.192|
  |C|192.168.0.128|192.168.0.129|192.168.0.190|192.168.0.191|255.255.255.192|
  |D|192.168.0.192|192.168.0.193|192.168.0.254|192.168.0.255|255.255.255.192|

k) Volte no circuito, e configure manualmente os IP para cada dispositivo. Note que agora temos o endereço do Gateway. Adotamos o último endereço útil de cada sub-rede para colocar a porta Giga respectiva voltada para o seu Switch como Gateway. É sempre assim? Não! Você escolhe qual será o endereço do Gateway e que fácil de memorizar.

|Dispositivo|Endereço IP|Máscara|Gateway|Observação|
|-|-|-|-|-|
|PC0|192.168.0.1|255.255.255.192|192.168.0.62|Rede A|
|PC1|192.168.0.2|255.255.255.192|192.168.0.62|Rede A|
|SW0|não tem|não tem|não tem|Não é gerencíavel|
|R0-GigaEth0/0|192.168.0.62|255.255.255.192|não tem|Último IP útil de A, Gateway de PC0 e PC1, Interface 0/0 de R0|
|R0-GigaEth0/1|192.168.0.126|255.255.255.192|não tem|Último IP útil de B, Interface 0/1 de R0|
|R1-GigaEth0/1|192.168.0.125|255.255.255.192|não tem|Penúltimo IP útil de B, Interface 0/1 de R1|
|R1-GigaEth0/0|192.168.0.190|255.255.255.192|não tem|Último IP útil de C, Gateway de PC2 e PC3, Interface 0/0 de R1|
|SW1|não tem|não tem|não tem|Não é gerencíavel|
|PC2|192.168.0.129|255.255.255.192|192.168.1.0|Rede C|
|PC3|192.168.0.130|255.255.255.192|192.168.1.0|Rede C|

l) Sua rede física está pronta, mas ela ainda não funciona, pois precisamos configurar manualmente os roteadores com as devidas tabelas de roteamento. Isso impacta no desempenho geral da rede. E sem tabela de roteamento, os roteadores não aprendem sobre os caminhos lógicos disponíveis nas sub-redes.

Pense em quais as redes estão diretamente interligadas em cada roteador, isto é, quais os cabos estão saindo e chegando nele. Essas redes diretamente ligadas já são de conhecimento do respectivo roteador.

* Roteador 0 conhece as redes 192.168.0.0 e 192.168.0.64
* Roteador 1 conhece as redes 192.168.0.0 e 192.168.0.128

Porém:

**Roteador 0 não conhece a rede 192.168.0.128 / 255.255.255.192**

**Roteador 1 não conhece a rede 192.168.0.0 / 255.255.255.192**

m) Abra o Roteador 0 e vá em **Config** e depois **Static**.

n) Em **Static Routes**, coloque em **Network** a rede que A não conhece, coloque 192.168.0.128 / 255.255.255.192 e no campo **Next hope** coloque o IP do próximo passo: 192.168.0.125 (que faz parte da 192.168.0.64). Essa interface GigaEthernet (192.168.0.125) é a porta de entrada mais próxima da sub-rede de A para chegar em B. Internamente, o roteador vai interconectar a 192.168.0.64 com a 192.168.0.128. Feito isso, clique em **Add**

o) Faça o mesmo para o Roteador 1, vá em **Config** e depois **Static**. No campo **Network**, coloque a rede que B não conhece, que é a rede A, lado interface 0/0: 192.168.0.0 / 255.255.255.192 e no campo **Next hoje**, coloque o IP 192.168.0.126 e clique em **Add**. 

p) Para testar a rede, clique no botão **Simulation** que fica no canto inferior direito, clique no botão **Edit Filters**, desmarque tudo, e só deixei o **ICMP** (protocolo de ping).

q) Pegue um ícone de evelope fechado que está **Add simple PDU (P)** e arraste e solte encima do PC0 e depois arraste para cima do PC3.

![LAN1](https://github.com/agodoi/inteli-pos-semana05b/blob/main/imgs/cartinha.png)


r) Dê um play e observe o pacote indo e voltando em direção ao PC3. Se o pacote foi e voltou, **SUCESSO!**. Se não, delete o pacotinho e repita o passo (q).

---
## Cartinha indo do PC0 em direção ao PC3


![LAN2](https://github.com/agodoi/inteli-pos-semana05b/blob/main/cartinha2.png)

---
## Cartinha voltando do PC3 em direção ao PC0

![LAN3](https://github.com/agodoi/inteli-pos-semana05b/blob/main/cartinha3.png)


# Exercício

1) Faça um mapeamento de IP para ter 256 endereços de host e 3 sub-redes A B C.
2) Monte outro workspace no Packet Tracer.
3) Monte a rede LAN no Packet Tracer.
4) Faça o primeiro computador da rede A mandar um ping para o último computador da sua rede C.


## Simulação ao Ataque de um IoT

Nessa parte da aula, vamos simular um ataque a um dispostivo IoT que controla uma válvula importante de gás, que se fechada, corta o fornecimento de gás nas residências em pleno inverno.

Regras:

a) Trabalho em dupla;

b) Use qualquer tipo de programação que achar necessária;

c) O IoT é um ESP32;

d) Há 2 LEDs para você atacar.

Alguns levantamentos por meio da engenharia social:

1) O dispositivo pode estar nas redes A ou C do mapeamento feito no Packet Tracer acima (considere a rede com subrede de 64 hosts);
2) Para controlar o dispositivo, usa-se a URL:
   
   a) X.X.X.X/pino/on (LIGA)
   
   b) X.X.X.X/pino/off (DESLIGA)
   
4) Sua missão é atacar esse dispositivo fazendo-o desligar (DESLIGAR O LED VERDE). 
5) Qual é a sua estratégia?
6) Faça o ataque e se funcionar, monte uma apresentação que será apresentada à turma.

## Montando o seu Dispositivo IoT

Agora, vamos montar o seu dispositivo IoT que você mesmo atacou.

Sabe gravar um programa usando o Arduino IDE?

### 1. Pré-requisitos
- **Arduino IDE instalado** (versão 1.8.19 ou superior).
  - Baixe a IDE no site oficial: [https://www.arduino.cc/en/software](https://www.arduino.cc/en/software).
- **Cabo USB** para conectar o ESP32 ao computador.
- **Placa ESP32** (qualquer modelo compatível, como DevKit V1 ou NodeMCU-32S).

---

### 2. Passo a Passo para Instalação

#### Passo 1: Abra o Arduino IDE
- Inicie o Arduino IDE no seu computador.

#### Passo 2: Adicione o Gerenciador de Placas ESP32
1. Vá para o menu **File** (ou **Arquivo**) e clique em **Preferences** (ou **Preferências**).
2. Na janela de Preferências, localize o campo **Additional Board Manager URLs** (ou **URLs Adicionais para Gerenciadores de Placas**).
3. Insira a URL abaixo no campo (caso já tenha outras URLs, separe-as por vírgula):
   ```
   https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
   ```
4. Clique em **OK** para salvar.

#### Passo 3: Instale as Placas ESP32
1. Vá para o menu **Tools** (ou **Ferramentas**) > **Board** (ou **Placa**) > **Boards Manager** (ou **Gerenciador de Placas**).
2. Na barra de busca, digite **ESP32**.
3. Clique em **Install** (ou **Instalar**) na entrada "esp32 by Espressif Systems".
4. Aguarde o download e a instalação serem concluídos.

#### Passo 4: Selecione a Placa ESP32
1. Conecte sua placa ESP32 ao computador usando o cabo USB.
2. No Arduino IDE, vá para **Tools** > **Board** > **ESP32 Arduino**.
3. Escolha a placa que corresponde ao seu modelo, como:
   - **ESP32 Dev Module** (para a maioria das placas DevKit V1).

#### Passo 5: Configure a Porta Serial
1. Ainda no menu **Tools**, vá para **Port**.
2. Selecione a porta correspondente ao ESP32 (geralmente é algo como `COM3`, `COM4`, etc., no Windows, ou `/dev/ttyUSB0` no Linux/Mac).

#### Passo 6: Teste a Instalação
1. Abra o exemplo básico de piscar LED integrado:
   - Vá para **File** > **Examples** > **Basics** > **Blink**.
2. Substitua o número do pino no código, se necessário, para o LED embutido no ESP32:
   ```cpp
   void setup() {
       pinMode(2, OUTPUT); // Pino 2 geralmente é o LED embutido
   }

   void loop() {
       digitalWrite(2, HIGH);
       delay(1000);
       digitalWrite(2, LOW);
       delay(1000);
   }
   ```
3. Clique em **Upload** (ou pressione `Ctrl + U`).
4. Aguarde o código ser enviado. Se aparecer "Done Uploading", o LED do ESP32 começará a piscar.

---

### 3. Solução de Problemas
- **Problema: Porta Serial não aparece**:
  - Verifique se o driver USB está instalado. Baixe o driver CP2102 ou CH340 (dependendo da sua placa) no site do fabricante.
  - [DONWLOAD](https://www.silabs.com/developer-tools/usb-to-uart-bridge-vcp-drivers?tab=downloads)
- **Problema: Erro ao enviar código**:
  - Pressione e mantenha o botão **BOOT** no ESP32 enquanto o código é carregado.

---

Com esses passos, o ESP32 estará configurado e pronto para ser usado na Arduino IDE! Se precisar de mais ajuda, é só perguntar.

# Código que Controla LED pela URL IP/on ou IP/off

```
// Load Wi-Fi library
#include <WiFi.h>

// Replace with your network credentials
const char* ssid = "RedeIoT";
const char* password = "inteli123";

// Set web server port number to 80
WiFiServer server(80);

// Variable to store the HTTP request
String header;

// Auxiliar variables to store the current output state
String output26State = "off";
String output27State = "off";

// Assign output variables to GPIO pins
const int output26 = 26;
const int output27 = 27;

// Current time
unsigned long currentTime = millis();
// Previous time
unsigned long previousTime = 0; 
// Define timeout time in milliseconds (example: 2000ms = 2s)
const long timeoutTime = 2000;

void setup() {
  Serial.begin(115200);
  // Initialize the output variables as outputs
  pinMode(output26, OUTPUT);
  pinMode(output27, OUTPUT);
  // Set outputs to LOW
  digitalWrite(output26, LOW);
  digitalWrite(output27, LOW);

  // Connect to Wi-Fi network with SSID and password
  Serial.print("Connecting to ");
  Serial.println(ssid);
  WiFi.begin(ssid, password);
  while (WiFi.status() != WL_CONNECTED) {
    delay(500);
    Serial.print(".");
  }
  // Print local IP address and start web server
  Serial.println("");
  Serial.println("WiFi connected.");
  Serial.println("IP address: ");
  Serial.println(WiFi.localIP());
  server.begin();
}

void loop(){
  WiFiClient client = server.available();   // Listen for incoming clients

  if (client) {                             // If a new client connects,
    currentTime = millis();
    previousTime = currentTime;
    Serial.println("New Client.");          // print a message out in the serial port
    String currentLine = "";                // make a String to hold incoming data from the client
    while (client.connected() && currentTime - previousTime <= timeoutTime) {  // loop while the client's connected
      currentTime = millis();
      if (client.available()) {             // if there's bytes to read from the client,
        char c = client.read();             // read a byte, then
        Serial.write(c);                    // print it out the serial monitor
        header += c;
        if (c == '\n') {                    // if the byte is a newline character
          // if the current line is blank, you got two newline characters in a row.
          // that's the end of the client HTTP request, so send a response:
          if (currentLine.length() == 0) {
            // HTTP headers always start with a response code (e.g. HTTP/1.1 200 OK)
            // and a content-type so the client knows what's coming, then a blank line:
            client.println("HTTP/1.1 200 OK");
            client.println("Content-type:text/html");
            client.println("Connection: close");
            client.println();
            
            // turns the GPIOs on and off
            if (header.indexOf("GET /26/on") >= 0) {
              Serial.println("GPIO 26 on");
              output26State = "on";
              digitalWrite(output26, HIGH);
            } else if (header.indexOf("GET /26/off") >= 0) {
              Serial.println("GPIO 26 off");
              output26State = "off";
              digitalWrite(output26, LOW);
            } else if (header.indexOf("GET /27/on") >= 0) {
              Serial.println("GPIO 27 on");
              output27State = "on";
              digitalWrite(output27, HIGH);
            } else if (header.indexOf("GET /27/off") >= 0) {
              Serial.println("GPIO 27 off");
              output27State = "off";
              digitalWrite(output27, LOW);
            }
            
            // Display the HTML web page
            client.println("<!DOCTYPE html><html>");
            client.println("<head><meta name=\"viewport\" content=\"width=device-width, initial-scale=1\">");
            client.println("<link rel=\"icon\" href=\"data:,\">");
            // CSS to style the on/off buttons 
            // Feel free to change the background-color and font-size attributes to fit your preferences
            client.println("<style>html { font-family: Helvetica; display: inline-block; margin: 0px auto; text-align: center;}");
            client.println(".button { background-color: #4CAF50; border: none; color: white; padding: 16px 40px;");
            client.println("text-decoration: none; font-size: 30px; margin: 2px; cursor: pointer;}");
            client.println(".button2 {background-color: #555555;}</style></head>");
            
            // Web Page Heading
            client.println("<body><h1>ESP32 Web Server</h1>");
            
            // Display current state, and ON/OFF buttons for GPIO 26  
            client.println("<p>GPIO 26 - State " + output26State + "</p>");
            // If the output26State is off, it displays the ON button       
            if (output26State=="off") {
              client.println("<p><a href=\"/26/on\"><button class=\"button\">ON</button></a></p>");
            } else {
              client.println("<p><a href=\"/26/off\"><button class=\"button button2\">OFF</button></a></p>");
            } 
               
            // Display current state, and ON/OFF buttons for GPIO 27  
            client.println("<p>GPIO 27 - State " + output27State + "</p>");
            // If the output27State is off, it displays the ON button       
            if (output27State=="off") {
              client.println("<p><a href=\"/27/on\"><button class=\"button\">ON</button></a></p>");
            } else {
              client.println("<p><a href=\"/27/off\"><button class=\"button button2\">OFF</button></a></p>");
            }
            client.println("</body></html>");
            
            // The HTTP response ends with another blank line
            client.println();
            // Break out of the while loop
            break;
          } else { // if you got a newline, then clear currentLine
            currentLine = "";
          }
        } else if (c != '\r') {  // if you got anything else but a carriage return character,
          currentLine += c;      // add it to the end of the currentLine
        }
      }
    }
    // Clear the header variable
    header = "";
    // Close the connection
    client.stop();
    Serial.println("Client disconnected.");
    Serial.println("");
  }
}
```
# Montagem do Circuito dos LEDs

![Circuito](https://github.com/agodoi/inteli-pos-semana10/blob/main/imgs/esp32com2leds.png)

---
# Solução para Varrer faixa de IP usando Python

```
import platform
import subprocess

def ping_sweep(start_ip, end_ip):
    # Certifique-se de que está rodando no Windows
    if platform.system() != "Windows":
        print("Este script está configurado para rodar no Windows.")
        return

    print(f"Varredura de {start_ip} a {end_ip}...\n")
    # Divide o IP inicial e final em partes
    start_parts = start_ip.split('.')
    end_parts = end_ip.split('.')

    # Certifica-se de que os IPs estão na mesma rede
    if start_parts[:3] != end_parts[:3]:
        print("Apenas suportamos a varredura na mesma sub-rede.")
        return

    # Converte os últimos octetos para inteiros
    start_range = int(start_parts[3])
    end_range = int(end_parts[3])
    base_ip = '.'.join(start_parts[:3])

    for i in range(start_range, end_range + 1):
        ip = f"{base_ip}.{i}"
        try:
            # Comando de ping para Windows
            output = subprocess.run(["ping", "-n", "1", ip], stdout=subprocess.PIPE, text=True)
            if "TTL=" in output.stdout:
                print(f"Dispositivo ativo: {ip}")
        except Exception as e:
            print(f"Erro ao tentar pingar {ip}: {e}")

# Define a faixa de IP para varrer
start_ip = "192.168.0.1"
end_ip = "192.168.0.62"

# Executa a função
ping_sweep(start_ip, end_ip)
```








# Mergulhando nas Redes como um Tubarão

Nessa instrução vamos nos aprofundar sobre o que acontece quando uma requisição-resposta entre cliente e servidor é processada. Faremos atividades práticas para simular esses processos, e compreenderemos ainda mais sobre Redes de Computadores.

# Galera, dá uma olhada nessa imagens. Com elas, vocês vão aprender o que é a Internet e seus Protocolos.

## Pontes

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m02-semana10/blob/main/imgs/pontes.png">
   <img alt="Tipo de Modelagens" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m02-semana10/blob/main/imgs/pontes.png)">
</picture>

## Mapas

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m02-semana10/blob/main/imgs/mapas.jpg">
   <img alt="Tipo de Modelagens" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m02-semana10/blob/main/imgs/mapas.jpg)">
</picture>

## Transportes

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m02-semana10/blob/main/imgs/modais-de-transporte.jpg">
   <img alt="Tipo de Modelagens" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m02-semana10/blob/main/imgs/modais-de-transporte.jpg)">
</picture>

## Compartilhamento de informações

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m02-semana10/blob/main/imgs/compartilhamento.jpg">
   <img alt="Tipo de Modelagens" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m02-semana10/blob/main/imgs/compartilhamento.jpg)">
</picture>

# Tipos de Redes

## 1) PAN

**Personal Area Network (PAN)** é uma rede de computadores usada para comunicação entre dispositivos próximos a uma pessoa. Normalmente, essas redes cobrem um raio de poucos metros. Na rede PAN têm-se os dispositivos:

* Smartphones;
* Computadores;
* Fones de ouvido;
* Mouse e teclado;
* Relógios;
* Impressoras e outros dispositivos pessoais.



### 1.1) Tecnologias de Conexão

As tecnologias mais comuns usadas em PANs são Bluetooth, ZigBee (conexão usada em ambientes com ruído eletromagnético) e NFC (Near Field Communication, usado no cartão de crédito) e, em alguns casos, o Wi-Fi.

### 1.2) Como Funciona uma Rede PAN?

As PANs funcionam através da comunicação direta entre dispositivos ou via um ponto de acesso central. A seguir, vamos explorar algumas das tecnologias mais comuns utilizadas em PANs.

### 1.3) Vantagens da PAN

* Mobilidade: permite a comunicação entre dispositivos pessoais em movimento;
* Fácil Configuração: geralmente, a configuração é simples e rápida;
* Conectividade sem fio: elimina a necessidade de cabos, proporcionando conveniência.

### 1.4) Desvantagens da PAN

* Alcance Limitado: o alcance é restrito a poucos metros;
* Interferência: pode haver interferência de outros dispositivos sem fio na mesma faixa de frequência;
* Segurança: a segurança pode ser uma preocupação, especialmente em tecnologias como Bluetooth.

### 1.5) Aplicações Práticas de Redes PAN

* Automação residencial: conectar e controlar dispositivos domésticos como lâmpadas inteligentes, termostatos e fechaduras;
* Acessórios pessoais: conectar fones de ouvido Bluetooth a smartphones;
* Saúde e fitness: Sincronização de dados entre smartwatches e aplicativos de saúde em smartphones.

## 2) LAN

**Local Area Network (LAN)** é uma rede de computadores que abrange uma área geográfica limitada, como uma residência, escola, laboratório, universidade ou prédio comercial. A principal característica das LANs é que elas são redes de alta velocidade que conectam computadores e dispositivos em uma área relativamente pequena.)

Na rede LAN têm-se os dispositivos:
 
* Computadores;
* Servidores;
* Impressoras;
* Switches (conectam dispositivos dentro da LAN);
* Roteadores (conectam a LAN à Internet);
* Cabos e Conectores;
* Pontos de Acesso (AP).


### 2.1) Tecnologias de Conexão

As tecnologias de conexão das LANs são de fio ou sem fio (rádio). No fio, a tecnologia de conexão chama-se **Ethernet** com as versões CAT5e, CAT6, CAT6a, CAT7 e no sem fio, **Wi-Fi** (Wireless Fidelity) têm-se as versões de tecnologias 802.11n, 802.11ac e o mais recente 802.11ax (Wi-Fi 6). Existe ainda o PLC (Power Line Communication) e a fibra óptica.

### 2.2) Como Funciona uma Rede LAN?

As LANs funcionam através da interconexão de dispositivos usando cabos Ethernet ou conexões sem fio. A seguir, vamos explorar algumas das tecnologias mais comuns utilizadas em LANs. As redes cabeadas são sempre mais velozes.

### 2.3) Vantagens da LAN

* Alta velocidade: oferece altas taxas de transferência de dados;
* Confiabilidade: conexões por cabo são muito estáveis e confiáveis;
* Compartilhamento de Recursos: facilita o compartilhamento de recursos como impressoras e arquivos.

### 2.4) Desvantagens da LAN

* Alcance limitado: cobertura restrita a uma área geográfica pequena;
* Custo de instalação: configurar uma LAN com cabeamento pode ser caro;
* Manutenção: requer manutenção regular para garantir o bom funcionamento.

### 2.5) Aplicações Práticas de Redes LAN

* Ambientes empresariais: conectar computadores e servidores em um escritório;
* Instituições de ensino: interconectar laboratórios de informática e dispositivos educacionais;
* Residências: conectar dispositivos domésticos como computadores, consoles de jogos e smart TVs.


## 3) MAN

**Metropolitan Area Network (MAN)** é uma rede de computadores que abrange uma área geográfica maior do que uma LAN, mas menor do que uma **WAN (Wide Area Network)**. Normalmente, uma MAN conecta várias LANs dentro de uma cidade ou região metropolitana para compartilhar recursos e serviços. Os dispositivos da MAN são:

* Roteadores, switches e servidores;
* Cabos de Fibra Óptica: Utilizados para conexões de alta velocidade entre diferentes LANs;
* Provedores de Serviço de Internet (ISP): são as empresas de telecom que fornecem a infraestrutura necessária para conectar as redes em uma área metropolitana;
* Equipamentos de Comunicação Com e Sem Fio: utilizados para conexões ponto-a-ponto ou multiponto entre LANs.

### 3.1) Tecnologias de Conexão

Fibra óptica ou links sem fio, que são rádios de micro-ondas que parecem antenas parabólicas ou antenas quadradas.


### 3.2) Como Funciona uma Rede MAN?

As MANs funcionam conectando várias LANs através de enlaces de alta velocidade.

### 3.3) Vantagens da MAN

* Alta velocidade: oferece altas taxas de transferência de dados entre diferentes LANs;
* Ampla cobertura: conecta redes em uma grande área geográfica;
* Eficiência de custo: compartilhamento de recursos e serviços reduz custos.

### 3.4) Desvantagens da MAN

* Complexidade de instalação: requer infraestrutura sofisticada e planejamento;
* Custo inicial: alto custo de instalação de fibra óptica e outros equipamentos;
* Manutenção: necessita de manutenção regular e suporte técnico especializado.

### 3.5) Aplicações Práticas de Redes MAN

* Governo e administração pública: Conectar diferentes departamentos e agências dentro de uma cidade;
* Instituições educacionais: Interconectar campus universitários e bibliotecas;
* Empresas grandes: Conectar escritórios e filiais espalhados por uma área metropolitana.

## 4) WAN

Uma **Wide Area Network (WAN)** é uma rede de computadores que abrange uma grande área geográfica, permitindo a comunicação e compartilhamento de recursos entre dispositivos e redes distantes. As WANs são essenciais para conectar escritórios corporativos, instituições governamentais, universidades e outros usuários que precisam de comunicação de longa distância.

Componentes:

* Roteadores e switches: dispositivos que direcionam o tráfego de rede e conectam diferentes redes;
* Linhas de comunicação: incluem cabos de fibra óptica, cabos submarinos, satélites e enlaces de rádio;
* Provedores de serviços de telecomunicações e Internet: empresas que fornecem infraestrutura de comunicação para conectar diferentes partes da WAN e à Internet.

### 4.1) Tecnologias de Conexão

As tecnologias de transmissão mais comuns: 

* Fibra óptica marítma;
* Satélites;
* MPLS (Multiprotocol Label Switching) que é um protocolo moderno que integra várias redes de telecomunicações, como celular e links de banda larga.

### 4.2) Como Funciona uma Rede WAN?

As WANs funcionam conectando várias LANs e MANs através de longas distâncias usando diversas tecnologias de transmissão.

### 4.3) Vantagens da WAN

* Conectividade global: permite a comunicação entre redes em diferentes locais geográficos;
* Compartilhamento de recursos: facilita o compartilhamento de recursos e informações entre escritórios e usuários dispersos;
* Escalabilidade: pode ser expandida para incluir novas regiões ou usuários conforme necessário.

### 4.4) Desvantagens da WAN

* Custo Elevado: implementação e manutenção podem ser caras;
* Complexidade: requer infraestrutura sofisticada e gerenciamento especializado;
* Latência: pode haver atrasos na comunicação devido à distância e à tecnologia utilizada.

### 4.5) Aplicações Práticas de Redes WAN

* Empresas multinacionais: conectar escritórios em diferentes países;
* Instituições governamentais: compartilhamento de informações e recursos entre departamentos em diferentes locais.
* Provedores de Serviços de Internet (ISP - Internet Service Provider): fornecer conectividade à internet em grande escala.

# Modelo TCP/IP

## Definição do Modelo TCP/IP

O modelo TCP/IP, também conhecido como **Modelo de Internet**, é um conjunto de protocolos de comunicação que forma a base da Internet. 


<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m02-semana10/blob/main/imgs/modeloTCP-IP.png">
   <img alt="Tipo de Modelagens" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m02-semana10/blob/main/imgs/modeloTCP-IP.png)">
</picture>



## Onde os protocolos vão?


<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m02-semana10/blob/main/imgs/camadas_v2.png">
   <img alt="Tipo de Modelagens" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m02-semana10/blob/main/imgs/camadas_v2.png)">
</picture>


## De que forma?

<picture>
   <source media="(prefers-color-scheme: light)" srcset="https://github.com/agodoi/m02-semana10/blob/main/imgs/TCP-IPfig1.png">
   <img alt="Tipo de Modelagens" src="[YOUR-DEFAULT-IMAGE](https://github.com/agodoi/m02-semana10/blob/main/imgs/TCP-IPfig1.png)">
</picture>



## Vantagens do Modelo TCP/IP

1. **Interoperabilidade Universal**:
    - **Explicação**: o modelo TCP/IP é amplamente adotado e suportado por praticamente todos os sistemas operacionais e dispositivos de rede, o que facilita a comunicação e integração entre diferentes tecnologias e plataformas.
    - **Exemplo**: Um smartphone rodando iOS pode se comunicar sem problemas com um servidor rodando Linux, graças ao uso comum do TCP/IP.

2. **Escalabilidade**:
    - **Explicação**: o TCP/IP foi projetado para escalar eficientemente, suportando desde pequenas redes locais até a vasta rede global da Internet.
    - **Exemplo**: uma empresa pode começar com uma pequena rede interna e expandir para uma rede global sem a necessidade de substituir a infraestrutura ou os protocolos de comunicação.

3. **Robustez e Flexibilidade**:
    - **Explicação**: o modelo é robusto e flexível, capaz de se adaptar a diferentes tecnologias de rede e resistir a falhas parciais na rede.
    - **Exemplo**: se uma rota de dados na Internet falhar, o TCP/IP pode redirecionar o tráfego por outras rotas, garantindo que a comunicação não seja interrompida.

## Desvantagens do Modelo TCP/IP

1. **Complexidade na Configuração**:
    - **Explicação**: a configuração de redes TCP/IP pode ser complexa, exigindo conhecimentos técnicos avançados para ajustar parâmetros como endereçamento IP, sub-redes e roteamento.
    - **Exemplo**: configurar uma rede corporativa com múltiplos roteadores e sub-redes requer uma compreensão detalhada de conceitos como máscara de sub-rede e tabelas de roteamento.

2. **Sobrecarga de Protocolo**:
    - **Explicação**: o protocolo TCP, em particular, adiciona uma sobrecarga significativa devido à necessidade de estabelecer e manter conexões, o que pode impactar a performance em redes com recursos limitados.
    - **Exemplo**: em redes de sensores ou dispositivos IoT com pouca largura de banda, a sobrecarga do TCP pode resultar em menor eficiência na transmissão de dados.

3. **Segurança Limitada por Padrão**:
    - **Explicação**: o TCP/IP foi desenvolvido com pouca preocupação com a segurança, e muitas de suas funcionalidades nativas são vulneráveis a ataques. Medidas de segurança adicionais são frequentemente necessárias.
    - **Exemplo**: o protocolo não possui mecanismos de criptografia ou autenticação nativos, necessitando de camadas extras de segurança, como VPNs ou TLS, para proteger os dados.

# Faixa de Endereçamentos IP

## Entendendo o CIDR: Uma Maneira Flexível de Endereçar Redes

CIDR - Classless Inter-Domain Routing.

Imagine que você precisa organizar um grande número de casas em uma cidade. Em vez de usar nomes de ruas e números de casas individuais, você decide agrupá-las em bairros. 

Cada bairro tem um nome e um número que representa quantas casas ele contém. Essa é a ideia básica por trás do CIDR.

## O que é CIDR?

CIDR é um método para alocar e identificar endereços IP em redes de computadores. Ele substitui o antigo sistema de classes de endereços (A, B, C) por uma abordagem mais flexível. Em vez de classes fixas, o CIDR usa prefixos de comprimento variável para definir o tamanho de uma rede.

## Como Funciona?

Um endereço CIDR é composto por duas partes:

1. **Endereço IP:** um endereço IP normal (por exemplo, 192.168.1.0).
2. **Prefixo:** um número que indica quantos bits do endereço IP são usados para **identificar o bairro**, que nesse conceito, chama-se **REDE** (por exemplo, /24).

O prefixo define a máscara de sub-rede e o número de endereços IP disponíveis na rede. Por exemplo:

* **/24:** são 24 bits todos **1**, logo usamos uma máscara = 255.255.255.0, e sobram 8 bits, totalizando 256 endereços IP de **CASAS** ou **COMPUTADORES**;
* **/25:** são 26 bits todos **1**, logo usamos uma máscara = 255.255.255.128, e sobram 7 bits, totalizando 128 endereços IP de COMPUTADORES;
* **/26:** são 27 bits todos **1**, logo usamos uma máscara = 255.255.255.192, e sobram 6 bits, totalizando 64 endereços IP de COMPUTADORES;

**Vantagens do CIDR:**

* **Alocação Eficiente:** Permite alocar endereços IP de forma mais granular, evitando o desperdício de endereços que ocorria com as classes fixas.
* **Roteamento Simplificado:** Facilita o roteamento de pacotes na internet, pois os roteadores podem usar o prefixo para determinar rapidamente a rede de destino.
* **Escalabilidade:** Adapta-se facilmente ao crescimento da internet, permitindo a criação de redes de diferentes tamanhos.

## Faixas de Endereços Privados (Gratuitos)

São faixas reservadas para uso em redes locais e não são roteados na Internet pública. Você pode usá-los livremente dentro de sua rede doméstica ou empresarial:

* 10.x.x.x,
* 172.16.x.x a 172.31.x.x e
* 192.168.x.x 

**Exemplo Prático:**

Você tem uma rede com o endereço IP 192.168.1.0 e precisa dividi-la em quatro sub-redes menores. Usando o CIDR, você pode fazer o seguinte:

* **Sub-rede 1:** 192.168.1.0/26
* **Sub-rede 2:** 192.168.1.64/26
* **Sub-rede 3:** 192.168.1.128/26
* **Sub-rede 4:** 192.168.1.192/26

Cada sub-rede terá 64 endereços IP disponíveis para seus dispositivos.

**Conclusão:**

O CIDR é uma ferramenta essencial para o endereçamento de redes na internet moderna. Sua flexibilidade e eficiência o tornam ideal para lidar com o crescimento contínuo da rede e a demanda por endereços IP. Se você trabalha com redes de computadores, entender o CIDR é fundamental para planejar e gerenciar suas redes de forma eficaz.


# Prática usando ```ipconfig /all```

## Orientações

### 1) Cada aluno precisa abrir o link a seguir e preencher os campos em vermelho no respectivo assento da sua bancada. Use o comando ```ipconfig /all``` no CMD do seu computador para puxar os dados necessários. No iMAC faça testes com ```system_profiler SPNetworkDataType```

[CLIQUE AQUI](https://docs.google.com/presentation/d/1juQH2R2auQRocWxc2rCXlqJZy550fF74A7VYAapsnHk/edit?usp=sharing)

# Prática com Wireshark

Caso não tenha instalado o Wireshark, vai dando NEXT e marque todas as opções na tela do Ncap.
Se aparecer várias telas pedindo permissão de administrador, vai dando SIM em todas até não ter mais nenhuma.

Clique no ícone da barbatana azul do tubarão no canto esquerdo superior. Isso vai abrir uma janela de observação de protocolos.

### 2) Observe a tela do Wireshark monitorando os diferentes protocolos que aparecem por 5 minutos e anote 5 protocolos diferentes que estão na lista.

[RELATÓRIO](https://docs.google.com/document/d/1IGRt-VtoJPHgFFuW-glrpMJ2s2PYaDem2KLrSdBYAog/edit?usp=sharing)


| Tipo de Evento     | O que está acontecendo?                                                             |
| ------------------ | ----------------------------------------------------------------------------------- |
| ARP                | Dispositivos buscando/confirmando IPs na LAN.                                       |
| TCP/TLS (HTTPS)    | Sessões seguras entre cliente `10.128.1.72` e servidores externos (TLS 1.2 e 1.3).  |
| DNS                | Resolução de nomes como `slackb.com` para IPs públicos.                             |
| mDNS/SSDP          | Dispositivos descobrindo serviços de mídia e rede na LAN.                           |
| DHCP               | Dispositivos se conectando e negociando IP com o servidor.                          |
| ACKs fora de ordem | Alta carga de dados sendo transmitida, possível buffer ou reenvio por controle TCP. |


### 3) Cada grupo deve montar uma apresentação de 5min definindo os protocolos que está observando, dar um exemplo de um pacote observado. Os 2 melhores grupos que melhor fazer um historytelling explicando os seus protocolos com os seus exemplos, leva um chocolate.





