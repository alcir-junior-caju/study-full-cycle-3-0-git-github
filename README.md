# Curso Full Cycle 3.0 - Módulo Padrões e técnicas avançadas com Git e Github

<div>
    <img alt="Criado por Alcir Junior [Caju]" src="https://img.shields.io/badge/criado%20por-Alcir Junior [Caju]-%23f08700">
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%23f08700">
</div>

---

## Descrição

O Curso Full Cycle é uma formação completa para fazer com que pessoas desenvolvedoras sejam capazes de trabalhar em projetos expressivos sendo capazes de desenvolver aplicações de grande porte utilizando de boas práticas de desenvolvimento.

---

## Repositório Pai
https://github.com/alcir-junior-caju/study-full-cycle-3-0

---

## Visualizar o projeto na IDE:

Para quem quiser visualizar o projeto na IDE clique no teclado a tecla `ponto`, esse recurso do GitHub é bem bacana

---

### Assinar Commit
- Instalar o GPG via brew;
- gpg --list-secret-key --keyid-form LONG;
- gpg --full-generate-key;
- gpg --armor --export ID_KEY
- Copiar a chave gerar;
- Gerar uma chave no github em settings -> SSH and GPG keys;
- Pegar o ID gerado e adicionar nas configs do git:
    - git config --global user.signingKey ID_KEY;
    - Adicionar variável de ambiente no terminal: export GPG_TTY=$(tty);
    - Editar o arquivo do terminal;
- Assinar por padrão o commit:
    - git config --global commit.gpgsign true;
    - git config --global tag.gpgsign true;
- Assinar apenas alguns commits sem ativar o padrão:
    - colocar no commit -S;
- Verificar assinatura:
    - git log --show-signature -1;

### Branches
- Trocar o Branch padrão;
- Proteger a Branch com CODEOWNERS;
- Exigir commits assinados;

### Pull Request / Templates
- [Template](https://github.com/embeddedartistry/templates/blob/master/.github/PULL_REQUEST_TEMPLATE.md)

### Code Owners
- Adicionar automaticamente quem faz o review do código;
- Pode se definir arquivos que tenham seus revisores:
    - *.js @user;
    - *.go @user1;

### SemVer
- MAJOR - API Pública;
- MINOR - Adicionando funcionalidade, mas compatível com a API;
- PATCH - Bugs e ajustes;
- MAJOR = 0 - API instavel, pode mudar a qualquer momento;
- [SemVer](https://semver.org/lang/pt-BR/)
