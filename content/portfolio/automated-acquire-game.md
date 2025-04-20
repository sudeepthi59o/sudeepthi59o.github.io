+++
categories = ["ai"]
coders = ["surebbal","prvs"]
date = 2025-04-12T23:00:00Z
description = "AI-powered automation in the classic Acquire board game"
image = "https://ik.imagekit.io/ys4gkaixy/economy-games-svgrepo-com.svg?updatedAt=1744655154207"
title = "Automated Acquire Game"
type = "post"
weight = 1
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

<p style="font-size: 1.8rem;">The Automated Acquire Game project is a Python-based implementation of the classic board game <a href="https://en.wikipedia.org/wiki/Acquire">Acquire</a>, designed to simulate and automate gameplay. It includes intelligent decision-making algorithms to simulate player behavior and strategic gameplay. The project is structured with a modular object-oriented architecture, handling different components such as gameplay flow, board state management, and AI-driven player logic.</p>

---

## <p style="font-size: 1.8rem;">**Key Features**</p>

<ul>
  <li><p style="font-size: 1.8rem;"><strong>Automated Gameplay</strong>: AI-driven simulation allows the game to play itself with no human input.</p></li>
  
  <li><p style="font-size: 1.8rem;"><strong>Strategic Player Modeling</strong>: Implements multiple strategies (ordered, random, largest-alphabetical, smallest-anti-alphabetical) using game-tree logic, simulating varied decision-making. The AI prioritizes strategy over the mathematically optimal move, resulting in more realistic gameplay.</p></li>
  
  <li><p style="font-size: 1.8rem;"><strong>Efficient Game Tree Evaluation (Lazy Generation)</strong>: To manage complexity, the project adopts a lazy generation approach. Instead of generating all possible future game states, the AI simulates placing each available tile and generates only immediate permutations of share purchases and replacement tiles — a much smaller and more manageable set. Strategy-based pruning is then applied to select the best move according to the player's behavior model. A full game board state is generated only for the selected action, dramatically improving efficiency while preserving strategic depth.</p></li>
  
  <li><p style="font-size: 1.8rem;"><strong>Board Management</strong>: Automates key gameplay mechanics, including tile placement, hotel formation, mergers, and score calculation.</p></li>
  
  <li><p style="font-size: 1.8rem;"><strong>Error Handling and Robustness</strong>: Includes mechanisms to handle edge cases, such as unavailable tile placements, ensuring smooth gameplay.</p></li>
</ul>

---

<p style="font-size: 1.8rem;"><strong>Impact</strong></p>

<p style="font-size: 1.8rem;">This project adds an AI-powered dimension to a classic strategy board game, showcasing expertise in algorithms, decision trees, and game theory. It provides a foundation for developing more sophisticated game-playing AIs or modeling competitive player strategies. It also encouraged analysis across multiple simulations to understand which strategies performed better, offering practical insight into player behavior modeling.</p>

---

<p style="font-size: 1.8rem;"><strong>Technologies Used</strong></p>

<ul>
  <li><p style="font-size: 1.8rem;"><strong>Python</strong>: Core programming language for game logic and AI behavior.</p></li>
  
  <li><p style="font-size: 1.8rem;"><strong>Object-Oriented Programming (OOP)</strong>: Used for modular, extensible, and maintainable design.</p></li>
  
  <li><p style="font-size: 1.8rem;"><strong>Game Trees and Lazy Evaluation</strong>: Strategy modeling and efficient search space reduction.</p></li>
  
  <li><p style="font-size: 1.8rem;"><strong>AI Algorithms</strong>: Uses rule-based AI agents and lazy game-tree evaluation to simulate autonomous player behavior, strategic tile placement, and share purchasing decisions.</p></li>
  
  <li><p style="font-size: 1.8rem;"><strong>Pytest + JSON</strong>: For high-coverage unit tests and scenario validation.</p></li>
</ul>

---

<p style="font-size: 1.8rem;"><strong>Future Work</strong></p>

<ul>
  <li><p style="font-size: 1.8rem;"><strong>Advanced AI Strategies</strong>: Integrating more sophisticated algorithms that could refine decision-making, allowing the AI to simulate more nuanced and competitive playstyles.</p></li>
  
  <li><p style="font-size: 1.8rem;"><strong>Graphical User Interface (GUI)</strong>: Adding a GUI to visualize gameplay and improve user experience.</p></li>
</ul>

<p style="font-size: 1.8rem;">This project was completed as part of academic coursework and is hosted in a private repository and available upon request.</p>

![Acquire Game Demo](/images/acquire_demo.gif)  
GIF created with <a href="http://www.cockos.com/licecap/">LiceCap</a>.

---