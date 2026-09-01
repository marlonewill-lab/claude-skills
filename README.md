# claude-skills

Repositório pessoal de [Skills do Claude](https://docs.claude.com) — instruções reutilizáveis que estendem o comportamento do Claude para tarefas específicas, sem precisar reescrever o mesmo prompt a cada conversa.

## Skills disponíveis

| Skill | O que faz |
|---|---|
| [`revisor-textual`](./revisor-textual) | Revisa, corrige e aprimora textos em português — gramática, clareza, coesão, estrutura — preservando a voz autoral. Também ajuda a compor textos de gênero específico (cartas formais, e-mails institucionais, dissertações) quando o rascunho ainda não tem os elementos estruturais exigidos pelo gênero. |
| [`prompt-architect`](./prompt-architect) | Projeta e refina prompts de sistema para o Claude, em sintaxe XML nativa, aplicando princípios de atenção do Transformer (ativação primária, isolamento semântico, efeito de recência). |

Veja o `README.md` de cada pasta para detalhes de funcionamento e exemplos de acionamento.

## Como usar uma skill

- **Claude.ai / Claude Desktop**: baixe o `SKILL.md` da pasta correspondente e envie pela seção de Skills nas configurações — o Claude reconhece automaticamente pelo `name` e `description` do frontmatter, sem precisar invocação manual.
- **Claude Code**: copie a pasta da skill inteira para o diretório de skills do projeto ou do usuário, conforme a documentação oficial de Skills do Claude Code.
- Cada skill aciona sozinha quando o pedido do usuário corresponde à descrição no frontmatter do `SKILL.md` — não é necessário chamar por nome.

## Estrutura

```
claude-skills/
├── revisor-textual/
│   ├── SKILL.md
│   └── README.md
└── prompt-architect/
    ├── SKILL.md
    └── README.md
```
