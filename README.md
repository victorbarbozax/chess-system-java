<div align="center">

# ♟️ Chess System Java

### *Where every move is a matter of logic — and legacy.*

> A fully object-oriented chess engine built from scratch in Java,  
> designed with clean architecture, layered design patterns, and terminal-based gameplay.


</div>

---

## 📖 The Story Behind This Project

Most chess implementations are black boxes — you call a method, pieces move, and you have no idea why.

This project was built with the opposite philosophy:  
**every rule, every move, every exception is explicit, traceable, and yours to understand.**

Built as part of a structured Java OOP curriculum, `chess-system-java` is not just a game —  
it's a demonstration of how real-world software architecture should feel:  
layered, extensible, and honest about what it does.

---

## ✅ Features

| Feature | Description |
|---|---|
| ♟️ **Full Move Validation** | Each piece computes its own legal moves via `possibleMoves()` |
| 🎯 **Possible Move Highlight** | After selecting a source, the board highlights all valid targets |
| 🏗️ **Layered Architecture** | Clean separation between `boardgame`, `chess`, and `application` layers |
| 🚨 **Custom Exception Hierarchy** | `BoardException` → `ChessException` for precise error handling |
| 🎨 **ANSI Terminal UI** | Colored output using ANSI escape codes — white vs yellow pieces |
| 🔒 **Input Validation** | Handles invalid positions and wrong moves without crashing |
| 📐 **Generic Board Engine** | The `boardgame` layer is fully reusable for any grid-based game |

---

## 🏛️ Architecture

The project is structured in three strict layers — each with a single responsibility:

```
chess-system-java/
│
├── src/
│   ├── application/        # Entry point & terminal UI
│   │   ├── Program.java    # Main game loop
│   │   └── UI.java         # Board rendering & input reading
│   │
│   ├── chess/              # Chess-specific rules & logic
│   │   ├── ChessMatch.java      # Match controller
│   │   ├── ChessPiece.java      # Abstract chess piece
│   │   ├── ChessPosition.java   # Human-readable coordinates (a1–h8)
│   │   ├── ChessException.java  # Chess-layer exceptions
│   │   └── Color.java           # WHITE / BLACK enum
│   │
│   └── boardgame/          # Generic, reusable board engine
│       ├── Board.java           # Grid management
│       ├── Piece.java           # Abstract piece contract
│       ├── Position.java        # Matrix coordinates
│       └── BoardException.java  # Board-layer exceptions
```

### Layer Dependency Rule

```
application  →  chess  →  boardgame
```

Upper layers depend on lower layers. Never the reverse.

---

## 🛠️ Tech Stack

| Technology | Version | Role |
|---|---|---|
| **Java** | OpenJDK 26 | Core language |
| **OOP Principles** | — | Abstraction, Inheritance, Polymorphism, Encapsulation |
| **ANSI Escape Codes** | — | Terminal color rendering |
| **Git** | — | Version control |

---

## 🚀 Quick Start

### Prerequisites

- Java JDK 17 or higher
- Git

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-username/chess-system-java.git

# 2. Navigate to the project directory
cd chess-system-java

# 3. Compile the source files
javac -sourcepath src -d classes src/application/Program.java

# 4. Run the game
java -cp classes application.Program
```

### How to Play

```
1. The board is printed with coordinates a–h (columns) and 1–8 (rows)
2. Enter the source position (e.g: e2)
3. Valid moves are highlighted on the board
4. Enter the target position (e.g: e4)
5. Repeat until checkmate
```

---

## 🎮 Gameplay Preview

```
8 R N B Q K B N R
7 P P P P P P P P
6 - - - - - - - -
5 - - - - - - - -
4 - - - - - - - -
3 - - - - - - - -
2 p p p p p p p p
1 r n b q k b n r
  a b c d e f g h

Source: e2
```

After selecting a source, valid destination squares are highlighted in blue directly on the board.

---

## 🗺️ Roadmap

- [x] Board rendering with ANSI colors
- [x] Move validation per piece type
- [x] Possible move highlighting
- [ ] Turn system (WHITE → BLACK → WHITE)
- [ ] Check and checkmate detection
- [ ] Special moves: castling, en passant, promotion
- [ ] Captured pieces display
- [ ] Full standard initial board setup

---

## 🤝 Contributing

Contributions are welcome and appreciated.

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m "add: your feature description"`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

Found a bug? Please open an [Issue](https://github.com/your-username/chess-system-java/issues) with a clear description and steps to reproduce.

---

## 📄 License

This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.

---

<div align="center">

*Built with precision. Designed with purpose.*

</div>
