# 🏨 Hotel Bom Pra Cachorro

> Jogo de lógica em Python desenvolvido como atividade prática de programação de nível básico.
> 

**Autora:** Emanuele Kmiecik

**Ambiente:** VSCode 

---

## 📖 Sobre o Projeto

**Hotel Bom Pra Cachorro** é um jogo interativo de raciocínio lógico baseado em terminal. O jogador assume o papel de gerente de um hotel peculiar, onde os hóspedes são animais com regras rígidas de convivência. O desafio consiste em alocar corretamente cada personagem nos quartos disponíveis, respeitando as restrições impostas — sem que nenhum hóspede seja devorado pelo outro!

O projeto demonstra a aplicação prática de conceitos fundamentais de Python, como funções, estruturas condicionais, laços de repetição e arte ASCII.

---

## 🎮 Personagens

| Personagem | Descrição |
| --- | --- |
| 🐶 **Cão** | Hóspede agressivo — devora o Osso se ficarem no mesmo andar |
| 🐱 **Gato** | Predador natural — come o Rato se forem vizinhos |
| 🐭 **Rato** | Vulnerável — foge do Gato e devora o Queijo |
| 🧀 **Queijo** | Item — desaparece se ficar perto do Rato |
| 🦴 **Osso** | Item — é destruído se ficar ao lado do Cão |

---

## 📏 Regras do Hotel

As seguintes combinações de quartos **são proibidas** (personagens não podem ser vizinhos de andar):

- 🐭 Rato **não pode** ficar ao lado do 🐱 Gato
- 🐶 Cão **não pode** ficar ao lado do 🦴 Osso
- 🐱 Gato **não pode** ficar ao lado do 🐶 Cão

> O hotel possui **8 quartos** distribuídos em **2 andares** com **4 quartos** cada. Quartos ocupados por hóspedes fixos são exibidos como `X X X X X` no mapa.
> 

---

## 🏆 Fases do Jogo

O jogo é composto por **4 fases** progressivas, cada uma adicionando novos personagens e aumentando a complexidade do desafio.

### Fase 1 — Introdução ao Hotel

- Personagens disponíveis: **Gato** e **Rato**
- Objetivo: Alocar os dois personagens sem que fiquem em quartos vizinhos
- Recompensa: ⭐ (1 estrela)

### Fase 2 — Chegada dos Cães

- Personagens disponíveis: **2 Cães** e **Osso**
- O hotel já tem hóspedes fixos; os quartos livres são limitados
- Objetivo: Posicionar o Osso longe de todos os Cães
- Recompensa: ⭐⭐ (2 estrelas)

### Fase 3 — O Equilíbrio Delicado

- Personagens disponíveis: **Gato**, **Rato** e **Osso**
- Múltiplas combinações possíveis, mas apenas uma está correta
- Objetivo: Alocar todos sem violações de vizinhança
- Recompensa: ⭐⭐⭐ (3 estrelas)

### Fase 4 — Desafio Final

- Personagens disponíveis: **2 Queijos** e **Osso**
- Fase mais complexa, com mais restrições simultâneas
- Objetivo: Completar a alocação sem erros
- Recompensa: ⭐⭐⭐⭐ (4 estrelas) + 🏆 Troféu de Vitória

---

## 🖥️ Como Executar

### Pré-requisitos

- [Python 3.x](https://www.python.org/downloads/) instalado
- [VSCode](https://code.visualstudio.com/) (recomendado) ou qualquer terminal

### Passos

```jsx
# 1. Clone o repositório
git clone https://github.com/seu-usuario/hotel-bom-pra-cachorro.git

# 2. Acesse a pasta do projeto
cd hotel-bom-pra-cachorro

# 3. Execute o jogo
python hotel.py
```

> ✅ Nenhuma dependência externa é necessária. O projeto usa apenas `os` da biblioteca padrão do Python.
> 

---

## 📂 Estrutura do Código

```
hotel-bom-pra-cachorro/
├── hotel.py          # Código principal do jogo
├── requirements.txt  # Dependências (biblioteca padrão — nenhuma instalação necessária)
├── .gitignore        # Arquivos ignorados pelo Git
└── README.md         # Este arquivo
```

---

## 💡 Conceitos de Python Aplicados

| Conceito | Aplicação no Projeto |
| --- | --- |
| **Funções (`def`)** | Modularização do código em blocos reutilizáveis |
| **Estruturas condicionais (`if/elif/else`)** | Validação das escolhas do jogador |
| **Laços de repetição (`while`)** | Loop do menu principal e reexibição de fases |
| **`input()` / `int()`** | Captura e conversão de dados do usuário |
| **`print()`** | Renderização da interface textual e arte ASCII |
| **Bibliotecas externas** | Importação de `pandas`, `numpy` e `matplotlib` |
| **`output.clear()`** | Atualização dinâmica da interface no Colab |

---

## 📊 Resultados Possíveis

```
✅ Fase concluída → Estrelas acumuladas + avança para próxima fase
❌ Erro de alocação → GAME OVER com mensagem explicativa
🏆 Todas as fases → Troféu + mensagem de parabéns
```

---

