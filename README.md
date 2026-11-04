# Command Center by Center Soft Inc.®

Sistema patrimonial modular para gestão financeira, imobiliária, contratual e patrimonial, desenvolvido para operação local diretamente no navegador.

## Visão Geral

O **Command Center** é uma central de gerenciamento integrada que reúne diversos módulos administrativos em uma única interface elegante e segura. O sistema foi projetado para uso local, sem dependência de servidores externos ou bancos de dados em nuvem.

### Principais Características

- Interface moderna com design premium inspirado em centros de comando corporativos.
- Navegação centralizada através de menu lateral.
- Controle de acesso por senha.
- Alteração dinâmica da senha de acesso.
- Carregamento modular via iframe.
- Operação 100% local.
- Armazenamento persistente utilizando LocalStorage do navegador.
- Política de uso e responsabilidade de backup integrada ao sistema.

---

## Módulos Disponíveis

O sistema possui integração com os seguintes módulos:

| Módulo | Função |
|---|---|
| Gestão de Aluguéis | Controle mensal e anual de aluguéis, documentos, Gmail, WhatsApp e backup em JSON |
| Imóveis & IPTU & Serviços | Administração patrimonial de imóveis |
| Gestão de Contratos | Controle contratual |
| Gestão Financeira Global | Consolidação financeira |
| Gestão Contas Bancárias | Administração bancária |
| Gestão Cartões de Crédito | Gestão de cartões |
| Gestão de Cartões | Controle de parcelas e despesas |
| Quantum Trade | Controle de operações financeiras e investimentos |
| FleetManager PRO | Gestão de frota veicular |

---

## Novas Funções da Gestão de Aluguéis

O módulo **Gestão de Aluguéis** inclui os seguintes recursos:

### Cadastro e organização

- Cadastro mensal de inquilino, e-mail, data de pagamento, reajuste, CDC/IPTU, destino do pagamento, aluguel, extras e descrição do extra.
- Inclusão, exclusão e reordenação de registros.
- Cópia dos dados do mês anterior, incluindo o campo de e-mail.
- Campos organizados em linhas, com as ações em uma linha própria.
- Cálculo automático do subtotal de aluguel e extras.
- Cálculo do total acumulado anual.

### Gmail

- Botão **Gmail** nas ações de cada registro.
- Abertura de mensagem com destinatários, assunto e corpo preenchidos automaticamente.
- Suporte a vários destinatários separados por ponto e vírgula.
- Validação individual dos endereços de e-mail.
- Saudação automática conforme o horário de emissão.
- Inclusão automática da competência, data de pagamento e valor a pagar.
- Texto preparado para inclusão manual da assinatura padrão configurada no Gmail.
- O PDF do demonstrativo deve ser anexado manualmente antes do envio.

### WhatsApp

- Botão **WhatsApp** nas ações de cada registro.
- Popup com a mensagem pronta para conferência.
- Botão **Copiar texto** para colar a mensagem na conversa desejada.
- Saudação automática conforme o horário:
  - 00h00 até 12h00: **bom dia**;
  - 12h01 até 17h59: **boa tarde**;
  - 18h00 até 23h59: **boa noite**.
- A mensagem começa com **🙋🏻‍♂️Olá**, sem exibir o nome do inquilino.
- Inclusão automática da competência, data de pagamento e valor a pagar.

### Documentos e relatórios

- Demonstrativo individual de aluguel.
- Recibo.
- Extrato anual individual para declaração de Imposto de Renda.
- Relatório mensal de recebimentos.
- Relatório anual consolidado.
- Impressão e salvamento em PDF pela janela de impressão do navegador.

### Backup e compatibilidade

- Exportação dos dados em arquivo JSON.
- Importação de backups gerados pelo sistema.
- Inclusão dos e-mails no backup mensal.
- Compatibilidade com backups antigos sem o campo de e-mail. Nesse caso, os demais dados são restaurados e o e-mail permanece vazio.
- Armazenamento local organizado por ano e mês utilizando LocalStorage.

### Observações operacionais

- A abertura do Gmail depende da permissão de pop-ups do navegador.
- A cópia do texto do WhatsApp depende da permissão de acesso à área de transferência. O sistema possui um método alternativo de cópia.
- A impressão e a geração de PDF dependem dos recursos de impressão do navegador.
- Tailwind CSS, Font Awesome e Google Fonts são carregados por CDN e dependem de conexão com a internet para carregar integralmente o estilo e os ícones.

