[🇺🇸 English version below](#-chaos-observatory-english)
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