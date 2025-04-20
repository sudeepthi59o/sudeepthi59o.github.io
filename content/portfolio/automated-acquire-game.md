+++
categories = ["ai"]
coders = ["surebbal","prvs"]
date = 2025-04-12T23:00:00Z
description = "AI-powered automation in the classic Acquire board game"
image = "https://ik.imagekit.io/ys4gkaixy/economy-games-svgrepo-com.svg?updatedAt=1744655154207"
title = "Automated Acquire Game"
type = "post"
[[tech]]
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Python_logo_01.svg?updatedAt=1744511052787"
name = "Python"
url = "https://www.python.org/"
[[tech]]
name = "Pytest"
url = "https://docs.pytest.org/"
logo = "https://ik.imagekit.io/ys4gkaixy/With%20Name%20logos/Pytest_logo.svg?updatedAt=1744656054099"
[[tech]]
name = "JSON"
url = "https://www.json.org/"
logo = "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/json/json-original.svg"
[[tech]]
name = "Game Trees"
url = "https://en.wikipedia.org/wiki/Game_tree"
logo="https://ik.imagekit.io/ys4gkaixy/With%20Name%20logos/Tic-tac-toe-game-tree.svg?updatedAt=1744656309126"
+++

# Automated Acquire Game

The Automated Acquire Game project is a Python-based implementation of the classic board game [Acquire](https://en.wikipedia.org/wiki/Acquire), designed to simulate and automate gameplay. It includes intelligent decision-making algorithms to simulate player behavior and strategic gameplay. The project is structured with a modular object-oriented architecture, handling different components such as gameplay flow, board state management, and AI-driven player logic.

---

## **Key Features**

- **Automated Gameplay**: AI-driven simulation allows the game to play itself with no human input.
  
- **Strategic Player Modeling**: Implements multiple player strategies — ordered, random, largest-alphabetical, and smallest-anti-alphabetical — using game-tree logic to simulate diverse decision-making styles.  
Rather than always selecting the mathematically optimal move, the AI reflects realistic and varied play patterns, offering a richer and more human-like simulation.
  
- **Efficient Game Tree Evaluation (Lazy Generation)**: To manage complexity, the project adopts a lazy generation approach.  
Instead of generating all possible future game states, the AI simulates placing each available tile and generates only immediate permutations of share purchases and replacement tiles — a much smaller and more manageable set.  
Strategy-based pruning is then applied to select the best move according to the player's behavior model.  
A full game board state is generated only for the selected action, dramatically improving efficiency while preserving strategic depth.

- **Board Management**: Automates key gameplay mechanics, including tile placement, hotel formation, mergers, and score calculation.

- **Error Handling and Robustness**: Incorporates fallback mechanisms to handle edge cases, such as unavailable tile placements, ensuring smooth gameplay.

---

## **Impact**

This project adds an AI-powered dimension to a classic strategy board game, showcasing expertise in algorithms, decision trees, and game theory.  
It provides a foundation for developing more sophisticated game-playing AIs or modeling competitive player strategies.  
It also encouraged analysis across multiple simulations to understand which strategies performed better, offering practical insight into player behavior modeling.

---

## **Technologies Used**

- **Python**: Core programming language for game logic and AI behavior.
- **Object-Oriented Programming (OOP)**: Used for modular, extensible, and maintainable design.
- **Game Trees and Lazy Evaluation**: Strategy modeling and efficient search space reduction.
- **AI Algorithms**: Uses rule-based AI agents and lazy game-tree evaluation to simulate autonomous player behavior, strategic tile placement, and share purchasing decisions.
- **Pytest + JSON**: For high-coverage unit tests and scenario validation.

---

## **Future Work**

- **Advanced AI Strategies**: Integrating more sophisticated algorithms that could refine decision-making, allowing the AI to simulate more nuanced and competitive playstyles.
  
- **Graphical User Interface (GUI)**: Adding a GUI to visualize gameplay and improve user experience.

> This project was completed as part of academic coursework and is hosted in a private repository and available upon request.  

![Acquire Game Demo](/images/acquire_demo.gif)  
GIF created with [LiceCap](http://www.cockos.com/licecap/).

---