---

## Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript Vanilla
- Tailwind CSS via CDN
- Font Awesome via CDN
- Google Fonts
  - Cinzel
  - Montserrat
- LocalStorage para persistência de dados locais
- JSON para exportação e importação de backups

---

## Estrutura do Projeto

```text
/
├── index.html
├── icon.ico
├── Gestão de Aluguéis.html
├── Imóveis & IPTU & Serviços.html
├── Gestão de Contratos.html
├── Gestão Financeira Global.html
├── Gestão Contas Bancárias.html
├── Gestão Cartões de Credito.html
├── Gestão de Cartões.html
├── Quantum Trade.html
└── FleetManager PRO.html
```

---

## Controle de Acesso

O sistema permite:

- Login protegido por senha.
- Alteração da senha diretamente pela interface.
- Remoção opcional da proteção por senha.
- Bloqueio manual da sessão.

A senha é armazenada localmente no navegador através do LocalStorage.

---

## Armazenamento de Dados

Todos os dados são armazenados localmente no navegador do usuário.

### Importante

O sistema:

- Não utiliza servidor próprio nem banco de dados remoto para armazenar os registros.
- Não realiza sincronização automática em nuvem.
- Mantém os dados operacionais no LocalStorage do navegador.
- Utiliza recursos visuais externos por CDN, como Tailwind CSS, Font Awesome e Google Fonts.
- Abre serviços externos somente quando o usuário aciona funções específicas, como Gmail.

---

## Política de Backup

⚠️ **A responsabilidade pelo backup é integralmente do usuário.**

Recomenda-se:

1. Exportar regularmente os dados dos módulos.
2. Manter cópias em:
   - Disco local
   - HD externo
   - Pen Drive
   - Serviços de nuvem

### Isenção de Responsabilidade

Os responsáveis pelo sistema não se responsabilizam por perdas decorrentes de:

- Limpeza de cache do navegador;
- Exclusão do LocalStorage;
- Formatação do computador;
- Falhas do sistema operacional;
- Ações de antivírus;
- Ausência de backups realizados pelo usuário.

---

## Instalação

1. Baixe todos os arquivos do projeto.
2. Mantenha os módulos HTML no mesmo diretório do arquivo principal.
3. Abra o arquivo `index.html` em um navegador moderno.
4. Realize o login utilizando a senha configurada.
5. Utilize o menu lateral para acessar os módulos.

---

## Requisitos

### Navegadores Compatíveis

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Opera

### Requisitos Mínimos

- JavaScript habilitado
- Suporte a LocalStorage
- Resolução mínima recomendada: 1366x768

---

### Instalação no computador

### No Google Chrome ou Microsoft Edge:

  1. Abra o endereço publicado do projeto.
  2. Aguarde o carregamento completo da página.
  3. Clique no ícone de instalação exibido na barra de endereço ou abra o menu do navegador.
  4. Selecione Instalar aplicativo ou Instalar este site como aplicativo.
  5. Confirme a instalação.

Depois disso, o aplicativo poderá ser aberto pelo menu Iniciar, pela área de trabalho ou pelo gerenciador de aplicativos do sistema.

### Instalação no celular ou tablet

### Em navegadores compatíveis:

1. Abra o endereço do projeto.
2. Acesse o menu do navegador.
3. Selecione Instalar aplicativo ou Adicionar à tela inicial.
4. Confirme o nome e a instalação.

O ícone será adicionado à tela inicial do dispositivo.

**Observações**

A disponibilidade e o nome da opção de instalação podem variar conforme o navegador e o sistema operacional.
Abrir somente o arquivo index.html pelo computador não garante a instalação como PWA.
O projeto deve ser publicado em HTTPS para utilizar os recursos completos de instalação e service worker.
O funcionamento offline depende da configuração do service-worker.js e dos arquivos adicionados ao cache.
Atualizações no projeto podem exigir a atualização da versão do cache do service worker.

---

## Licenciamento

**Command Center by Center Soft Inc.®**

Todos os direitos reservados.

Este software destina-se exclusivamente ao gerenciamento patrimonial, financeiro e administrativo do usuário final autorizado.

---

## Autor

**Alberto de Campos Neto**

**Center Soft Inc.®**

---

## Aviso

> Este projeto é uma demonstração educacional desenvolvida para estudos de HTML, CSS e JavaScript. A empresa mencionada é fictícia e qualquer semelhança com empresas reais é mera coincidência.
