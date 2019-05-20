[[Página Inicial](../term_unix/home.md)]

---

## Comandos para usar no Terminal Linux

---

---

Glossário:

<code style="color : red">Programa do Terminal</code>

<code style="color : dodgerblue">Comandos de Teclado</code>

<code style="color : greenyellow">Comandos no Terminal</code>


---


---

<code style="color : yellow">Iniciando Shells</code>

---


Informação|Comando
|---|---|
Como abrir uma nova tela pelo Teclado|<code style="color : dodgerblue">CTRL + ALT + T</code>
Limpando a tela do Terminal|<code style="color : greenyellow"><code style="color : red">clear</code></code>

---

<code style="color : yellow">Instalação de Programas</code>

---

Informação|Comando
|---|---|
Ativando permição de Super user|<code style="color : greenyellow"><code style="color : red">sudo</code> su</code>
Ativando permição Temporária|<code style="color : greenyellow"><code style="color : red">sudo</code> comando</code>
Instalando um Programa|<code style="color : greenyellow"><code style="color : red">apt-get</code> install nome_programa</code>
Desinstalando um programa e seus Diretórios|<code style="color : greenyellow"><code style="color : red">apt-get</code> --purge remove nome_programa</code>
Desinstalando somente o Programa|<code style="color : greenyellow"><code style="color : red">apt-get</code> remove nome_programa</code>
Desinstalando Pacotes Desnecessários|<code style="color : greenyellow"><code style="color : red">apt-get</code> autoremove</code>
Vendo todos os programas instalados|<code style="color : greenyellow"><code style="color : red">dpkg</code> --list</code>

---

<code style="color : yellow">Informações do Sistema no Terminal</code>

---

Informação|Comando
|---|---|
Verificar Data e Tempo Atual|<code style="color : greenyellow"><code style="color : red">date</code></code>
Para saber quem é o Usuário no Sistema|<code style="color : greenyellow"><code style="color : red">whoami</code></code>
Para saber Informação do Kernel|<code style="color : greenyellow"><code style="color : red">uname -a</code></code>
Para saber Informação do CPU|<code style="color : greenyellow"><code style="color : red">cat</code> /proc/cpuinfo</code>
Para saber Informação da Memoria|<code style="color : greenyellow"><code style="color : red">cat</code> /proc/meminfo</code>
Para saber quanto ja foi usado do Disco|<code style="color : greenyellow"><code style="color : red">df</code> -h</code>
Para ler o Manual de um Comando ou Programa|<code style="color : greenyellow"><code style="color : red">man</code> nome_programa</code>
Para Navegar pelo Terminal para ler todas as Informações|<code style="color : dodgerblue">SHIFT + PAGE UP/PAGE DOWN</code>

---

<code style="color : yellow">Comandos de Controle dos Diretórios</code>

---

Informação|Comando
|---|---|
Para abrir um Diretório no GUI|<code style="color : greenyellow"><code style="color : red">xdg-open</code> /caminho/pro/diretorio</code>
Como mudar de Diretório|<code style="color : greenyellow"><code style="color : red">cd</code> nome_diretorio</code>
Como mostrar todos os Arquivos e Diretórios do Diretório Atual|<code style="color : greenyellow"><code style="color : red">ls</code> -la</code>
Como mostrar Arquivos de uma Extensao Especifica|<code style="color : greenyellow"><code style="color : red">ls</code> *.extensao</code>
Como criar um Diretório novo no Diretório Atual|<code style="color : greenyellow"><code style="color : red">mkdir</code> nome_diretorio</code>
Para Deletar um Diretório Vazio|<code style="color : greenyellow"><code style="color : red">rmdir</code> nome_diretorio</code>
Para Deletar um Diretório com Informações|<code style="color : greenyellow"><code style="color : red">rm -rf</code> nome_diretorio</code>
Para saber o caminho até o Diretório atual|<code style="color : greenyellow"><code style="color : red">pwd</code></code>
Para copiar um arquivo em um novo Diretório|<code style="color : greenyellow"><code style="color : red">cp</code> nome_arquivo /caminho/para/diretorio</code>
Para mover um arquivo em um novo Diretório|<code style="color : greenyellow"><code style="color : red">mv</code> caminho/para/arquivo caminho/para/diretorio/novo</code>

---

<code style="color : yellow">Leitura e Renomeio de Arquivos</code>

---

Informação|Comando
|---|---|
Para copiar um arquivo em um novo Diretório|<code style="color : greenyellow"><code style="color : red">cp</code> nome_arquivo /caminho/para/diretorio</code>
Para mover um arquivo em um novo Diretório|<code style="color : greenyellow"><code style="color : red">mv</code> /caminho/do/arquivo /novo/diretorio/</code>
Para ler um arquivo no Shell|<code style="color : greenyellow"><code style="color : red">cat</code> nome_programa</code>
Para ler um arquivo no Programa Nano|<code style="color : greenyellow"><code style="color : red">nano</code> nome_arquivo.extensao</code>
Para ler um arquivo no Programa VIM/VI|<code style="color : greenyellow"><code style="color : red">vi/vim</code> nome_arquivo.extensao</code>
Para renomear um Arquivo no Shell|<code style="color : greenyellow"><code style="color : red">mv</code> nome_antigo.extensao nome_novo.extensao</code>

---

<code style="color : yellow">Comandos de Compressão</code>

---

Informação|Comando
|---|---|
Para criar um Arquivo .tar adicionando um arquivo|<code style="color : greenyellow"><code style="color : red">tar</code> cf nome_tar.tar arquivo</code>
Extrair Arquivos de um tar|<code style="color : greenyellow"><code style="color : red">tar</code> xf nome_tar.tar</code>
Extrair Arquivos de um tar.gz|<code style="color : greenyellow"><code style="color : red">tar</code> xzf nome_tar_gz.tar.gz</code>
Criar Arquivo .gz|<code style="color : greenyellow"><code style="color : red">gzip</code> nome_arquivo</code>
Extrair arquivo .gz|<code style="color : greenyellow"><code style="color : red">gzip</code> -d nome_arquivo.gz</code>

---

<code style="color : yellow">Comandos de Conexão Network</code>

---

Informação|Comando
|---|---|
Listar todos os IPs das Maquinas Locais|<code style="color : greenyellow"><code style="color : red">ifconfig</code></code>
Baixar um arquivo da internet|<code style="color : greenyellow"><code style="color : red">wget</code> nome_arquivo</code>
Como descompactar um Arquivo .deb|<code style="color : greenyellow"><code style="color : red">dpkg</code> -i caminho/ate/o/arquivo</code>
Como abrir uma Página de Internet pelo Terminal|<code style="color : greenyellow"><code style="color : red">xdg-open</code> caminho_para_site</code>
