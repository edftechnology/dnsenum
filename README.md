# Como configurar/instalar/usar o `dnsenum` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar o `dnsenum` no `Linux Ubuntu`.

## _Abstract_

_In this document are contained the main commands and settings to set up/install the `dnsenum` on `Linux Ubuntu`._


## Descrição [2]

### `dnsenum`

O "dnsenum" é uma ferramenta de código aberto amplamente usada para coletar informações de reconhecimento em um alvo específico, como endereços de e-mail, nomes de domínio, subdomínios, hosts e outras informações relacionadas à presença online. Desenvolvido em Python, o dnsenum permite que os profissionais de segurança, pesquisadores de segurança e hackers éticos coletem informações valiosas que podem ser usadas para avaliar a superfície de ataque de um alvo e identificar possíveis vulnerabilidades ou pontos fracos em sua infraestrutura de TI. A ferramenta é especialmente útil durante as fases de coleta de informações e reconhecimento em testes de penetração e auditorias de segurança, auxiliando na análise de ameaças e na tomada de decisões informadas para melhorar a postura de segurança de uma organização. O dnsenum suporta várias fontes de dados públicas e privadas e é uma escolha popular para tarefas de coleta de informações em cenários de segurança cibernética. É importante observar que o uso dessa ferramenta deve ser sempre legal e ético, em conformidade com as leis e regulamentos aplicáveis.

### `DNS`

O DNS, ou Sistema de Nomes de Domínio, é um sistema fundamental na Internet que traduz nomes de domínio legíveis por humanos, como exemplo.com, em endereços IP numéricos, que são utilizados pelos computadores para localizar serviços e recursos na rede. Funcionando como uma espécie de catálogo telefônico da Internet, o DNS permite que os usuários acessem sites, enviem e recebam e-mails, e realizem outras atividades online, sem precisar memorizar endereços IP complexos. Quando um usuário digita um nome de domínio em um navegador da web ou em outro aplicativo de Internet, o computador faz uma consulta DNS para encontrar o endereço IP correspondente associado a esse nome de domínio. Esse processo envolve a comunicação com servidores DNS distribuídos em toda a Internet, começando com servidores de nomes raiz e percorrendo uma hierarquia de servidores DNS autorizados até encontrar a resposta desejada. O DNS é essencial para o funcionamento da Internet moderna e é uma parte crítica da infraestrutura de rede global.


## 1. Como configurar/instalar/usar o `dnsenum` no `Linux Ubuntu` [1]

Para configurar/instalar/usar o `dnsenum` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o `Root Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Suft + Alt + T`

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.2 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.3 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update -y`

    2.4 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.5 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update -y`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`

    2.6 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.7 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

3. O `dnsenum` já vem pré-instalado do `Linux Ubuntu`. Sendo assim, para instalar o `nmap` tant no `Linux Ubuntu` quanto no `Linux Ubuntu`, siga as instruções abaixo:

### 1.1 Primeiro método (e mais complicado)

Para instalar o dnsenum no Linux Ubuntu, você pode seguir os seguintes passos. Esses passos assumem que você está usando uma versão do Ubuntu que suporta esses comandos e tem permissões para executá-los (geralmente como usuário root ou utilizando o comando sudo para obter permissões de administrador).

4. **Instale as dependências necessárias:** `dnsenum` depende do Perl e de vários módulos Perl. Você pode instalar as dependências necessárias com o seguinte comando: `sudo apt-get install cpanminus perl libwww-perl libnet-ssleay-perl libxml-libxml-perl libnet-dns-perl`

5. **Baixe o script do `dnsenum`:** Você pode obter a versão mais recente do `dnsenum` clonando o repositório do GitHub ou baixando o script diretamente, se disponível. Verifique a página oficial do dnsenum no GitHub para obter o link de clonagem: `git clone https://github.com/fwaeytens/dnsenum.git`

6. **Mude para o diretório do `dnsenum`:** `cd dnsenum`

