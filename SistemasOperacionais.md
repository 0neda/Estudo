### 1. Gerenciamento de Discos no Linux
- **Identificação e Preparação de Novos Discos:**
  - Use `df` para verificar discos atuais.
  - Utilize `dmesg | grep disk` para identificar novos discos.
  - Use `fdisk` para particionar e `mkfs.ext3` para formatar discos.
  - Configure montagens automáticas no `/etc/fstab` utilizando o UUID do disco.

### 2. Gerenciamento de Processos no Linux
- **Comunicação entre Processos (IPC):**
  - Técnicas como `memória compartilhada`, `pipes`, `sinais`, `semáforos`, e `filas de mensagens`.
  - Comando `ipcs` para visualizar canais de comunicação.

- **Comandos para Gerenciar Processos:**
  - `ps`, `top`, e `htop` para listar e monitorar processos.
  - `kill` e `killall` para enviar sinais a processos.
  - `nice` e `renice` para ajustar a prioridade dos processos.

- **Entendendo Sinais:**
  - Sinais como `SIGHUP (1)`, S`IGINT (2)`, `SIGTERM (15)`, e `SIGKILL (9)`.
  - `kill -9` força a interrupção de processos, enquanto `kill -15` solicita uma interrupção graciosa.

- **Monitoramento de Processos:**
  - Use `top` para monitoramento em tempo real.
  - Comando `ps` para listar detalhadamente processos e `kill` para encerrar.

### 3. Manipulação de Arquivos e Diretórios
- **Comandos Básicos:**
  - Criar diretórios: `mkdir`.
  - Navegar no sistema de arquivos: `cd`, `ls`.
  - Manipular arquivos: `touch`, `mv`, `cp`, `rm`.

### 4. Controle de Usuários e Grupos no Linux
- **Gerenciamento de Usuários:**
  - Arquivo `/etc/passwd` armazena informações de usuários.
  - Comandos como `useradd`, `userdel`, `usermod`.

- **Gerenciamento de Grupos:**
  - Comandos `groupadd`, `groupdel`, `groupmod`.
  - Arquivo `/etc/group` contém informações sobre grupos e seus membros.

### 5. Gerenciamento de Memória
- **Conceitos Básicos:**
  - Memória física (**RAM**) e virtual (**swap**).
  - O kernel gerencia a memória, alocando e desalocando conforme necessário.

- **Monitoramento:**
  - `free` para verificar uso de memória.
  - `vmstat` para estatísticas de memória virtual e sistema.

- **Técnicas de Gerenciamento:**
  - **Paginação e segmentação** para gerenciamento eficiente.
  - **Swapping** para liberar **RAM** movendo processos inativos para o disco.

### Conceitos Adicionais
- **Prioridades de Processos:**
  - Valores de `nice` variando de -20 (mais alta prioridade) a +19 (mais baixa).
  - Ajuste de prioridade usando `nice` e `renice`.

- **Execução em Segundo Plano:**
  - Utilize o operador `&` para rodar processos em segundo plano.
  - Comando `bg` para mover processos para segundo plano e `fg` para trazê-los de volta.

- **Uso de `nohup`:**
  - Comando para executar processos que ignoram o sinal de hangup, permitindo logout sem encerrar o processo.



# Comandos

| Comando         | Função                                                                                  |
|-----------------|-----------------------------------------------------------------------------------------|
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
| `ps`            | Exibe informações sobre processos em execução.                                          |
| `top`           | Monitora processos em tempo real.                                                       |
| `htop`          | Uma versão interativa e mais amigável do top.                                           |
| `kill`          | Envia sinais para processos, geralmente usados para terminar processos.                 |
| `killall`       | Envia sinais para todos os processos que correspondem ao nome dado.                     |
| `nice`          | Inicia um processo com uma prioridade alterada.                                         |
| `renice`        | Altera a prioridade de processos em execução.                                           |
| `nohup`         | Executa um comando ignorando sinais de hangup.                                          |
| `useradd`       | Adiciona novos usuários ao sistema.                                                     |
| `userdel`       | Remove usuários do sistema.                                                             |
| `usermod`       | Modifica contas de usuário.                                                             |
| `passwd`        | Altera a senha de um usuário.                                                           |
| `groupadd`      | Cria um novo grupo.                                                                     |
| `groupdel`      | Remove um grupo.                                                                        |
| `groupmod`      | Modifica informações de um grupo.                                                       |
| `logname`       | Exibe o nome do usuário atual.                                                          |
| `id`            | Exibe informações sobre o usuário atual ou especificado.                                |
| `chfn`          | Altera informações adicionais do usuário.                                               |
| `last`          | Exibe um histórico de logins no sistema.                                                |
