# Relatórios de Práticas - Sistemas Operativos e Redes

**Aluno:** Seu Nome Completo  
**Matrícula:** Sua Matrícula  
**Turma:** SysDevTech 2026.2  
**Repositório:** Atividades Práticas (Aulas 01, 02 e 03)  

---

## Aula 01 - Instalação e Configuração do Ubuntu Server

### 1. Objetivos
Aprender os conceitos de virtualização com o VirtualBox, organizar a pasta do laboratório, criar a VM e instalar o Ubuntu Server 26.04 LTS com particionamento LVM e usuário padrão.

### 2. Preparação do Ambiente no Host
1. Verificação da imagem ISO `ubuntu-26.04-live-server-amd64.iso` na pasta `C:\2026.2\SysDevTech\VM\original`.
2. Criação da pasta individual e da VM: `C:\2026.2\SysDevTech\VM\SeuNome\ubuntu_server`.

### 3. Configuração da VM (VirtualBox)
* **Nome:** ubuntu_server
* **Tipo/Versão:** Linux / Ubuntu (64-bit)
* **Memória RAM:** 1.5 GB (reduzido para 768 MB pós-instalação)
* **Processador:** 1 vCPU
* **Disco Rígido Virtual:** VDI, Dinamicamente Alocado com 32 GB

### 4. Instalação e Particionamento (LVM)
* **Idioma/Teclado:** English / Portuguese (Brazil)
* **Rede:** DHCP ativo na interface `enp0s3`
* **Layout de Disco Personalizado:**
  * `/boot`: 1 GB (`ext4`)
  * `/` (root): 29 GB (`ext4`)
  * `swap`: 2 GB
* **Utilizador Criado:** `administrador` (Senha: `adminifal`)
* **Serviços:** OpenSSH Server instalado.

### 5. Pós-Instalação
Login efetuado com sucesso e atualização de pacotes executada:
```bash
sudo apt-get update