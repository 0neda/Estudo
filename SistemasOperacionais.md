# Material de Estudo Sistemas Operacionais

## 1. Introdução ao Linux

### Histórico
- **Unix** surgiu em 1969 como um sistema operacional multiusuário e multitarefa.
- **Linus Torvalds** desenvolveu o kernel Linux em 1991 para computadores pessoais, baseado em UNIX.
- Inicialmente compartilhado na Internet, o Linux cresceu rapidamente graças à colaboração global.
- Em menos de 10 anos, o kernel 2.4 foi lançado, com suporte a múltiplos dispositivos e plataformas (i386, Sparc, PowerPC, etc.).

### Estrutura do Linux
- **Kernel**: O núcleo do sistema que interage diretamente com o hardware. É responsável por gerenciar recursos do sistema.
- **Utilitários**: Ferramentas e programas que permitem a interação com o sistema, como shells e editores de texto.

### Sistema de Arquivos
- **Estrutura em Árvore**: O Linux utiliza uma estrutura hierárquica de diretórios com um único diretório raiz (`/`).
- **Arquivos**: São conjuntos de dados armazenados no disco. Podem ter diferentes tipos, como texto ou binário.
- **Setor de Disco**: A menor unidade de armazenamento em um disco, geralmente de 512 bytes.
- **Cluster**: Um grupo de setores usados para armazenar arquivos, sendo a menor quantidade de espaço em disco que pode ser alocada para um arquivo.

### Conceito de Multiusuário
- O Linux suporta múltiplos usuários, cada um com um ID único e senha.
- Sistemas multiusuário permitem que várias pessoas acessem recursos do sistema com permissões restritas.

### Comandos de Sobrevivência no Linux
- **Manuais**: Utilize `man <comando>` para acessar a documentação de comandos.
- **Comandos Essenciais**:
  - `pwd`: Mostra o diretório atual.
  - `passwd`: Altera a senha do usuário.
  - `su/sudo`: Executa comandos com privilégios de superusuário.
  - `ls`: Lista arquivos e diretórios.
  - `mkdir`: Cria novos diretórios.
  - `rm`: Remove arquivos ou diretórios.

## 2. Gerenciamento de Sistemas Operacionais

### Interface e Hardware
- **Gerenciador de Dispositivos**: Controla o funcionamento dos dispositivos conectados ao sistema.
- **IRQ (Interrupção)**: Mecanismo que permite dispositivos de hardware interromperem o processador para atenção imediata.
- **Mapeamento de Hardware**: Processo de alocação de recursos de hardware para garantir que os dispositivos funcionem corretamente.

### Tipos de Sistemas
- **Usuário**: Sistemas voltados para uso pessoal.
- **Servidor**: Sistemas projetados para fornecer serviços a outros computadores em uma rede.

### Desempenho e Segurança
- **Desempenho**: Linux é geralmente mais rápido em operações de banco de dados comparado ao Windows.
- **Segurança**: Embora o Linux seja considerado seguro, a experiência dos administradores pode impactar a segurança. Profissionais especializados em Linux são comuns, mas é preciso ter cuidado com a configuração e manutenção.

## 3. Estrutura de Arquivos e Diretórios

### Unidades de Armazenamento
- **Setor de Disco**: Unidade mínima de armazenamento em discos, geralmente 512 bytes.
- **Cluster**: Múltiplos setores formam um cluster, a menor unidade de espaço que pode ser alocada.

### Atributos de Arquivos
- **Nome**: Identificador do arquivo, que pode ser case sensitive.
- **Atributos**: Incluem tipo, tamanho, permissões, e data/hora de criação ou modificação.
- **Estrutura Interna**: Sequência de bytes ou registros, que podem ser interpretados de diferentes formas.

### Sistemas de Arquivos
- **Linux**:
  - **EXT2/EXT3/EXT4**: Suportam grandes volumes e arquivos, com EXT4 sendo uma evolução de EXT2 e EXT3.
  - **ReiserFS**: Conhecido por excelente desempenho em manipulação de muitos arquivos pequenos.
- **Windows**:
  - **NTFS**: Suporta grandes volumes e arquivos, com segurança integrada.
  - **FAT32**: Mais antigo, com limitações de tamanho de arquivo.
  - **ReFS**: Sistema mais recente, projetado para alta resiliência.

### Comandos de Arquivos
- **chmod**: Altera permissões de arquivos e diretórios.
- **useradd/addgroup**: Gerencia usuários e grupos no sistema.

## 4. Gerenciamento de Recursos no Linux

### Processos
- **Comunicação entre Processos (IPC)**: Utiliza técnicas como memória compartilhada, pipes, sinais, semáforos e filas de mensagens.
- **Comandos**:
  - `ps`: Lista processos em execução.
  - `top`: Monitora processos em tempo real.
  - `kill`: Envia sinais para processos, terminando-os se necessário.
  - `nice`: Ajusta a prioridade de um processo.

### Memória
- **Memória Física (RAM)** e **Memória Virtual (swap)**: O kernel gerencia a alocação de memória para processos, movendo dados para swap quando necessário.
- **Monitoramento**:
  - `free`: Mostra o uso de memória.
  - `vmstat`: Fornece estatísticas sobre memória virtual e sistema.

## 5. Comandos Essenciais no Linux

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
| `pwd`           | Exibe a localização na árvore de diretórios.                                            |
| `passwd`        | Altera a senha de um usuário.                                                           |
| `su/sudo`       | Entra no modo super usuário.                                                            |
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
| `groupadd`      | Cria um novo grupo.                                                                     |
| `groupdel`      | Remove um grupo.                                                                        |
| `groupmod`      | Modifica informações de um grupo.                                                       |
| `logname`       | Exibe o nome do usuário atual.                                                          |
| `id`            | Exibe informações sobre o usuário atual ou especificado.                                |
| `chfn`          | Altera informações adicionais do usuário.                                               |
| `last`          | Exibe um histórico de logins no sistema.                                                |
| `history`       | Mostra os últimos comandos digitados.                                                   |
| `!<número>`     | Reexecuta o comando <número> da lista de histórico.                                     |

## 6. Conceitos Adicionais

### Prioridades e Execução
- **Prioridades de Processos**: Ajustadas com `nice` e `renice`, variando de -20 (prioridade alta) a +19 (prioridade baixa).
- **Execução em Segundo Plano**: Use `&` para colocar processos em segundo plano, `bg` para continuar em segundo plano e `fg` para trazer de volta ao primeiro plano.
- **Uso de `nohup`**: Permite que processos continuem executando após logout.

### Segurança
- **Sistema de Arquivos**: Protegido por listas de controle de acesso, que definem permissões de leitura, escrita e execução.
- **Permissões**: Podem ser alteradas com `chmod`, `chown`, e `chgrp` para controlar o acesso a arquivos e diretórios.