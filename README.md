# WSL (Subsistema do Windows para Linux)

Comandos para utilizar o WSL.

## 1. Instalar o WSL

```bash
wsl --install
```

## 2. Desinstalar a versão padrão do WSL

```bash
wsl --unregister ubuntu
```

## 3. Listar Distribuições Disponíveis

Para visualizar as distribuições disponíveis, use:

```bash
wsl --list --online

Lista de distribuições válidas:

NAME                                   FRIENDLY NAME
Ubuntu                                 Ubuntu
Debian                                 Debian GNU/Linux
kali-linux                             Kali Linux Rolling
Ubuntu-18.04                           Ubuntu 18.04 LTS
Ubuntu-20.04                           Ubuntu 20.04 LTS
Ubuntu-22.04                           Ubuntu 22.04 LTS
Ubuntu-24.04                           Ubuntu 24.04 LTS
OracleLinux_7_9                        Oracle Linux 7.9
OracleLinux_8_7                        Oracle Linux 8.7
OracleLinux_9_1                        Oracle Linux 9.1
openSUSE-Leap-15.5                     openSUSE Leap 15.5
SUSE-Linux-Enterprise-Server-15-SP4    SUSE Linux Enterprise Server 15 SP4
SUSE-Linux-Enterprise-15-SP5           SUSE Linux Enterprise 15 SP5
openSUSE-Tumbleweed                    openSUSE Tumbleweed
```

## 4. Instalar uma Distribuição

Para instalar a distribuição desejada, use:

```bash

wsl.exe --install <Distro>
```

Argumentos para Executar Binários do Linux

    Nenhuma linha de comando fornecida: Inicia o shell padrão.
    --exec, -e <CommandLine>: Executa o comando especificado sem usar o shell padrão.
    --shell-type <standard|login|none>: Executa o comando com o tipo de shell fornecido.
    --: Passa a linha de comando restante como está.

Opções Gerais

    --cd <Directory>: Define o diretório especificado como o diretório de trabalho atual.
    --distribution, -d <Distro>: Executa a distribuição especificada.
    --user, -u <UserName>: Executa como o usuário especificado.
    --system: Inicia um shell para a distribuição do sistema.

Gerenciar o WSL

    --help: Exibe as informações de uso.
    --debug-shell: Abre um shell de depuração WSL2.
    --install [Distro] [Options...]: Instala uma distribuição do WSL.
        Opções:
            --no-launch, -n: Não inicia a distribuição após a instalação.
            --web-download: Baixa a distribuição da internet em vez da Microsoft Store.
            --no-distribution: Instala apenas os componentes opcionais.
            --enable-wsl1: Habilita o suporte para WSL1.
    --manage <Distro> <Options...>: Altera opções específicas da distribuição.
        Opções:
            --set-sparse, -s <true|false>: Define o vhdx da distribuição como esparso.
    --mount <Disk>: Anexa e monta um disco físico ou virtual em todas as distribuições do WSL 2.
        Opções:
            --vhd: Especifica que <Disk> é um disco rígido virtual.
            --bare: Anexa o disco ao WSL2, mas não o monta.
            --name <Name>: Usa um nome personalizado para o ponto de montagem.
            --type <Type>: Sistema de arquivos a ser usado ao montar um disco; padrão é ext4.
            --options <Options>: Opções de montagem adicionais.
            --partition <Index>: Índice da partição a ser montada.
    --set-default-version <Version>: Altera a versão padrão para novas distribuições.
    --shutdown: Encerra todas as distribuições em execução e a máquina virtual do WSL 2.
    --status: Mostra o status do WSL.
    --unmount [Disk]: Desmonta e desanexa um disco de todas as distribuições do WSL2.
    --uninstall: Desinstala o WSL deste computador.
    --update: Atualiza o pacote do WSL.
        Opções:
            --pre-release: Baixa uma versão de pré-lançamento.
    --version, -v: Exibe informações da versão.

Gerenciar Distribuições no WSL

    --export <Distro> <FileName> [Options]: Exporta a distribuição para um arquivo tar.
        Opções:
            --vhd: Exporta como um arquivo .vhdx.
    --import <Distro> <InstallLocation> <FileName> [Options]: Importa um arquivo tar como uma nova distribuição.
        Opções:
            --version <Version>: Especifica a versão para a nova distribuição.
            --vhd: Especifica que o arquivo é um .vhdx.
    --import-in-place <Distro> <FileName>: Importa um arquivo .vhdx como uma nova distribuição.
    --list, -l [Options]: Lista distribuições.
        Opções:
            --all: Lista todas as distribuições.
            --running: Lista apenas as distribuições em execução.
            --quiet, -q: Mostra apenas os nomes das distribuições.
            --verbose, -v: Mostra informações detalhadas.
            --online, -o: Lista distribuições disponíveis para instalação.
    --set-default, -s <Distro>: Define a distribuição como padrão.
    --set-version <Distro> <Version>: Altera a versão da distribuição.
    --terminate, -t <Distro>: Encerra a distribuição especificada.
    --unregister <Distro>: Cancela o registro da distribuição e exclui o sistema de arquivos raiz.