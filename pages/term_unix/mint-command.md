[[Página Inicial](../prog_c/home.md)]

---

## Comandos para usar no Terminal Linux

---

---

Glossário:

<code style="color : dodgerblue">Comandos de Teclado</code>

<code style="color : greenyellow">Comandos no Terminal</code>


---


---

<code style="color : yellow">Iniciando Shells</code>

---


Informação|Comando
|---|---|
Como abrir uma nova tela pelo Teclado|<code style="color : dodgerblue">CTRL + ALT + T</code>
Limpando a tela do Terminal|<code style="color : greenyellow">clear</code>

---

<code style="color : yellow">Instalação de Programas</code>

---

Informação|Comando
|---|---|
Ativando permição de Super user|<code style="color : greenyellow">sudo su</code>
Ativando permição Temporária|<code style="color : greenyellow">sudo comando</code>
Instalando um Programa|<code style="color : greenyellow">apt-get install nome_programa</code>
Desinstalando um programa e seus Diretórios|<code style="color : greenyellow">apt-get --purge remove nome_programa</code>
Desinstalando somente o Programa|<code style="color : greenyellow">apt-get remove nome_programa</code>
Desinstalando Pacotes Desnecessários|<code style="color : greenyellow">apt-get autoremove</code>
Vendo todos os programas instalados|<code style="color : greenyellow">dpkg --list</code>

---

<code style="color : yellow">Informações do Sistema no Terminal</code>

---

Informação|Comando
|---|---|
Verificar Data e Tempo Atual|<code style="color : greenyellow">date</code>
Para saber quem é o Usuário no Sistema|<code style="color : greenyellow">whoami</code>
Para saber Informação do Kernel|<code style="color : greenyellow">uname -a</code>
Para saber Informação do CPU|<code style="color : greenyellow">cat /proc/cpuinfo</code>
Para saber Informação da Memoria|<code style="color : greenyellow">cat /proc/meminfo</code>
Para saber quanto ja foi usado do Disco|<code style="color : greenyellow">df -h</code>
Para ler o Manual de um Comando ou Programa|<code style="color : greenyellow">man nome_programa</code>
Para Navegar pelo Terminal para ler todas as Informações|<code style="color : dodgerblue">SHIFT + PAGE UP/PAGE DOWN</code>

---

<code style="color : yellow">Comandos de Controle dos Diretórios</code>

---

Informação|Comando
|---|---|
Para abrir um Diretório no GUI|<code style="color : greenyellow">xdg-open /caminho/pro/diretorio</code>
Como mudar de Diretório|<code style="color : greenyellow">cd nome_diretorio</code>
Como mostrar todos os Arquivos e Diretórios do Diretório Atual|<code style="color : greenyellow">ls -la</code>
Como mostrar Arquivos de uma Extensao Especifica|<code style="color : greenyellow">ls *.extensao</code>
Como criar um Diretório novo no Diretório Atual|<code style="color : greenyellow">mkdir nome_diretorio</code>
Para Deletar um Diretório Vazio|<code style="color : greenyellow">rmdir nome_diretorio</code>
Para Deletar um Diretório com Informações|<code style="color : greenyellow">rm -rf nome_diretorio</code>
Para saber o caminho até o Diretório atual|<code style="color : greenyellow">pwd</code>
Para copiar um arquivo em um novo Diretório|<code style="color : greenyellow">cp nome_arquivo /caminho/para/diretorio</code>
Para mover um arquivo em um novo Diretório|<code style="color : greenyellow">mv caminho/para/arquivo caminho/para/diretorio/novo</code>

---

<code style="color : yellow">Leitura e Renomeio de Arquivos</code>

---

Informação|Comando
|---|---|
Para copiar um arquivo em um novo Diretório|<code style="color : greenyellow">cp nome_arquivo /caminho/para/diretorio</code>
Para mover um arquivo em um novo Diretório|<code style="color : greenyellow">mv /caminho/do/arquivo /novo/diretorio/</code>
Para ler um arquivo no Shell|<code style="color : greenyellow">cat nome_programa</code>
Para ler um arquivo no Programa Nano|<code style="color : greenyellow">nano nome_arquivo.extensao</code>
Para ler um arquivo no Programa VIM/VI|<code style="color : greenyellow">vi/vim nome_arquivo.extensao</code>
Para renomear um Arquivo no Shell|<code style="color : greenyellow">mv nome_antigo.extensao nome_novo.extensao</code>

---

<code style="color : yellow">Comandos de Compressão</code>

---

Informação|Comando
|---|---|
Para criar um Arquivo .tar adicionando um arquivo|<code style="color : greenyellow">tar cf nome_tar.tar arquivo</code>
Extrair Arquivos de um tar|<code style="color : greenyellow">tar xf nome_tar.tar</code>
Extrair Arquivos de um tar.gz|<code style="color : greenyellow">tar xzf nome_tar_gz.tar.gz</code>
Criar Arquivo .gz|<code style="color : greenyellow">gzip nome_arquivo</code>
Extrair arquivo .gz|<code style="color : greenyellow">gzip -d nome_arquivo.gz</code>

---

<code style="color : yellow">Comandos de Conexão Network</code>

---

Informação|Comando
|---|---|
Listar todos os IPs das Maquinas Locais|<code style="color : greenyellow">ifconfig</code>
Baixar um arquivo da internet|<code style="color : greenyellow">wget nome_arquivo</code>
Como descompactar um Arquivo .deb|<code style="color : greenyellow">dpkg -i caminho/ate/o/arquivo</code>
Como abrir uma Página de Internet pelo Terminal|<code style="color : greenyellow">xdg-open caminho_para_site</code>
