OakOS - Sistema Operacional Experimental

Status: Em Desenvolvimento (InDev)

Este projeto encontra-se em estágio inicial de desenvolvimento e não está disponível em versões Alpha ou Beta. O OakOS pode apresentar falhas, bugs e diversas funcionalidades ainda não implementadas.

Descrição:
OakOS é um sistema operacional experimental destinado ao estudo e desenvolvimento de conceitos de baixo nível, incluindo bootloader próprio, kernel minimalista, gerenciamento de memória, sistema de arquivos, drivers e interface de usuário. Trata-se de um projeto proprietário, cuja distribuição e uso são restritos exclusivamente a colaboradores autorizados.

Requisitos para Testes:
Para executar e testar o OakOS, é necessário utilizar o QEMU, um emulador de hardware que suporta as plataformas Linux, Windows e macOS.

Instruções para instalação do QEMU:

- Linux (Ubuntu/Debian):
  Execute os comandos abaixo em um terminal:
  sudo apt update
  sudo apt install qemu qemu-system-x86

- Windows:
  Faça o download do QEMU no endereço: https://qemu.weilnetz.de/w64/
  Extraia o conteúdo do arquivo e execute a partir da pasta ou configure o PATH do sistema para facilitar o uso via linha de comando.

- macOS:
  Instale o Homebrew, caso ainda não possua, e em seguida o QEMU:
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  brew install qemu

Execução do OakOS com QEMU:

Após obter a imagem do OakOS (arquivo oakos.iso ou oakos.img), utilize os comandos abaixo para iniciar a máquina virtual:

- Caso possua um arquivo ISO:
  qemu-system-x86_64 -cdrom oakos.iso -m 512 -smp 2 -boot d

- Caso possua um arquivo IMG:
  qemu-system-x86_64 -drive format=raw,file=oakos.img -m 512 -smp 2 -boot d

Parâmetros importantes:
- -m 512: aloca 512 MB de memória RAM para a máquina virtual
- -smp 2: configura 2 CPUs virtuais
- -boot d: define o boot pelo drive de CD
- -enable-kvm: (Linux) habilita aceleração por hardware para melhor desempenho

Exemplo completo para Linux:
qemu-system-x86_64 -cdrom oakos.iso -m 512 -smp 2 -boot d -enable-kvm

Estado Atual do Projeto:
- Bootloader próprio: concluído
- Kernel básico: em desenvolvimento
- Sistema de arquivos: não implementado
- Gerenciamento de processos: não implementado
- Interface gráfica: não implementada

Avisos Legais:
Este projeto é proprietário e confidencial. A cópia, modificação ou distribuição do código-fonte e arquivos relacionados é expressamente proibida sem autorização prévia e por escrito do autor. O repositório é privado, e o acesso é concedido apenas a colaboradores autorizados.

Contato para Colaboração:
Caso tenha interesse em contribuir ou testar o OakOS, por favor, entre em contato pelo e-mail: seu.email@exemplo.com

Autor:
Seu Nome
Email: seu.email@exemplo.com

Licença:
Copyright (c) 2025 Seu Nome
Todos os direitos reservados.
Este software é proprietário e confidencial.
Não é permitida a cópia, distribuição ou modificação sem autorização expressa do autor.
