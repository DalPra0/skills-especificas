# skills-especificas

# Prompts de Contexto — Referência Rápida

Esses dois prompts podem ser colados diretamente em qualquer conversa, mesmo sem ter os skills instalados.

---

## 📥 PROMPT 1 — Salvar Contexto

Cole isso no final de qualquer conversa para salvar tudo:

```
Por favor, salve toda a conversa atual em um arquivo chamado `contexto_projeto.md`.

O arquivo deve conter:

1. **Metadados**: data/hora do salvamento e nome do projeto (se identificável)

2. **Resumo Executivo**: 3-5 linhas sobre o projeto, objetivo e estado atual

3. **Estado do Projeto**:
   - O que foi concluído
   - O que está em progresso
   - O que está pendente ou bloqueado

4. **Artefatos Criados**: tabela com nome, descrição e caminho de cada arquivo gerado

5. **Conversa Completa** — para CADA turno:
   - **Usuário:** (mensagem exata, citada literalmente)
   - **IA:** (resposta completa)
   - **Contexto Mental:** (o raciocínio por trás da resposta — estratégia adotada, alternativas consideradas, por que essa abordagem, incertezas existentes)

6. **Contexto Mental Acumulado**: síntese do modelo mental construído ao longo de toda a conversa — decisões-chave, premissas adotadas, raciocínio geral

7. **Próximos Passos**: lista ordenada do que ainda falta fazer

O objetivo é que uma instância da IA sem nenhum contexto anterior possa ler esse arquivo e retomar o projeto exatamente de onde paramos, com o mesmo nível de entendimento.

Salve o arquivo e confirme o caminho.
```

---

## 📤 PROMPT 2 — Carregar Contexto

Cole isso no início de uma nova conversa para retomar o projeto:

```
Por favor, leia os seguintes arquivos e retome o projeto de onde parou:

1. `contexto_projeto.md` — contexto completo da conversa anterior (obrigatório)
2. `README.md` — visão geral do projeto (se existir)

Após ler, me apresente um briefing com:
- O que é esse projeto e qual o objetivo
- O que já foi feito (lista)
- Onde exatamente paramos (último estado)
- O modelo mental reconstruído: raciocínio acumulado, premissas, decisões-chave já tomadas
- Próximos passos identificados (lista ordenada)

Aja como se essa fosse uma continuação direta da conversa anterior — não preciso reexplicar nada que já estava no arquivo. Após o briefing, me pergunte como desejo continuar.
```

---

## 💡 Como usar

**Para salvar:**
1. No final de qualquer conversa, cole o **Prompt 1**
2. O arquivo `contexto_projeto.md` será criado na pasta do projeto

**Para retomar:**
1. Inicie uma nova conversa
2. Cole o **Prompt 2**
3. A IA vai ler o arquivo e fazer um briefing completo antes de continuar

**Dica:** Se quiser um nome de arquivo diferente, substitua `contexto_projeto.md` pelos dois prompts.

---

## 🔌 Versão com Skills instalados

Se você tiver os skills `save-context` e `load-context` instalados, basta dizer:

- **"salva o contexto"** → dispara o save-context automaticamente
- **"carrega o contexto"** → dispara o load-context automaticamente

Os arquivos `.skill` para instalação estão nessa mesma pasta.
