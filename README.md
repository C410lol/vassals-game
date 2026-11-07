# Vassals

**Vassals** é um jogo 2D de plataforma desenvolvido em **C++ e SFML**. O projeto foi construído com foco na aplicação de Programação Orientada a Objetos, organização de entidades de jogo, gerenciamento de estados e implementação de sistemas próprios para controlar a execução do jogo.

Um dos principais aspectos do projeto é a implementação da estrutura da engine e dos sistemas centrais do jogo em C++, utilizando a SFML como biblioteca para recursos gráficos, janela, áudio e entrada.

## 🎮 Sobre o jogo

O jogo possui fases de plataforma com personagens controláveis, inimigos e obstáculos com comportamentos distintos. A estrutura inclui:

- Menus para navegação, seleção de jogadores e fases.
- Estados separados para menu e execução do jogo.
- Fases organizadas em classes próprias.
- Personagens controláveis e sistema de inimigos.
- Inimigos terrestres, voadores e um chefe.
- Obstáculos como plataformas, espinhos e melecas, com comportamentos específicos.
- Projéteis e elementos de interação com as entidades do cenário.
- Menus de pausa, pontuação e ranking.
- Arquivos locais utilizados para persistência de dados de jogo e pontuações.

## 🧩 Organização e conceitos aplicados

O código está separado em módulos que representam as principais responsabilidades do jogo:

- **Entidades:** classes-base e especializações para personagens, inimigos, projéteis e obstáculos.
- **Fases:** construção e gerenciamento das fases do jogo.
- **Estados:** controle da transição entre menu e jogo.
- **Gerenciadores:** gerenciamento gráfico, de colisões e de estados.
- **Menus:** componentes e telas de navegação, pausa, jogadores, pontuação e ranking.
- **Observer:** estrutura para comunicação de eventos de entrada entre o sujeito e os observadores.

Essa organização permite separar a lógica do jogo em componentes com responsabilidades específicas e facilita a manutenção e evolução do projeto.

## 🧰 Tecnologias

- **C++11**
- **SFML 2.x** — janela, gráficos, áudio e entrada.
- **CMake 3.16+**
- Programação Orientada a Objetos
- Padrão Observer

## 📁 Estrutura do projeto

```
vassals-jogo/
├── assets/       # Imagens, fontes, cenários e recursos do jogo
├── fases-template/ # Arquivos de configuração das fases
├── includes/     # Cabeçalhos organizados por módulo
├── src/          # Implementações das classes
├── salvamentos/  # Arquivos locais de pontuação e salvamento
├── main.cpp
└── CMakeLists.txt
```

## ▶️ Como compilar e executar

### Pré-requisitos

- CMake 3.16 ou superior.
- Compilador C++ com suporte a C++11.
- SFML com os módulos `system`, `window`, `graphics` e `audio`.

Em distribuições Linux baseadas em Debian/Ubuntu, a biblioteca pode ser instalada com:

```bash
sudo apt update
sudo apt install build-essential cmake libsfml-dev
```

### Build

Na raiz do repositório:

```bash
cmake -S . -B build
cmake --build build
```

O executável é configurado pelo CMake para ser gerado no diretório `bin/`. Em Linux, execute:

```bash
./bin/jogo
```

No Windows, o `CMakeLists.txt` espera encontrar a distribuição SFML 2.6.2 no caminho `tools/SFML-2.6.2`, conforme a configuração específica da plataforma.

---

Projeto desenvolvido no contexto acadêmico da disciplina de Técnicas de Programação.
