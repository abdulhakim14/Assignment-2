## Rock, Paper, Scissors Game – Python Project

This article demonstrates how to create a **Rock, Paper, Scissors** game using Python's **Tkinter** module. The game is a simple hand-based game, where two players simultaneously choose one of three shapes: **Rock**, **Paper**, or **Scissors**. 

In this implementation, the user competes against the computer.

---

### Game Rules
The winner is determined based on the following conditions:
1. **Paper vs. Scissors**: Scissors win.
2. **Rock vs. Scissors**: Rock wins.
3. **Paper vs. Rock**: Paper wins.
4. If both the player and the computer choose the same shape, the result is a **Draw**.

---

### Tools and Technologies
1. **Tkinter**: A Python library for building graphical user interfaces (GUIs). It is simple and effective for creating GUI applications.
2. **Random**: A Python module used to generate random selections (used for the computer's choices).
3. **PIL (Python Imaging Library)**: This library enables image processing tasks, such as resizing, flipping, and displaying images.

---

### GUI Implementation

#### **Part 1: Image Handling**
1. **Import Required Modules**:
   - Import **Tkinter** for GUI development.
   - Import **ImageTk** and **Image** from **PIL** for handling image processing.
   - Import the **random** module for the computer's random choice generation.

2. **Window Creation**:
   - Create the main window object named `root`.
   - Set the window title to **"Rock Paper Scissor"**.
   - Define the window dimensions as **800×680**.

3. **Canvas and Labels**:
   - Create a canvas with dimensions **800×680**.
   - Add labels for the Player, Computer, and "Vs":
     - Player: Font -> *Algerian*, Size -> *25*, Positioned at (*80, 20*).
     - Computer: Font -> *Algerian*, Size -> *25*, Positioned at (*560, 20*).
     - "Vs": Font -> *Algerian*, Size -> *40*, Positioned at (*370, 230*).

4. **Default Image Setup**:
   - **Player's Default Image**:
     - Load and resize the default image (*default.jpg*) to **(300, 300)**.
   - **Computer's Default Image**:
     - Flip the default image horizontally using the `transpose()` function.
   - Display both images using `Tk.PhotoImage` on the canvas.

5. **Image Handling for Rock, Paper, and Scissors**:
   - For each choice (Rock, Paper, Scissors), create separate images for the player and computer. 
   - Use `transpose()` to flip the computer’s images horizontally.
   - Load each image onto the canvas using `Tk.PhotoImage`.

6. **Selection Image**:
   - Load an image (*selection.jpg*) showing combined hand gestures (Rock, Paper, Scissors).
   - Resize it to **(300, 130)** and display it on the canvas.

---

#### **Part 2: Game Logic**
1. **Game Function**:
   - Define a list, `select`, containing values `1`, `2`, and `3`, representing Rock, Paper, and Scissors respectively.
   - Use `random.choice()` to generate the computer's selection.

2. **Player's Choice**:
   - Display the player's choice on the canvas using `create_image()`. 
   - Update the player’s side based on their selected option (Rock, Paper, or Scissors).

3. **Computer's Choice**:
   - Display the computer's choice on the canvas using `create_image()`.
   - Update the computer’s side based on the randomly chosen option.

4. **Result Calculation**:
   - Compare the player’s and computer’s choices:
     - **Draw**: If both choose the same option.
     - **Player Wins**: 
       - Rock beats Scissors.
       - Paper beats Rock.
       - Scissors beat Paper.
     - **Computer Wins**: In all other cases.
   - Display the result as text on the canvas, positioned at **(390, 600)** with font *Algerian* and tag `'result'`.

5. **Buttons**:
   - **Clear Button**: Resets the game to its default state by removing the result and restoring the default images.
   - **Rock Button**: Sets the player’s choice to Rock.
   - **Paper Button**: Sets the player’s choice to Paper.
   - **Scissors Button**: Sets the player’s choice to Scissors.

---

### Summary
This Python project creates an interactive **Rock, Paper, Scissors** game using Tkinter for the GUI and PIL for image handling. Randomness is incorporated for the computer’s selections, making the game dynamic and engaging. Various images (default, Rock, Paper, Scissors) are displayed in real time based on the player's and computer’s choices, and the winner is determined based on the predefined rules.