7. **Torne o script `dnsenum.pl` executável:** `chmod +x dnsenum.pl`

8. **Instalar o módulo `Net::Netmask` via `CPAN`:** Você pode instalar o módulo `Net::Netmask` diretamente usando o `CPAN` com o seguinte comando: `sudo cpanm Net::Netmask`

9. Alternativamente, instalar o módulo `Net::Netmask` via `APT`:
Algumas vezes, módulos Perl podem estar disponíveis como pacotes no repositório do Ubuntu. Você pode tentar instalar o `Net::Netmask` usando o `apt` com o seguinte comando: `sudo apt-get install libnet-netmask-perl`


10. Certifique-se de que seu sistema esteja limpo e atualizado.

    10.1 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    10.2 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    10.3 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update -y`

    10.4 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    10.5 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update -y`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`

    10.6 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    10.7 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

11. Depois de instalar o módulo `Net::Netmask`, tente executar o `dnsenum.pl` novamente. Se houver mais módulos faltando, você pode usar o mesmo processo para instalá-los. O erro fornecido geralmente indica qual módulo está faltando, e você pode seguir o formato do comando acima para instalar os módulos necessários, ajustando o nome do módulo conforme necessário.

Para instalar o módulo String::Random, você tem duas opções: usar o CPAN ou procurar se ele está disponível como um pacote do sistema. Aqui estão os comandos para cada método:

12. **Instalar o módulo `String::Random` via `CPAN`: `sudo cpanm String::Random`

    Este comando instalará o módulo `String::Random` usando o `CPAN`, que é um repositório abrangente de módulos Perl.

13. **Instalar o módulo `String::Random` via `APT` (se disponível):** Embora nem todos os módulos Perl estejam disponíveis como pacotes `APT`, é sempre uma boa ideia verificar. Para o `String::Random`, você pode tentar: `sudo apt-get install libstring-random-perl`

    Se este pacote não estiver disponível (o que pode acontecer, já que nem todos os módulos Perl são empacotados para o `APT`), você deve voltar ao método `CPAN`.

    Após instalar o módulo `String::Random`, tente executar o script `dnsenum.pl` novamente. Se outros módulos estiverem faltando, repita o processo para instalá-los. Este método de instalar módulos conforme necessário é uma abordagem eficaz para resolver dependências de scripts Perl.

14. **Execute o dnsenum (você pode precisar de privilégios de administrador dependendo de onde você deseja instalá-lo):** `sudo ./dnsenum.pl`

Lembre-se de verificar a documentação oficial ou o `README` do projeto para obter instruções específicas de instalação, pois as dependências ou os passos podem mudar com novas versões do software.

### 1.2 Segundo método (e menos complicado)

Para configurar/instalar/usar o `dnsenum` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Shift + Alt + T`

2. **Execute o comando:** `sudo apt install dnsenum -y`

## 2. Usar o `dnsenum`

1. **Execute o comando:** `dnsenum meklogistics.com.br`

2. **Execute o comando:** `dnsenum -p 5 -s 20 meklogistics.com.br`

3. **Execute o comando:** `dnsenum -f dns_meklogistics.txt meklogistics.com.br`

## 3. Código completo para configurar/instalar

Para instalar o `dnsenum` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```
    NÃO há.
    ```


## Referências

[1] OPENAI. ***Instale dnsenum no Ubuntu:*** https://chat.openai.com/c/c69e02ed-f24b-4fcc-a470-7cc910ea6b7d (texto adaptado). Acessado em: 09/02/2024 00:37.

[2] OPENAI. ***Vs code: editor popular:*** https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42 (texto adaptado). Acessado em: 09/02/2024 00:37.

[3] USER: FREE EDUCATION FOR ALL. ***Lesson 29: dnsenum:*** https://www.youtube.com/watch?v=FYJ7oiiYvek&list=PLnjNR4-S-EVqfJWovxEJyb7I0IOkKkoYM&index=29 (texto adaptado). Acessado em: 09/02/2024 00:37.

