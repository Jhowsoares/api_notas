# 📝 API Notas

[![CI/CD — Minha API](https://github.com/Jhowsoares/api_notas/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/Jhowsoares/api_notas/actions)
[![OpenAPI Spec](https://img.shields.io/badge/OpenAPI-3.0.0-green.svg)](https://swagger.io/)
[![Documentation](https://img.shields.io/badge/Docs-Redoc-blue.svg)](https://jhowsoares.github.io/api_notas/)

A **API Notas** é um ecossistema completo para o gerenciamento de notas de alunos por meio de operações CRUD básicas e completas. O projeto foi desenvolvido seguindo o padrão OpenAPI 3.0.0, garantindo contratos de dados consistentes, respostas em formato JSON e autenticação segura baseada em tokens.

---

## 🌐 Documentação Oficial da API

A documentação interativa e completa da API foi gerada pelo Redoc e está publicada no GitHub Pages. Você pode acessar os detalhes de payloads, schemas e códigos de retorno no link abaixo:

🔗 **[Acessar Documentação da API Notas](https://jhowsoares.github.io/api_notas/)**

---

## 🛠️ Funcionalidades e Endpoints

A API expõe os seguintes endpoints estruturados sob a tag `/notas`:

* **`GET /notas`**: Lista todas as notas cadastradas no sistema com suporte integrado a paginação estruturada (`cursor` e `limit`).
* **`POST /notas`**: Cadastra a nota de um novo aluno (Campos obrigatórios: `nome_aluno` e `valor_nota`).
* **`GET /notas/{id}`**: Busca de forma isolada os detalhes e metadados de uma nota específica através de seu ID.
* **`PUT /notas/{id}`**: Atualiza por completo as informações de uma nota existente no banco de dados.
* **`DELETE /notas/{id}`**: Remove em definitivo o registro de uma nota do sistema.

---

## 🔒 Segurança

Todas as rotas da API são protegidas, exigindo autenticação do tipo **Bearer Token (JWT)**.
* **Nome do Esquema:** `bearerAuth`
* **Formato:** JWT (JSON Web Token)

---

## 🤖 Este Repositório possui Automação (CI/CD)

Este projeto utiliza um robô automático via **GitHub Actions** (`.github/workflows/ci-cd.yml`). A cada modificação enviada para o repositório (`git push`), o robô executa as seguintes etapas de forma isolada:

1. **Integração Contínua (CI):** Baixa o código e utiliza a ferramenta **Spectral** para validar se o contrato `openapi.yaml` segue estritamente as regras de boas práticas e sintaxe padrão do ecossistema OpenAPI.
2. **Entrega Contínua (CD):** Caso a validação passe com sucesso, o robô chama a CLI do **Redoc**, transforma o arquivo YAML em uma interface HTML estática moderna e faz o upload automático do artefato para o **GitHub Pages**.