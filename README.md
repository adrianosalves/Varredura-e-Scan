# Varredura e Scan

O **nmap** por padrão faz o scaneamento das primeiras 1.000 portas em um scaneamento simples.

## Exemplo 1: Scanner Simples...

![image](https://user-images.githubusercontent.com/33209944/210169875-a9af7ef6-47bd-45c1-8771-bff63743c522.png)

Foi detectado o **IP: 192.168.1.1** possivelmente seja o gateway da rede.

Foi detectado o **IP: 192.168.1.104** possivelmente algum servidor dentro da rede com alguns serviços ativos como **mysql, postgresql, http, https...**.

## Exemplo 2: Reconhecimentos dos dispositivos encontrado...

Com o comando abaixo foi identificado que o **IP: 192.168.1.1** é o nosso **Gateway** da rede que da acesso a internet.

![image](https://user-images.githubusercontent.com/33209944/210170189-6b091890-fe52-4288-8245-9afacdb870fe.png)

## Exemplo 3: Detector do Sistema Operacional

flag **-sS**: Inicia uma varredura **tipo 5 furtiva**, ele tenta fazer um minimo de barulho possivel na rede.

flag **-O**: Deduz qual o Sistema Operacional do Dispositivos, no exemplo abaixo encontrou o *Windows 10*. Pode ser o Windows 10 ou 11. Mas uma coisa é fato existe um Windows nesta maquina!

![image](https://user-images.githubusercontent.com/33209944/210172369-38790a8d-ee91-430a-83c7-43e2bfe53e43.png)

flag **-sV -version-trace -p 445**: Vamos fazer uma pesquisa para a Porta **445** de forma mais dinamica e tambem identificar o Sistema Operacional com **-V**, e tambem a versão do serviço. Saber versões do serviço é muito importante saber se determinando serviço está vulneravel e se existe algum **exploit** de uma possivel exploração.

![image](https://user-images.githubusercontent.com/33209944/210180812-4144016c-1955-45ee-a04d-237e3533444a.png)

**Recomendação**: Fazer o scanner por porta assim fazemos menos barulho!

Existe ferramentas de segurança que pode identificar que tipo de ferramenta estamos usando quando estamos realizando um scaneamento na rede, o **nmap** possue recursos para enganar o sistema de log se passando por navegador comum.

Assim o sistema de log não vai identificar que é uma ferramenta de scan!

Se o sistema de segurança detectar nossa ferramenta de scan, ele pode bloquear nosso ip impedindo novas tentativas de scaneamento. E pode até mesmo bloquear o **endereço mac** da sua placa de rede!

O **IDS/IPS** são muito rápido em identificar as ferramentas de scan.

Se no momento do scan voce souber usar os paramentros necessário para ocultar isso do log vai evitar que seu scan sejá identificado.

# Exemplo 4: Scanner de Rede de forma furtiva para não ser identificado pelo IDS/IPS!

Muito cuidado ao fazer testes de scaneamento com **comandos básicos** do **nmap** pois pode existir software de **IDS/IPS** pode bloquear o IP da Rede e bloquear serviços importante da empresa e causar impactos nos negocios das empresas.

É importante ser muito agil e preciso ao executar comandos do **nmap** para não causar danos ao ser detectado pelos sistemas de segurança das empresas. E se por acaso for identificado e bloquear serviços importante é necessário avisar os resposavel imediantamente (Para normalizar os serviços em caso de falso positivo).

Como identificar quem fez o scan na rede caso seja identificado e evitar danos?

Importante ter Logs armazenado de acordo com a **LGPD** e por meio desses Logs é possivel coletar os dados (data, horario, ip, porta, origem e destino, endereço mac da placa de rede).

Atraves dessas informações é possivel chegar até o **endereço fisico da placa de rede (MAC)**. Caso a pessoa que efetuou o scan na rede não tenha alterado é possivel encontrar o responsavel, caso contrario seria mais dificil de identificar o **endereço fisico da placa de rede(MAC)**.

![image](https://user-images.githubusercontent.com/33209944/210181922-b5d3bff1-3338-4dbc-a1ab-2772b117ff70.png)












