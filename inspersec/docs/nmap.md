# Conhecendo o Nmap

---

O Nmap, também conhecido como “Network Mapper”, é uma ferramenta open-source usada para explorar e auditar a segurança de redes de computadores. Vamos explorar essa ferramenta essencial passo a passo, conhecendo alguns comandos e suas funções para ajudar você a começar com segurança no mundo da cybersegurança.

## Instalando o Nmap

O Nmap é uma ferramenta open-source, o que significa que você pode baixá-lo gratuitamente. Para instalar o Nmap no Windows, basta baixar o instalador no site oficial e seguir as instruções (Apenas por curiosidade, não vamos usar o Windows). No Linux, você pode instalar o Nmap através do gerenciador de pacotes da sua distribuição. No Ubuntu, por exemplo, basta executar o comando `sudo apt install nmap` no terminal.

## Usando o Nmap

O Nmap é uma ferramenta de linha de comando, o que significa que você precisa executá-lo através do terminal. No Linux, você pode abrir o terminal pressionando `Ctrl + Alt + T`. Aqui está um exemplo de comando Nmap:

```bash
nmap scanme.nmap.org
```

Este comando irá escanear o site `scanme.nmap.org` e retornar informações sobre os serviços que estão rodando na máquina. Você pode executar este comando no seu terminal e ver o resultado. Mas antes, vamos entender o que está acontecendo.

## Entendendo o comando

O comando `nmap` é usado para executar o Nmap. O que vem depois do comando é o alvo do escaneamento, que pode ser um IP ou um domínio. No nosso caso, o alvo é o domínio `scanme.nmap.org`. Você pode substituir este domínio por qualquer outro que desejar.

## Entendendo o resultado

O resultado do comando acima deve ser algo parecido com isto:

```bash
Starting Nmap 7.80 ( https://nmap.org ) at 2020-04-20 16:00 -03
Nmap scan report for scanme.nmap.org (

Host is up (0.11s latency).
Other addresses for scanme.nmap.org (not scanned): 2600:3c01::f03c:91ff:fe18:bb2f
Not shown: 996 filtered ports
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
9929/tcp open  nping-echo
31337/tcp open  Elite

Nmap done: 1 IP address (1 host up) scanned in 10.06 seconds
```

A primeira linha mostra a versão do Nmap que está sendo usada. A segunda linha mostra o alvo do escaneamento. A terceira linha mostra o endereço IP do alvo e o tempo de latência. A quarta linha mostra outros endereços IP do alvo que não foram escaneados. A quinta linha mostra o número de portas que não foram escaneadas. A sexta linha mostra as portas que foram escaneadas, o estado delas e o serviço que está rodando em cada uma. A sétima linha mostra o tempo que o escaneamento levou para ser concluído.

## Explorando mais comandos

Agora que você já sabe como executar o Nmap e interpretar o resultado, vamos dar uma olhada em alguns comandos basicos que você pode usar para explorar ainda mais o Nmap.

- `nmap -sP [alvo]`:
    - **Descrição:** Este comando é utilizado para fazer um ping scan, identificando quais hosts estão online na rede especificada.
    - **Exemplo:** `nmap -sP 192.168.1.0/24`

- `nmap -sT [alvo]`:
    - **Descrição:** Este comando é utilizado para fazer um TCP connect scan, que é o tipo de escaneamento mais básico. Ele tenta estabelecer uma conexão com cada porta do alvo e determinar se ela está aberta ou fechada.
    - **Exemplo:** `nmap -sT scanme.nmap.org`

- `nmap -sU [alvo]`:
    - **Descrição:** Este comando é utilizado para fazer um UDP scan, que é usado para identificar portas UDP abertas no alvo.
    - **Exemplo:** `nmap -sU scanme.nmap.org`

- `nmap -sS [alvo]`:
    - **Descrição:** Este comando é utilizado para fazer um TCP SYN scan, que é um tipo de escaneamento stealth. Ele envia um pacote SYN para cada porta do alvo e analisa a resposta para determinar se a porta está aberta ou fechada.
    - **Exemplo:** `nmap -sS scanme.nmap.org`

- `nmap -sV [alvo]`:
    - **Descrição:** Este comando é utilizado para fazer um service scan, que é usado para identificar os serviços que estão rodando em cada porta do alvo.
    - **Exemplo:** `nmap -sV scanme.nmap.org`

- `nmap -O [alvo]`:
    - **Descrição:** Este comando é utilizado para fazer um OS detection scan, que é usado para identificar o sistema operacional do alvo.
    - **Exemplo:** `nmap -O scanme.nmap.org`

- `nmap -A [alvo]`:
    - **Descrição:** Este comando é utilizado para fazer um aggressive scan, que é usado para identificar o sistema operacional do alvo, os serviços que estão rodando em cada porta e as versões desses serviços.
    - **Exemplo:** `nmap -A scanme.nmap.org`

**Alguns Comandos Auxiliares:**

- `nmap -p [portas] [alvo]`:
    - **Descrição:** Este comando é utilizado para especificar quais portas devem ser escaneadas.
    - **Exemplo:** `nmap -p 80,443 scanme.nmap.org`

- `nmap -oN [arquivo] [alvo]`:
    - **Descrição:** Este comando é utilizado para salvar o resultado do escaneamento em um arquivo.
    - **Exemplo:** `nmap -oN resultado.txt scanme.nmap.org`

- `nmap -script [script] [alvo]`:
    - **Descrição:** Este comando é utilizado para executar um script do Nmap.
    - **Exemplo:** `nmap -script http-headers scanme.nmap.org`

- `nmap -v [alvo]`:
    - **Descrição:** Este comando é utilizado para executar o Nmap em modo verbose, que mostra mais informações sobre o escaneamento.
    - **Exemplo:** `nmap -v scanme.nmap.org`

- `nmap -h`:
    - **Descrição:** Este comando é utilizado para mostrar a lista de comandos do Nmap.
    - **Exemplo:** `nmap -h`

## Conclusão

O Nmap é uma ferramenta essencial para qualquer profissional de cybersegurança. Neste módulo, você aprendeu como instalar e usar o Nmap, além de conhecer alguns comandos básicos. Agora que você já sabe como usar o Nmap, é hora de praticar! Execute o Nmap em diferentes alvos e explore os resultados. Você também pode pesquisar sobre os comandos que não foram abordados neste módulo e testá-los. Lembre-se de que a prática é a melhor maneira de aprender! E pratique onde quiser, eu não sou ninguem pra te falar qual site pode e não pode, fique a vontade para instaurar o caos na internet, mas lembre-se, *com grandes poderes vem grandes responsabilidades.*