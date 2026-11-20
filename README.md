# Example_CCv2

Projeto de estudo e experimentação com o **Claude Code**, a CLI de agentes de código da Anthropic.

## Objetivo

Este repositório serve como ambiente prático para explorar recursos do Claude Code, como:

- Geração e edição de arquivos assistida por IA
- Integração com servidores **MCP** (Model Context Protocol), como o servidor do GitHub
- Fluxos de trabalho com Git (commit, push) executados pelo agente
- Skills, hooks e configurações personalizadas

## Pré-requisitos

- [Claude Code](https://claude.com/claude-code) instalado
- [Git](https://git-scm.com/)
- Um token de acesso pessoal (PAT) do GitHub, caso use o servidor MCP do GitHub

## Configurando o servidor MCP do GitHub

Defina o token como variável de ambiente (nunca o coloque diretamente em arquivos versionados):

```powershell
$env:GITHUB_PAT = "seu_token_aqui"
```

Depois registre o servidor no Claude Code:

```bash
claude mcp add-json github '{"type":"http","url":"https://api.githubcopilot.com/mcp","headers":{"Authorization":"Bearer ${GITHUB_PAT}"}}'
```

Use `/mcp` dentro do Claude Code para verificar a conexão.

## Como usar

```bash
git clone https://github.com/marceliino/Example_CCv2.git
cd Example_CCv2
claude
```

## Estrutura

```
Example_CCv2/
└── README.md
```

## Licença

Projeto de uso pessoal para fins de estudo.
