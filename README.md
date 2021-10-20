# Docs
Repositório para documentações a respeito de práticas das equipes de desenvolvimento do TRE-TO


# Git

Regras de uso do Git/Gitlab.

Sempre ao comitar, utilizar mensagens informativas sobre o que foi alterado no código, e incluir o número da tarefa. Exemplo: "#30123 Iniciado o cadastro de usuários".

## Fluxo durante desenvolvimento
1. Ao iniciar uma tarefa: criar branch a partir da branch develop, com nome no padrão #<num_tarefa>. Exemplo: #30123.
2. Enquanto atua em uma tarefa: a cada dia, comitar e fazer "push" do trabalho realizado na branch da tarefa (criada no item 1).
3. Ao concluir a tarefa:
    1. commitar e fazer "push" na branch da tarefa.
    2. mudar para a branch "develop". Exemplo: `git checkout develop`
    3. fazer "rebase" da branch da tarefa sobre a branch "develop". Exemplo: `git rebase "#30123"`.
    4. fazer "git push" do branch "develop".
    5. verificar se o trabalho foi atualizado no ambiente de homologação (iniciado automatica e imediatamente via Jenkins, pode demorar alguns minutos para concluir).
    6. excluir a branch da tarefa remotamente. Exemplo: `git push origin -d "#30123"`. Se quiser, excluir a branch da tarefa localmente.
