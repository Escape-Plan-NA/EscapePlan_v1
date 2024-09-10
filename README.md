# Warder and Prisoner Game

## Overview
This project is a simple 2-player game involving a **warder** and a **prisoner**, where both players navigate a 5x5 block map. The objective of the warder is to catch the prisoner, while the prisoner tries to escape by reaching a tunnel block. The game is played over a server-client architecture, with predefined server IP and port set in the source code.

### Key Features:
- 5x5 block grid with randomly placed **free**, **obstacle**, and **tunnel** blocks.
- Two characters: **Warder** and **Prisoner**.
- Players are assigned characters randomly at the start of the game.
- **Turn-based gameplay**: Warder moves first, followed by the prisoner, with a 10-second timer for each turn.
- **Winning conditions**: Warder wins by accessing the block occupied by the prisoner. Prisoner wins by accessing the tunnel block.
- **Game reset**: The server can reset the game and players' scores.

## Game Rules
1. The map consists of:
   - 19 **free** blocks (accessible by both players).
   - 5 **obstacle** blocks (unreachable by both players).
   - 1 **tunnel** block (accessible only by the prisoner).
   
2. **Random Placement**: 
   - At the start of the game, the server randomly places all blocks and characters in the free blocks.
   
3. **Player Assignment**: 
   - Each player is randomly assigned either the warder or prisoner role. The warder moves first.

4. **Turn-based System**: 
   - Each player has 10 seconds to make a move to an adjacent block (up, down, left, or right). If a player fails to move in 10 seconds, the turn is skipped.
   
5. **Winning Conditions**: 
   - **Warder Wins**: If the warder moves to the block where the prisoner is located.
   - **Prisoner Wins**: If the prisoner moves to the tunnel block.
   
6. **Game Over**:
   - Once a player wins, their name and the current scores are displayed. The winning player starts first in the next game.

7. **Reset Button**: 
   - The server has a reset button to restart the game, resetting both the game map and the player scores.

## Server Specifications
- **Server Address and Port**: The server’s IP address and port number are hardcoded into the source code. No need for clients to input this information.
- **Concurrent Clients**: The server tracks and displays the number of concurrent clients and the total number of clients that are online.
- **Reset Feature**: The server can reset the game and players' scores using a reset button.

## Installation and Setup

### Prerequisites:
- Make sure you have **Java** installed on your system as this game is built using Java.

### Clone the Repository:
```bash
git clone https://github.com/your-username/warder-prisoner-game.git
cd warder-prisoner-game
