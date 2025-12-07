Terminal Typer: A Console Reaction Game

A simple, fast-paced reaction test built in C for the Windows console. The entire game logic and output rely on text manipulation, avoiding any external libraries for sound.

💡 Game Idea

Terminal Typer is designed to test and improve the user's typing speed and reaction time. The player is presented with a single target character (an uppercase letter) and must press the corresponding key before the allocated time limit expires.

The game is entirely driven by the difficulty level, which shortens the time limit allowed for each reaction.

📜 Rules

Objective: Successfully type the displayed character within the time limit.

Scoring: Every correct type increases the score by 1 and advances the level.

Time Limit: The initial time limit is 1000 milliseconds (1 second).

Difficulty: For every successful type, the time limit decreases by 20ms, making subsequent levels faster and harder.

Game Over: The game ends immediately if the player either:

Fails to type the character before the timer hits 0.

Types the wrong character.

🕹️ Controls

The game requires no specific controls other than standard keyboard input.

Action

Input

Reaction

Press the key corresponding to the displayed target character (case-insensitive).

Exit

Close the console window after the "Game Over" screen.

✨ Features

No Sound Dependencies: Built entirely using standard C libraries and windows.h console functions, eliminating the need for mmsystem.h or external audio files.

Difficulty Scaling: Uses variable current_speed to dynamically adjust the time limit, ensuring the game becomes progressively challenging.

High-Resolution Timing: Employs Windows' QueryPerformanceCounter for accurate timing in milliseconds, crucial for a reaction-based game.

Flicker Reduction: Uses SetConsoleCursorPosition (clear_screen_fast) instead of system("cls") for smoother rendering of the game screen between turns.

HUD: Displays the current Level, Score, and the precise remaining Time Limit for the current round
