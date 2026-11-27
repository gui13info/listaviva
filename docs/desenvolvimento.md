# Guia de desenvolvimento

## Organização do monorepo

- `frontend/` abrigará a aplicação Angular e TypeScript, com o código em `src/`, o manifesto npm e o lockfile.
- `backend/` abrigará a API REST em Java e Spring Boot, com o wrapper da ferramenta de build escolhida.
- `infrastructure/` reunirá o Docker Compose e os exemplos de configuração para o ambiente de desenvolvimento.
- `docs/` reúne os requisitos, as convenções e as decisões técnicas do projeto.
- `database/` fica previsto caso scripts ou migrations precisem de um diretório próprio.
- `.agents/` fica previsto para agentes, skills e workflows de apoio ao desenvolvimento.

## Convenções

- Escreva a documentação em português e use nomes de classes, funções, variáveis e demais identificadores de código em inglês.
- Use UTF-8 e inclua uma nova linha no fim de cada arquivo. Siga o `.editorconfig` para a indentação e o tratamento de espaços finais.

## Branches e Pull Requests

1. Crie uma branch de trabalho a partir de `origin/main` para cada alteração. Toda alteração em `main` deve chegar por Pull Request.
2. Mantenha o PR pequeno e restrito ao escopo aprovado. Revise o diff, execute as verificações aplicáveis e descreva no PR o que mudou e o que foi verificado.
3. Abra o PR com `main` como base. Todo PR exige revisão humana antes do merge.
4. Agentes de IA podem implementar, verificar e abrir PRs dentro do escopo aprovado. Agentes de IA não podem dar a aprovação definitiva nem realizar merges em `main`.
5. Somente Guilherme, responsável pelo projeto, pode decidir e executar o merge em `main`.
