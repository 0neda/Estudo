# 1. Introdução ao Linux

## Histórico

> [!NOTE]
> ### Histórico do UNIX ao Linux
>- **Unix** surgiu em 1969 como um sistema operacional multiusuário e multitarefa.
>- **Linus Torvalds** desenvolveu o kernel Linux em 1991 para computadores pessoais, baseado em UNIX.
>- Inicialmente compartilhado na Internet, o Linux cresceu rapidamente graças à colaboração global.
>- Em menos de 10 anos, o kernel 2.4 foi lançado, com suporte a múltiplos dispositivos e plataformas (i386, Sparc, PowerPC, etc.).
><br>
>
> ### Linux hoje e seu desenvolvimento
>- O desenvolvimento do Linux é centralizado por Linus Torvalds.
>- Qualquer pessoa no mundo pode colaborar com o kernel, que está sob a GPL.
><br>
>
>_GPL (Gnu Public License) é a licença criada por Stallman, que permite a distribuição do código e do programa livremente, e permite a alteração, sob algumas condições._
><br>
>
> ### Estrutura do Linux
> _Mas o que é Linux? Kernel, utilitários, etc_
>- **Kernel**: O núcleo do sistema que interage diretamente com o hardware. É responsável por gerenciar recursos do sistema.
>- **Utilitários**: Ferramentas e programas que permitem a interação com o sistema, como shells e editores de texto.

---
<br>

## Sistema de Arquivos
>[!NOTE]
> ### Sistemas de arquivos, discos, arquivos e diretórios
>- 1 byte = 8 bits. 1 bit assume valor 0 ou 1.
>- Discos magnéticos: divididos em trilhas (circulares), e cada trilha é dividida em setores. Um setor, em geral, tem 512 bytes.
>- Utilização do conceito de **arquivos e diretórios.**
><br>
>
>Arquivo: um conjunto de setores no disco, associado a um nome
>- O arquivo nada mais é que uma sequência de bits (0 e 1), mas que podem assumir diversos tipos (arquivo binário, arquivo texto, etc).
><br>
>
>Cada sistema permite uma maneira de organizar os discos e arquivos. o UNIX e o Linux utilizam a estrutura de árvores.
><br>
>
>Para o agrupamento de arquivos, existe o conceito de diretório.
><br>
>
>Árvore: o sistema contém apenas um diretório Raiz (root), e todos outros estão "dentro" da raiz.
>- Um diretório pode conter vários diretórios.

<br>

## Conceito de Multiusuário
>[!NOTE]
>#### Conceitos de usuário e senha Sistema multi-usuário e proteção
>- O UNIX e o Linux incorporam o conceito de multiusuário, onde cada uma deve ter acesso restrito aos recursos.
>- Cada usuário tem um ID no sistema, associado a um username.
>- Para acessar a máquina, o usuário possui uma senha.

<br>

## Sobrevivência no Linux
>[!NOTE]
>#### Palavra essencial: MANUAIS
>- `man <comando>`
>- `man -k <palavra>` ou `apropos <palavra>`
><br>
>
>#### Tecla importante:
>- Control + C ->Encerrar terminal
><br>
>
>#### Comandos
>- `pwd`: exibe a localização na árvore de diretórios
>- `passwd`: altera a senha
>- `su/sudo`: entra no modo super usuário
>- `ls`: lista os arquivos e diretórios
>- `mkdir`: cria um diretório
>- `rm`: remove um diretório

---
<br>

# 2. Gerenciamento de Sistemas Operacionais

## Interface e Hardware
>[!NOTE]
>#### Partes do Sistema Operacional
>- **Gerenciador de Dispositivos**: Controla o funcionamento dos dispositivos conectados ao sistema.
>- **Conceito de IRQ (Interrupção)**: Permite que dispositivos de hardware interrompam o processador para atenção imediata.
>- **Mapeamento de Hardware**: Processo de alocação de recursos de hardware para garantir que os dispositivos funcionem corretamente.

<br>

## Tipos de Sistemas
>[!NOTE]
>#### Classificações
>- **Usuário**: Sistemas voltados para uso pessoal.
>- **Servidor**: Sistemas projetados para fornecer serviços a outros computadores em uma rede.

