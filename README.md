# Desafio DevSecOps — Gerenciador de Tarefas

## Sobre o Projeto
Este repositório faz parte do desafio prático do módulo de DevSecOps da ADA Tech.
Você receberá este projeto com vulnerabilidades propositais e uma pipeline incompleta.
Seu objetivo é **implementar a pipeline de segurança** e **corrigir as vulnerabilidades**.

## Estado atual
A pipeline está **incompleta**. Os steps de segurança precisam ser implementados por você.

## Sua missão
1. Implementar os steps de segurança no `pipeline.yml`
2. Fazer a pipeline **quebrar** ao detectar os problemas
3. Corrigir as vulnerabilidades encontradas
4. Fazer a pipeline **passar** com tudo verde ✅
5. Documentar o funcionamento da pipeline neste README

## O que implementar
- [ ] Secrets Scanning com **Gitleaks**
- [ ] SAST com **Semgrep**
- [ ] SCA com **Grype**
- [ ] Deploy com **GitHub Pages**

## Como a pipeline funciona
Esta pipeline implementa práticas de segurança no processo de desenvolvimento, garantindo que nenhuma aplicação vulnerável seja enviada para produção.

🔍 Step 3 — Gitleaks (Secrets Scanning)

O Gitleaks analisa o código e o histórico de commits em busca de informações sensíveis, como:

Senhas
Tokens de API
Chaves privadas

Se qualquer segredo for encontrado, a pipeline falha automaticamente.

Por que isso é importante?
Evita vazamento de credenciais que poderiam comprometer toda a aplicação.

🛡️ Step 4 — Semgrep (SAST)

O Semgrep realiza análise estática de código (SAST), identificando padrões inseguros como:

XSS (Cross-Site Scripting)
SQL Injection
Uso de funções perigosas

Se vulnerabilidades forem detectadas, o build é interrompido.

Por que isso é importante?
Detecta falhas de segurança diretamente no código antes mesmo da aplicação rodar.

📦 Step 5 — Grype (SCA)

O Grype verifica as dependências do projeto em busca de vulnerabilidades conhecidas (CVEs).

A pipeline falha se encontrar vulnerabilidades de severidade média ou alta.

Por que isso é importante?
Mesmo que seu código esteja seguro, bibliotecas externas podem introduzir riscos.

🚫 Break the Build (Regra de Ouro)

O deploy só acontece se todos os passos de segurança passarem.

Isso garante que:

Nenhum código vulnerável chegue à produção
Segurança seja parte obrigatória do processo

## URL de Produção
https://gleycebarbosa.github.io/projeto-devsecops-desafio/
