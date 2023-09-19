# Introdução ao Wireshark

---

Bem-vindo ao universo do Wireshark, uma poderosa ferramenta de análise de rede que é essencial na área de cybersegurança. Neste módulo, você aprenderá como instalar e usar o Wireshark para capturar e analisar o tráfego de rede. Vamos começar!

## Instalando o Wireshark

O Wireshark está disponível para Windows, Linux e macOS. Para instalar o Wireshark no Windows, basta acessar o site oficial e baixar o instalador. Para instalar no Linux, basta executar o comando `sudo apt install wireshark`. Para instalar no macOS, basta acessar o site oficial e baixar o instalador. Mas como dito nos outros modulos, nao vamos usar nem Mac e nem Windows, portanto no seu Linux instale o Wireshark com o comando `sudo apt install wireshark`.

## O que é o Wireshark?

Vamos entender melhor sobre o Wireshark e como ele funciona. O Wireshark é uma ferramenta de análise de rede que permite capturar e analisar o tráfego de rede em tempo real. Ele é usado por profissionais de cybersegurança para identificar problemas de rede e vulnerabilidades de segurança. O Wireshark é uma ferramenta open-source, o que significa que você pode baixá-lo gratuitamente. Ele é compatível com a maioria dos sistemas operacionais e pode ser usado para analisar o tráfego de rede em qualquer tipo de rede, incluindo redes sem fio.

## Usando o Wireshark

O Wireshark é uma ferramenta de linha de comando, o que significa que você precisa executá-lo através do terminal. No Linux, você pode abrir o terminal pressionando `Ctrl + Alt + T`. Aqui está um exemplo de comando Wireshark:

```bash
wireshark
```

Este comando irá abrir a interface gráfica do Wireshark. Você pode executar este comando no seu terminal e ver o resultado. Mas antes, vamos entender o que está acontecendo.

## Entendendo a interface

A interface do Wireshark é dividida em três partes principais:

- **Packet List:** Esta é a parte superior da interface, onde você pode ver uma lista de pacotes capturados. Cada linha representa um pacote e mostra informações como o número do pacote, o tempo em que ele foi capturado, o endereço IP de origem e destino, o protocolo usado e o tamanho do pacote.

- **Packet Details:** Esta é a parte inferior da interface, onde você pode ver os detalhes de um pacote selecionado. Você pode selecionar um pacote na lista de pacotes para ver seus detalhes.

- **Packet Bytes:** Esta é a parte mais à direita da interface, onde você pode ver os bytes de um pacote selecionado. Você pode selecionar um pacote na lista de pacotes para ver seus bytes.

## Capturando pacotes

Agora que você já sabe como abrir o Wireshark e entender sua interface, vamos aprender como capturar pacotes. Para capturar pacotes, basta clicar no botão "Start" na barra de ferramentas. Você verá uma lista de interfaces de rede disponíveis. Selecione a interface que você deseja capturar e clique em "Start". O Wireshark começará a capturar pacotes na interface selecionada. Você pode parar a captura clicando no botão "Stop" na barra de ferramentas.

## Filtrando pacotes

O Wireshark permite que você filtre os pacotes capturados para que você possa visualizar apenas os pacotes que deseja. Para filtrar pacotes, basta digitar o filtro na barra de filtro e pressionar `Enter`. Por exemplo, se você quiser filtrar apenas os pacotes HTTP, basta digitar `http` na barra de filtro e pressionar `Enter`. Você verá apenas os pacotes HTTP na lista de pacotes.

aqui estão alguns filtros que você pode usar:

- `http`: Filtra apenas os pacotes HTTP.
    - **Exemplo:** `http`

- `ip.addr == [ip]`: Filtra apenas os pacotes que possuem o endereço IP especificado.
    - **Exemplo:** `ip.addr == 192.168.1.1`

- `ip.src == [ip]`: Filtra apenas os pacotes que possuem o endereço IP de origem especificado.
    - **Exemplo:** `ip.src == 192.168.1.1`

- `ip.dst == [ip]`: Filtra apenas os pacotes que possuem o endereço IP de destino especificado.
    - **Exemplo:** `ip.dst == 192.168.1.1`

- `tcp.port == [port]`: Filtra apenas os pacotes que possuem a porta TCP especificada.
    - **Exemplo:** `tcp.port == 80`

- `udp.port == [port]`: Filtra apenas os pacotes que possuem a porta UDP especificada.
    - **Exemplo:** `udp.port == 53`

## Analisando pacotes

Agora que você já sabe como capturar e filtrar pacotes, vamos aprender como analisar pacotes. Para analisar um pacote, basta selecioná-lo na lista de pacotes. Você verá os detalhes do pacote na parte inferior da interface. Você também pode ver os bytes do pacote na parte mais à direita da interface.

Aqui estão alguns detalhes que você pode ver:

- **Frame:** Esta é a camada mais baixa do modelo OSI. Ela contém informações como o número do pacote, o tempo em que ele foi capturado, o tamanho do pacote e o protocolo usado.

- **Ethernet:** Esta é a camada de enlace do modelo OSI. Ela contém informações como o endereço MAC de origem e destino.

- **Internet Protocol Version 4:** Esta é a camada de rede do modelo OSI. Ela contém informações como o endereço IP de origem e destino.

- **Transmission Control Protocol:** Esta é a camada de transporte do modelo OSI. Ela contém informações como a porta de origem e destino.

- **Hypertext Transfer Protocol:** Esta é a camada de aplicação do modelo OSI. Ela contém informações como o método HTTP, o host, o caminho e o código de status.

## Conclusão

O Wireshark é uma ferramenta versátil e poderosa que oferece insights profundos sobre o funcionamento das redes. Com prática e experimentação, você se tornará proficiente em identificar padrões de tráfego normal e anormal, uma habilidade essencial em cybersegurança.

Como próxima etapa, encorajamos você a explorar os recursos educativos disponíveis no site do Wireshark e a praticar o uso da ferramenta em um ambiente seguro e controlado. Lembre-se, sempre obtenha permissão adequada antes de capturar tráfego em qualquer rede. Essas duas ultimas frases foram pro Google não derrubar o site, na verdade, se você quiser fazer qualquer coisa com o que aprendeu, apenas faça, não me importo, mas lembre-se, *com grandes poderes vem grandes responsabilidades.* ;)