<br>

## Desempenho e Segurança
>[!NOTE]
>#### Desempenho
>- Linux tem aproximadamente 40% de velocidade superior na questão de banco de dados em relação ao Windows.

>[!TIP]
>#### Segurança
>- Linux é possivelmente mais seguro, mas existem mais profissionais especializados em Linux, o que pode de certa forma facilitar a invasão.
>- Em resumo, ambos são bem compatíveis, mas, de forma breve, Linux é mais recomendado.

---
<br>

# 3. Estrutura de Arquivos e Diretórios

## Unidades de Armazenamento
>[!NOTE]
>#### Estrutura de Armazenamento
>- **Setor de Disco**: Unidade mínima de armazenamento em discos, geralmente 512 bytes.
>- **Cluster**: Múltiplos setores formam um cluster, a menor unidade de espaço que pode ser alocada.

<br>

## Atributos de Arquivos
>[!NOTE]
>#### O que um arquivo possui?
>- **Nome**: Identificador do arquivo, que pode ser case sensitive.
>- **Atributos**: Incluem tipo, tamanho, proteção, data/hora de criação ou modificação.
>- **Estrutura Interna**: Sequência de bytes ou registros, que podem ser interpretados de diferentes formas.

<br>

## Sistemas de Arquivos
>[!TIP]
>#### Linux
>- **EXT2**: Não possui journaling, adequado para dispositivos de armazenamento menores.
>- **EXT3**: Adiciona journaling, o que melhora a recuperação após falhas.
>- **EXT4**: Suporta volumes e arquivos maiores, melhor desempenho e eficiência.
>- **ReiserFS**: Bom para manipulação de muitos arquivos pequenos, mas menos usado atualmente.
><br>
>
>#### Windows
>- **NTFS**: Sistema de arquivos avançado do Windows, com suporte para grandes volumes e arquivos, e segurança integrada.
>- **FAT32**: Sistema antigo, com limitação de 4GB por arquivo.
>- **ReFS**: Sistema mais recente da Microsoft, projetado para resiliência.

<br>

## Comandos de Arquivos
>[!NOTE]
>#### Comandos para Gerenciamento de Arquivos
>- **chmod**: Altera permissões de arquivos e diretórios.
>- **useradd/addgroup**: Gerencia usuários e grupos no sistema.

---
<br>

# 4. Gerenciamento de Recursos no Linux

## Processos
>[!NOTE]
>#### Comunicação entre Processos (IPC)
>1. Utiliza técnicas como memória compartilhada, pipes, sinais, semáforos e filas de mensagens.
>2. Comandos:
>  - `ps`: Lista processos em execução.
>  - `top`: Monitora processos em tempo real.
>  - `kill`: Envia sinais para processos, terminando-os se necessário.
>  - `nice`: Ajusta a prioridade de um processo.

<br>

## Memória
>[!NOTE]
>#### Gerenciamento de Memória
>1. **Memória Física (RAM)** e **Memória Virtual (swap)**: O kernel gerencia a alocação de memória para processos, movendo dados para swap quando necessário.
>2. **Monitoramento**:
>  - `free`: Mostra o uso de memória.
>  - `vmstat`: Fornece estatísticas sobre memória virtual e sistema.

---
<br>

# 5. Comandos Essenciais no Linux

