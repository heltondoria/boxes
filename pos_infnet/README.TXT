Pré-requisitos:
  - Virtualbox 5.0 ou inferior
  - Vagrant
  - Arquivo Vagrantfile distribuído por mim via dropbox

Passos para instalação e utilização da VM:
 
 1 - Garantir que tem uma versão adequada de Virtualbox. O Vagrant não trabalha 
 ainda com a versão mais nova (5.1), então, caso sua versão seja posterior à 5.0, 
 desinstale e baixe uma nova. Durante o processo de montagem dessa VM, utilizei 
 a versão 5.0.24 com Oracle VM Extension Pack. Os instaladores e extensões para
 versões mais antigas de Virtualbox podem ser encontradas em:
 
 https://www.virtualbox.org/wiki/Download_Old_Builds_5_0 
   
 2 - Baixe e instale o Vagrant. O site é bem simples e explicativo sobre como 
 usá-lo. Ele pode ser encontrado em: https://www.vagrantup.com

 3 - Copie o arquivo Vagranfile que compartilhei para a pasta a partir da qual
 pretenda iniciar a VM. O processo de construção inicial da VM é via terminal,
 mas, depois de pronta, ela poderá ser iniciada diretamente através da interface
 gráfica do VirtualBox. A pasta onde você irá colocar o arquivo Vagrantfile é 
 importante porque ela será mapeada dentro da VM permitindo a troca de arquivos
 entre o sistema hóspede e o hospedeiro. Ou seja, tudo o que você colocar nessa 
 pasta, será visível dentro da VM.

 4 - Entre na pasta escolhida usando o terminal e gigite o comando "vagrant up".
 Esse processo pode demorar vários minutos, dependendo da sua conexão e da sua
 máquina. 

 5 - Ao terminar o processo de intallação, ele vai executar a VM e abri-la em 
 modo gráfico. É importante prestar muita atenção nesse ponto porque será exibida
 uma tela popup perguntando como pretende usar as barras de botões. Escolham 
 sempre a primeira opção que diz "Use default config". Se escolherem a  segunda, 
 vão ficar sem a barra de menus que dá acesso aos programas. 

 6 - Abrir o spyder clicando no menu no canto superior esquerdo, e procurando 
 por ele menu "development". Eu já deixei instalado o Python 3,5 e a biblioteca 
 NLTK, porém, vocês ainda terão que realizar aqueles passos de download do módulo
 Book, como fizemos em sala de aula. Para quem não lembra, basta criar digitar 
 no editor as seguintes linhas e pressionar F5:
 
 import nltk

 nltk.download()
 

 Se, ao apertar F5 ele não executar alegando que você precisa escolher uma console
 Python onde o programa será executado, basta ir na barra de menus do spyder, clicar 
 no menu "Consoles" e escolher uma das opções.


Considerações finais: 

- O sistema instalado na máquina virtual é um Debian 8.2 (também conhecido como 
Debian Jessie)

- O ambiente gráfico escolhido foi o xfce4. Ele não é tão bonito, mas é leve e 
deve funcionar rápido nas máquinas de todos. 

- Para facilitar a vida dos colegas, eu, propositalmente, coloquei para não haver 
tela de login, porém, ao finalizar o sistema, ainda será solicitada um senha de 
autorização. O usuário que vocês estarão usando é o "vagrant" com senha "vagrant".

- Dentro da VM, vocês encontrarão a pasta que pode ser usada para trocar arquivos 
entre a VM e a máquina real no caminho /vagrant (não confundir com a home do 
usuário vagrant que fica em /home/vagrant)

- Se algo der errado, como, por exemplo, escolher a opção errada naquele popup 
inicial, basta destruir a VM e criá-la de novo. Para isso, estando com a VM 
desligada, basta abrir o terminal entrar na pasta onde se encontra o comando 
arquivo Vagrantfile e digitar "vagrant destroy -f". Para recriá-la, o processo 
é o mesmo de antes, basta digitar vagrant up. 

- Se vocês executarem o comando "vagrant up" com a VM já criada, ela apenas abrirá 
a VM, sem realizar aquele processo inicial de construção. 

- O comando para desligar a VM pelo terminar é "vagrant halt".

- O sistema está em inglês (incluindo o layout do teclado), mas isso pode ser alterado
indo em "Settings" no menu do sistema.  

- A VM foi configurada para usar apenas um núcleo de processador (fica mais rápido 
assim no virtualbox) e 1/4 da memória RAM da máquina hospedeira. Se quiserem mudar 
esses parâmetros, me procurem que explico como alterar esses valores. 
