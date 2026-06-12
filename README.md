# Diagnóstico do Líder Aumentado por IA

Ferramenta web (HTML estático) do programa **Factfulness / Líder Aumentado por IA**.

## Estrutura

```
index.html        → página inicial (escolhe Aluno ou Instrutor)
aluno/index.html  → diagnóstico do participante  → /aluno
instrutor/index.html → painel do instrutor       → /instrutor
```

## GitHub Pages

O site é publicado via **GitHub Pages** a partir da branch `main` (raiz `/`).

- Aluno: `https://andrefmb.github.io/diagnosticoIA/aluno/`
- Instrutor: `https://andrefmb.github.io/diagnosticoIA/instrutor/`

O arquivo `.nojekyll` desabilita o processamento Jekyll para servir os arquivos como estão.

## Dados (Turso)

As respostas são gravadas numa base [Turso](https://turso.tech) via HTTP. As credenciais
ficam **mascaradas** (base64 invertido) no JavaScript — isso é apenas ofuscação leve, **não
criptografia**. Como o app grava direto do navegador, o token é tecnicamente recuperável por
qualquer pessoa com acesso ao código.

> **Importante:** revogue/rotacione o token no painel do Turso ao fim do uso. Para o painel do
> instrutor, idealmente use um token somente-leitura.
