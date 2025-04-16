## 🧩 Prefabs

### 🚀 NaveDoJogador
- **Descrição**: Nave controlada pelo jogador durante o combate.
- **Quando são utilizados**: Durante todo o gameplay.
- **Componentes**:
  - **Sprite**: Nave principal.
  - **Colisor**: Box Collider 2D.
  - **Fonte de Áudio**: Efeitos de tiro e dano.
  - **Scripts**:
    - `ControladorNave`: Controla movimento com teclas e mira.
    - `Disparo`: Gerencia a criação dos projéteis.
    - `Vida`: Reduz vida ao colidir com inimigos ou projéteis.

---

### 👾 InimigoNave
- **Descrição**: Naves inimigas que atacam o jogador.
- **Quando são utilizados**: Em todas as fases, com dificuldade crescente.
- **Componentes**:
  - **Sprite**: Naves pequenas, médias ou grandes.
  - **Colisor**: Box Collider 2D.
  - **Fonte de Áudio**: Explosão ao morrer.
  - **Scripts**:
    - `MovimentoInimigo`: Movimento automático em direção ao jogador.
    - `AtaqueInimigo`: Atira projéteis em intervalos.
    - `Vida`: Destrói o inimigo ao chegar a 0.

---

### 🐙 CriaturaEspacial
- **Descrição**: Inimigo especial em forma de criatura (tipo polvo).
- **Quando são utilizados**: Todo momento (Inimigo mais dificil).
- **Componentes**:
  - **Sprite**: Criatura animada com tentáculos.
  - **Colisor**: Polygon Collider 2D.
  - **Fonte de Áudio**: Rugido, ataque especial.
  - **Scripts**:
    - `MovimentoTentacular`: Movimento aleatório com padrão de perseguição.
    - `AtaqueEspecial`: Lança múltiplos projéteis em todas as direções.
    - `Vida`: Mostra barra de vida e destrói com animação especial.

---

### 💥 Projetil
- **Descrição**: Projéteis disparados pela nave do jogador ou inimigos.
- **Quando são utilizados**: Sempre que há disparos.
- **Componentes**:
  - **Sprite**: Tiro pequeno com brilho.
  - **Colisor**: Circle Collider 2D.
  - **Scripts**:
    - `MovimentoProjetil`: Movimento contínuo na direção disparada.
    - `Dano`: Aplica dano ao colidir com inimigos ou jogador.

---

### 🔊 GerenciadorDeAudio
- **Descrição**: Controla os efeitos sonoros e músicas do jogo.
- **Quando são utilizados**: Durante todo o jogo.
- **Componentes**:
  - **Fonte de Áudio**: Músicas de fundo, tiros, explosões, efeitos de fase.
  - **Scripts**:
    - `AudioManager`: Reproduz sons com base em eventos do jogo (ex: colisão, morte, transição de fase).
