# prompt-architect

## O que faz

Projeta, estrutura e refina prompts de sistema e prompts operacionais em sintaxe XML nativa para o Claude, aplicando princípios de atenção da arquitetura Transformer (ativação primária, isolamento semântico, efeito de recência) para maximizar previsibilidade comportamental e reduzir alucinação.

## Quando aciona

Pedidos para criar, escrever, estruturar, revisar ou otimizar um "system prompt", instruções de comportamento para um agente/assistente de IA, ou para "transformar isso num prompt" — mesmo sem usar os termos técnicos "prompt engineering" ou "XML". Também aciona quando o pedido é para definir papel, restrições ou formato de resposta de um agente Claude.

## Como funciona

1. **Classifica a tarefa** numa de três faixas de complexidade — simples, moderada, ou agente autônomo/complexo — antes de escrever qualquer coisa, para não gerar um prompt curto demais para uma tarefa crítica nem um prompt inchado para um pedido trivial.
2. **Segue uma ordem canônica de blocos** (`<role>`, `<context>`, `<intent>`, `<tools>`, `<references>`, `<constraints>`, `<examples>`, `<output_format>`, `<workflow>`, `<action>`), incluindo só os blocos que a faixa de complexidade exige.
3. **Entrega o prompt pronto para cópia**, junto com o diagnóstico da faixa escolhida, a fundamentação arquitetural da ordem de blocos, e as lacunas de informação que ainda precisam da confirmação do usuário.

Também sabe editar um prompt já gerado anteriormente sem reconstruir do zero, preservando a faixa de complexidade original a menos que a mudança pedida justifique reclassificar.

## Instalação

Copie o arquivo `SKILL.md` desta pasta para o diretório de skills do seu ambiente Claude — veja o `README.md` na raiz do repositório para instruções por plataforma (Claude.ai, Claude Desktop ou Claude Code).