| Comando         | Função                                                                                  |
|--|--|
| `df`            | Exibe o espaço em disco usado e disponível em sistemas de arquivos.                     |
| `dmesg`         | Exibe mensagens do kernel, útil para ver logs do sistema, como discos conectados.       |
| `fdisk`         | Manipula tabelas de partição de disco.                                                  |
| `mkfs.ext3`     | Formata uma partição para o sistema de arquivos ext3.                                   |
| `tune2fs`       | Ajusta parâmetros de sistemas de arquivos ext2/ext3/ext4.                               |
| `blkid`         | Exibe o UUID de dispositivos, útil para configurar o fstab.                             |
| `mkdir`         | Cria um novo diretório.                                                                 |
| `cd`            | Navega entre diretórios.                                                                |
| `ls`            | Lista arquivos e diretórios.                                                            |
| `touch`         | Cria arquivos vazios ou atualiza timestamps de arquivos existentes.                     |
| `mv`            | Move ou renomeia arquivos e diretórios.                                                 |
| `cp`            | Copia arquivos e diretórios.                                                            |
| `rm`            | Remove arquivos ou diretórios.                                                          |
| `pwd`           | Exibe a localização na árvore de diretórios.                                            |
| `passwd`        | Altera a senha de um usuário.                                                           |
| `su/sudo`       | Entra no modo super usuário.                                                            |
| `ps`            | Exibe informações sobre processos em execução.                                          |
| `top`           | Monitora processos em tempo real.                                                       |
| `kill`          | Envia sinais para processos, geralmente usados para terminar processos.                 |
| `killall`       | Envia sinais para todos os processos que correspondem ao nome dado.                     |
| `nice`          | Inicia um processo com uma prioridade alterada.                                         |
| `renice`        | Altera a prioridade de processos em execução.                                           |
| `nohup`         | Executa um comando ignorando sinais de hangup.                                          |
| `useradd`       | Adiciona novos usuários ao sistema.                                                     |
| `userdel`       | Remove usuários do sistema.                                                             |
| `usermod`       | Modifica contas de usuário.                                                             |
| `groupadd`      | Cria um novo grupo.                                                                     |
| `groupdel`      | Remove um grupo.                                                                        |
| `groupmod`      | Modifica informações de um grupo.                                                       |
| `logname`       | Exibe o nome do usuário atual.                                                          |
| `id`            | Exibe informações sobre o usuário atual ou especificado.                                |
| `chfn`          | Altera informações adicionais do usuário.                                               |
| `last`          | Exibe um histórico de logins no sistema.                                                |
| `history`       | Mostra os últimos comandos digitados.                                                   |
| `!<número>`     | Reexecuta o comando <número>da lista de histórico.                                     |

---
<br>

# 6. Conceitos Adicionais

## Gerenciamento de Permissões e Segurança
>[!NOTE]
>#### Sistema de Arquivos
>1. **Sistema de Arquivos**: Estrutura de dados que o sistema operacional usa para controlar como os dados são armazenados e recuperados.
>2. **Lista de Controle de Acesso (ACL)**: Define quais usuários ou grupos têm permissões para acessar ou modificar um arquivo ou diretório.
>3. **Tipos de Acesso**:
>  - `Read (r)`: Permissão para ler o conteúdo.
>  - `Write (w)`: Permissão para modificar o conteúdo.
>  - `Execute (x)`: Permissão para executar o arquivo como um programa.
>4. **Comandos Relevantes**:
>  - `chmod`: Altera as permissões de arquivos e diretórios.
>  - `chown`: Altera o proprietário de arquivos e diretórios.
>  - `chgrp`: Altera o grupo de arquivos e diretórios.

<br>

## Gerenciamento de Discos
>[!NOTE]
>#### Gerenciamento de Discos no Linux
>1. **Identificação e Preparação de Novos Discos**:
>  - Use `df` para verificar discos atuais.
>  - Utilize `dmesg | grep disk` para identificar novos discos.
>  - Use `fdisk` para particionar e `mkfs.ext3` para formatar discos.
>  - Configure montagens automáticas no `/etc/fstab` utilizando o UUID do disco.
>2. **Estrutura de Partições**:
>  - Limitação de 4 partições primárias no sistema.
>  - **Partição Estendida**: Uma solução para contornar a limitação de 4 partições primárias; pode conter múltiplas partições lógicas.

<br>

## Estrutura de Arquivos e Diretórios
>[!NOTE]
>#### Estrutura de Diretórios
>1. **Estrutura em Árvore**: Modelo utilizado tanto no Linux quanto no Windows. A raiz é o ponto de partida para todos os diretórios.
>2. **Comandos para Gerenciamento de Arquivos**:
>  - `mkdir`: Cria novos diretórios.
>  - `cd`: Navegar entre diretórios.
>  - `ls`: Lista arquivos e diretórios.
>  - `touch`: Cria arquivos vazios ou atualiza timestamps de arquivos existentes.
>  - `mv`: Move ou renomeia arquivos e diretórios.
>  - `cp`: Copia arquivos e diretórios.
>  - `rm`: Remove arquivos ou diretórios.
