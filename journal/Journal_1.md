[🇺🇸 English version below](#1---initial-setup)
<br>

# 1 - Setup Inicial

## Primeira Instalação

### Problemas com usuário e login

Como trouxe no readme, estou utilizando para este projeto uma máquina antiga. E, por conta disso, surgiu um problema que eu não imaginava no início: fiquei trancada para fora do sistema.<br>
Na primeira tentativa de instalação do sistema operacional, ocorreu um erro na criação do usuário durante o processo inicial. O sistema finalizou a instalação, mas o login não funcionava. A hipótese: como o teclado não está tão bom, a senha gravada não correspondia à que eu criei e o resultado foi não conseguir logar no sistema.

**O que eu fiz:**

* Acessei ao sistema em *recovery mode*.
* Excluí manualmente do usuário criado incorretamente.
* Criei de um novo usuário e reconfiguração das permissões.


### Problemas com a conectividade

Outro problema que ocorreu foi com a configuração do Wi-Fi. O notebook não possui entrada RJ45 e não tenho adaptador. A interface `wlan0` não estava sendo reconhecida por nada e, para não abortar o processo, a instalação foi concluída **sem rede**.
Após a instalação, não foi possível habilitar o wi-fi manualmente.

**O que eu fiz:**

Aí não teve jeito. Precisei reinstalar o sistema operacional.

**Desafio adicional:**

Ocorreram problemas com o boot pelo pendrive e precisei alterar algumas configurações da BIOS para conseguir conseguir inicializar corretamente pelo USB novamente. Sorte que encontrei alguns tutoriais que me ajudaram nessa etapa.

**Resultado:**

* Reinstalação bem-sucedida.
* Wi-Fi configurado corretamente durante o setup inicial.

**Trade-off:**

* Gastei tempo com a reinstalação mas reduzi o custo congnitivo de ficar batendo cabeça para debugar estando offline.

---

## Segunda instalação

### Setup base

Após a terceira tentativa, o sistema foi configurado com sucesso. As seguintes etapas foram concluídas:

* Configuração correta do Wi-Fi durante a instalação.
* Acesso SSH configurado já no processo inicial, utilizando chave do GitHub.
* Ajuste do layout do teclado.
* Verificação do IP local e conectividade.
* Atualização completa do sistema.
* Configuração do timezone.
* Habilitação do OpenSSH.
* Configuração inicial do firewall.
* Instalação de ferramentas essenciais para administração.
* Instalação e validação do Docker e Docker Compose.
* Criação da estrutura de pastas base do projeto.
* Manutenção da configuração padrão de swap (sem ajustes prematuros).


### Configurações e Limitações de hardware

Foi necessário ajustar o sistema para não desligar a tela e não entrar em modo de suspensão.
A ideia inicial era manter o notebook fechado, funcionando como um servidor headless. No entanto, algumas limitações físicas impediram isso:

* Dobradiça estava travada.
* Moldura da tela se desintegrando (literalmente).
* Risco mais danos físicos se mantido fechado (tela rachou quando fui tentar abrir a tampa).

Decidi então manter o notebook aberto, aceitando a limitação estética em prol da estabilidade física do hardware.


### Acesso Remoto e Rede

Segui para a configuração do acesso remoto via SSH.
A rede Wi-Fi foi configurada com **IP estático**, garantindo previsibilidade para configurações como:

  * Acesso remoto.
  * Futuras configurações de serviços.
  * Monitoramento e observabilidade.

---

## Principais Aprendizados

* Problemas básicos (usuário, rede, boot) trouxe um desafio real à minha mini operação.
* Preocupação e necessidade de lidar com limitações reais de hardware.

</br>

---

# 1 - Initial Setup

## First Installation

### User and Login Issues

As mentioned in the README, I am using an old machine for this project. Because of this, a problem arose that I hadn't anticipated: I got locked out of the system.

During the first OS installation attempt, an error occurred during the initial user creation process. The system finished the installation, but the login failed. **The hypothesis:** Since the keyboard is in poor condition, the recorded password didn't match the one I intended to create, resulting in a login failure.

**What I did:**

* Accessed the system via **Recovery Mode**.
* Manually deleted the incorrectly created user.
* Created a new user and reconfigured permissions.

### Connectivity Issues

Another problem occurred with the Wi-Fi configuration. The laptop lacks an RJ45 port and I don't have an adapter. The `wlan0` interface was not being recognized at all; to avoid aborting the process, the installation was completed **offline**.
After installation, I was unable to enable the Wi-Fi manually.

**What I did:**

In the end, there was no other way: I had to reinstall the operating system.

**Additional Challenge:**

Issues arose with the USB boot process, requiring me to change several BIOS settings to successfully boot from the USB drive again. Luckily, I found some tutorials that guided me through this stage.

**Result:**

* Successful reinstallation.
* Wi-Fi correctly configured during the initial setup.

**Trade-off:**

* I spent extra time on the reinstallation, but it reduced the cognitive load of "banging my head against the wall" trying to debug while offline.

---

## Second Installation

### Base Setup

After the third attempt, the system was successfully configured. The following steps were completed:

* Correct Wi-Fi configuration during installation.
* **SSH access** configured during the initial process using my GitHub keys.
* Keyboard layout adjustment.
* Local IP verification and connectivity testing.
* Full system update (`dist-upgrade`).
* Timezone configuration.
* **OpenSSH** enabled.
* Initial Firewall (UFW) configuration.
* Installation of essential administration tools.
* Installation and validation of **Docker and Docker Compose**.
* Creation of the base project folder structure.
* Maintenance of the default **swap** configuration (avoiding premature optimization).

### Hardware Configurations and Limitations

It was necessary to adjust the system settings to prevent the screen from turning off and the system from entering sleep mode.
The initial idea was to keep the laptop lid closed, functioning as a true **headless server**. However, physical limitations prevented this:

* The hinge was seized/stuck.
* The screen bezel was literally disintegrating.
* Risk of further physical damage if kept closed (the screen actually cracked when I tried to force the lid open).

I decided to keep the laptop open, accepting the aesthetic limitation in favor of the hardware's physical stability.

### Remote Access and Networking

I proceeded with the remote access setup via SSH.
The Wi-Fi network was configured with a **Static IP**, ensuring predictability for:

* Remote access.
* Future service deployments.
* Monitoring and Observability stack.

---

## Key Takeaways

* Basic issues (user creation, networking, booting) posed a real challenge to my "mini-operation."
* Realized the necessity and concern of dealing with genuine hardware limitations.