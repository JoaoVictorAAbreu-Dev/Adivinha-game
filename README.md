# Jogo de Adivinhação em C

Um jogo de adivinhação de números desenvolvido em linguagem C, com níveis de dificuldade, sistema de pontuação e interface ASCII art no terminal.

---

## Índice

- [Sobre o Projeto](#sobre-o-projeto)
- [Funcionalidades](#funcionalidades)
- [Pré-requisitos](#pré-requisitos)
- [Como Compilar e Executar](#como-compilar-e-executar)
- [Como Jogar](#como-jogar)
- [Níveis de Dificuldade](#níveis-de-dificuldade)
- [Sistema de Pontuação](#sistema-de-pontuação)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)

---

## Sobre o Projeto

O **Jogo de Adivinhação** é um programa de terminal desenvolvido em C que desafia o jogador a descobrir um número secreto entre **0 e 99**. A cada tentativa, o jogo fornece dicas indicando se o chute foi maior ou menor que o número secreto, enquanto o sistema de pontuação penaliza chutes distantes do alvo.

O número secreto é gerado de forma aleatória a cada execução com base no timestamp do sistema, garantindo uma experiência única a cada partida.

---

## Funcionalidades

- **Número aleatório** gerado por seed de tempo (`time(0)`), garantindo imprevisibilidade
- **3 níveis de dificuldade** com número de tentativas diferentes
- **Sistema de pontuação dinâmico** que desconta pontos conforme a distância do chute ao número secreto
- **Validação de entrada** — impede chutes com números negativos
- **Feedback instantâneo** a cada tentativa (maior ou menor)
- **Interface visual** com ASCII art de vitória e derrota

---

## Pré-requisitos

Para compilar e executar o projeto você precisará de:

- **GCC** (GNU Compiler Collection) ou qualquer compilador C compatível com C99/C11
- **Terminal** (Linux, macOS ou Windows com MinGW/WSL)

Para verificar se o GCC está instalado:

```bash
gcc --version
```

---

## Como Compilar e Executar

**1. Clone ou baixe o repositório:**

```bash
git clone https://github.com/seu-usuario/jogo-adivinhacao.git
cd jogo-adivinhacao
```

**2. Compile o programa:**

```bash
gcc adivinhacao.c -o adivinhacao
```

**3. Execute o jogo:**

```bash
# Linux / macOS
./adivinhacao

# Windows
adivinhacao.exe
```

---

## Como Jogar

1. Ao iniciar, o programa exibirá uma tela de boas-vindas em ASCII art.
2. Escolha um nível de dificuldade digitando `1`, `2` ou `3`.
3. Digite seu chute (um número entre **0 e 99**) a cada rodada.
4. O jogo indicará se o número secreto é **maior** ou **menor** que o seu chute.
5. Acerte o número antes de esgotar suas tentativas para vencer!

---

## Níveis de Dificuldade

| Nível | Nome    | Tentativas |
|-------|---------|------------|
| `1`   | Fácil   | 20         |
| `2`   | Médio   | 15         |
| `3`   | Difícil | 6          |

---

## Sistema de Pontuação

O jogador começa com **1000 pontos**. A cada tentativa errada, pontos são descontados com base na distância entre o chute e o número secreto:

```
Pontos perdidos = |chute - número_secreto| / 2
```

Quanto mais próximo você chuta, menor é a penalidade. O objetivo é acertar com o maior número de pontos possível!

---

## Estrutura do Projeto

```
jogo-adivinhacao/
│
├── adivinhacao.c    # Código-fonte principal
└── README.md        # Documentação do projeto
```

---

## Tecnologias Utilizadas

- **Linguagem:** C (C99)
- **Bibliotecas padrão:** `stdio.h`, `stdlib.h`, `time.h`
- **Compilador recomendado:** GCC

---

## Licença

Este projeto está sob a licença MIT. Sinta-se livre para usar, modificar e distribuir.
