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



