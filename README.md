# 🔍 MINIC Lexical Analyzer / Scanner

Analisador léxico (scanner) para a linguagem **MINIC**, desenvolvido em duas implementações equivalentes: **C** e **Python**. O projeto lê arquivos de código-fonte (`.minic` ou `.c`), identifica tokens com suas respectivas coordenadas/atributos e gera diagnósticos detalhados para erros léxicos em formato JSON Lines (`.jsonl`).

---

## 📌 Funcionalidades

- **Reconhecimento de Tokens**: Suporte a palavras reservadas (`if`, `else`, `while`, `int`, etc.), identificadores, literais (`INT_LIT`, `FLOAT_LIT`, `CHAR_LIT`, `STRING_LIT`) e operadores/pontuações (`==`, `!=`, `&&`, `{`, `}`, `;`, etc.).
- **Tratamento Avançado de Erros**: Detecta e categoriza erros como literais malformados, identificadores inválidos, strings/caracteres não terminados e zero à esquerda em numéricos.
- **Mecanismo de Recuperação**: Emite os símbolos estruturais válidos (ex: `)`, `;`) mesmo após a ocorrência de erros em literais não terminados.
- **Saída Estruturada**: Emite tokens diretamente na saída padrão (`stdout`) como objetos JSON por linha (`.jsonl`).
- **Geração Automática de Logs de Erro**: Grava erros encontrados em arquivos na pasta `errors/`.
- **Suíte de Testes Automatizada**: Scripts em Bash para validar a conformidade das implementações contra gabaritos esperados.

---

## 📁 Estrutura do Repositório

```text
.
├── scanner.c             # Implementação do analisador léxico em C
├── scanner.py            # Implementação do analisador léxico em Python
├── testar_scanner_c.sh   # Script de testes para a versão em C
├── testar_scanner_py.sh  # Script de testes para a versão em Python
└── errors/               # Pasta gerada automaticamente contendo os relatórios de erro
