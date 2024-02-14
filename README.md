# Projeto de Skins para OTRS Znuny

Este repositório é público e foi dedicado a auxiliar usuários que desejam criar e personalizar skins para aplicar em seus projetos OTRS Znuny, mesmo sem possuir conhecimento técnico avançado. A proposta é simplificar o processo, permitindo que os usuários clonem este repositório, efetuem as alterações necessárias nos arquivos de skin e, por fim, implementem a cópia personalizada em seus servidores OTRS.

Este repositório contém arquivos e pastas necessários para criar e implementar uma nova skin no OTRS Znuny. Veja a baixo mais detalhes

## Estrutura do Repositório

O projeto está estruturado da seguinte forma:

```
skin
|
├── opt
│   ├── znuny-6.5.5
│   │   │   ├── var
│   │   │   │   ├── httpd
│   │   │   │   │   ├── htdocs
│   │   │   │   │   |   ├── skins
│   │   │   │   │   |   |   ├── Agent
│   │   │   │   │   |   |   |   ├── novaskin
│   │   │   │   │   |   |   |   |   ├── css
│   │   │   │   │   |   |   |   |   |   ├── Core.Default.css
│   │   │   │   │   |   |   |   |   ├── img
│   │   │   │   │   |   |   |   |   |   ├── logo.png
│   │   │   ├── Kernel
│   │   │   │   ├── Config
│   │   │   │   │   ├── Files
│   │   │   │   │   |   ├── XML
│   │   │   │   │   |   |   ├── novaSkin.xml
│   │   │   │   │   |   ├── novaSkin.xml
├── README.md
```

- **`opt/znuny-6.5.5/var/httpd/htdocs/skins/Agent/novaskin/css/Core.Default.css`**: Arquivo CSS principal para a nova skin.
- **`opt/znuny-6.5.5/var/httpd/htdocs/skins/Agent/novaskin/img/logo.png`**: Logotipo da nova skin.
- **`opt/znuny-6.5.5/Kernel/Config/Files/novaSkin.xml`**: Configurações específicas para a nova skin.
- **`opt/znuny-6.5.5/Kernel/Config/Files/XML/novaSkin.xml`**: Arquivo XML relacionado à nova skin.

## Como Utilizar

1. Clone este repositório em sua máquina local.
2. Faça as alterações desejadas nos arquivos CSS, imagens e XML (Renomeie a pasta novaskin para o nome desejado da sua skin).
3. Suba os arquivos modificados para os diretórios correspondentes em seu servidor OTRS Znuny.
4. No terminal linux excute cada um dos comando um por vez:

##### Rebuildando
	/opt/otrs/bin/otrs.Console.pl Maint::Config::Rebuild
	
##### Deletando o cache
	/opt/otrs/bin/otrs.Console.pl Maint::Cache::Delete

##### Limpando o cache do sistema
    /opt/otrs/bin/otrs.Console.pl Maint::Loader::CacheCleanup

##### Gerando um novo cache para o sistema
    /opt/otrs/bin/otrs.Console.pl Maint::Loader::CacheGenerate

5. Após feitos todos os passo acima abra o Znuny vá até "Administração" > Configuração do Sistema
6. Na caixa de pesquisa digite 

##### 
    Loader::Agent::DefaultSelectedSkin

7. Clique no botão "Editar esta definição"
8. Altere a skin "default" ou a que estiver setada para o nome que você criou. (Se você não alterou o nome ele será novaskin. o nome que está setado neste projeto)


# Requisitos de Software o Znuny

**Sistema Operacional**
- Linux (Debian or Red Hat preferred)
- Perl 5.16.0 or higher

**Servidor Web**

- Apache 2 + mod_perl2 or higher (recommended)
- Web server with CGI support (CGI is not recommended)

**Banco de Dados**

- MySQL 5.0 or higher
- MariaDB
- PostgreSQL 9.2 or higher
- Oracle 10g or higher

**Navegadores**
 - Estes navegadores **NÃO** são suportados:
  -- Internet Explorer versão anterior a 11
  -- Firefox versão anterior a 31
  -- Safari versão anterior a 6

## Licença
O projeto é distribuído sob a Licença Pública Geral GNU (GPL v3) - consulte o arquivo [COPYING](https://github.com/znuny/Znuny/blob/dev/COPYING) que o acompanha para obter informações gerais sobre a licença. Se precisar de mais detalhes, você pode consultar [aqui](https://snyk.io/learn/what-is-gpl-license-gplv3-explained/).

## Contribuição

Se você achar útil este projeto e desejar contribuir, sinta-se à vontade para realizar um fork e enviar suas melhorias através de pull requests.

Esperamos que este projeto facilite a personalização das skins no OTRS Znuny. Qualquer dúvida ou sugestão, por favor, abra uma [issue](https://github.com/kadim-almeida/skins-para-otrs-znuny/issues).

## Znuny Oficial

Znuny é uma continuação da Edição Comunitária do ((OTRS)) (versão 6.0.30), que foi declarada como fim de vida (EOL) no final de dezembro de 2020.

O principal objetivo deste projeto é fornecer uma versão mantida e estável do conhecido sistema de tickets e aprimorá-lo com novos recursos.Como segundo objetivo é restabelecer uma conexão com a comunidade.

[Baixe a versão oficial atualizada e gratuita](https://github.com/znuny)

## Criador

**Ricardo Almeida**

- <https://twitter.com/kdimalmeida>
- <https://github.com/kadim-almeida>
- <https://www.linkedin.com/in/kdimalmeida/>
