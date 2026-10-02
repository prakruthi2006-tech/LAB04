# Lab 4: VibeCoding - Dino Run Repair Lab 

## Name - Prakruthi.NK

## SRN - PES2UG24AM118

## LAB - 04

##  Project Overview
This project is a single-file side-scrolling endless-runner clone using Pygame. It introduces students to obstacle spawning, jump-state tracking, and simple file-based persistence using a small, readable object-oriented codebase.

This repository contains the completed Lab 4 (VibeCoding) submission. The original broken code was analyzed, debugged, and enhanced using an AI assistant (LLM) as a pair-programming partner to fix the bug and implement the missing features.

##  Setup & Running the Game

**Requirements:**
* Python 3.10+
* Pygame

**Installation:**
```bash
pip install pygame

Run the game:

bash
python game.py
Controls:

Space, Up Arrow, or W: Start the game and jump.

Same keys to restart after a Game Over.

 Completed Tasks & Code Changes
The following tasks were successfully completed for this lab:

Task 1: Fixed the high-score bug
Issue: The comparison logic in Game.update was backwards, preventing the high score from updating.

Fix: Changed the condition to correctly compare the current run's score against the stored high score.

python
# Before (Buggy):
if self.high_score > current:
    self.high_score = current
    save_high_score(self.high_score)

# After (Fixed):
if current > self.high_score:
    self.high_score = current
    save_high_score(self.high_score)
Task 2: Implemented dino_tint(on_ground)
Implementation: Returns a blue color (0, 0, 255) when the dino is airborne, and None (default green) when on the ground.

python
def dino_tint(on_ground):
    if on_ground:
        return None
    else:
        return (0, 0, 255)  # Blue color while jumping
Task 3: Implemented on_obstacle_passed(obstacle, score)
Implementation: Prints a message to the terminal indicating the obstacle was cleared and the current score.

python
def on_obstacle_passed(obstacle, score):
    print(f"Obstacle passed! Current Score: {score}")
Task 4: Implemented max_jumps()
Implementation: Returns 2 to enable a double jump mechanic.

python
def max_jumps():
    return 2  # Allows a double jump
 Submission Deliverables
As per the lab instructions, the following deliverables are located in the Lab-4/ folder within this repository:

before.mp4: A 10-second video showing the original gameplay and the high-score bug.

after.mp4: A 10-second video showing the fixed gameplay with the new features (double jump, color change, high score saving).

chat_history.pdf: The complete exported chat history with the AI assistant used for debugging and pair-programming.

Updated Code: The modified game.py file containing all fixes and new features.

🛠️ Technologies Used
Python 3

Pygame

AI Assistant (ChatGPT/Claude/Gemini) for Vibe Coding

Git & GitHub for version control
