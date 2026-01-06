
# Monty Hall Paradox: A Monte Carlo simulation exercise

> "Suppose you're on a game show, and you're given the choice of three doors: Behind one door is a car; behind the others, goats. You pick a door, say No. 1, and the host, who knows what's behind the doors, opens another door, say No. 3, which has a goat. He then says to you, 'Do you want to pick door No. 2?' Is it to your advantage to switch your choice?"

## About The Project

This project is a **Monte Carlo simulation** designed to prove the counter-intuitive statistical truth behind the famous **Monty Hall Problem**.

While human intuition suggests a 50/50 probability after a door is revealed, probability theory dictates that switching doors actually **doubles** your chances of winning. To demonstrate this without complex equations, I built a Python script that simulates the game **20,000 times**.

### Key Features
* **Pure Logic:** Simulates the game mechanics (Choice -> Reveal -> Switch/Stay).
* **Massive Iteration:** Runs 20,000 cycles to invoke the Law of Large Numbers.
* **Data Visualization:** Uses `Matplotlib` to generate professional, Cyberpunk-styled charts analyzing the win rates.

## Results

The simulation consistently converges to the mathematical probability:

* **Strategy: Keep Original Choice** → ~33.3% Win Rate
* **Strategy: Switch Doors** → ~66.6% Win Ratw

## How to Run

1.  **Clone the repo**
    ```bash
    git clone [https://github.com/tu-usuario/monty-hall-simulation.git](https://github.com/tu-usuario/monty-hall-simulation.git)
    ```
2.  **Install dependencies** (Matplotlib & Numpy)
    ```bash
    pip install matplotlib numpy
    ```
3.  **Run the simulation**
    ```bash
    python monty_hall.py
    ```

## The Logic Behind the Math

Why does switching work?

1.  **Initial State:** There is a 1/3 chance you picked the Car, and a 2/3 chance you picked a Goat.
2.  **The Reveal:** The host *must* reveal a Goat from the remaining doors.
3.  **The Switch:**
    * If you initially picked the **Car** (1/3), switching makes you **LOSE**.
    * If you initially picked a **Goat** (2/3), switching makes you **WIN** (because the host removed the other goat).

Since you are more likely to pick a goat initially (2/3), you are more likely to win by switching.

## Tech Stack

* **Python** (Core Logic)
* **Matplotlib** (Visualization)
* **NumPy** (Data handling)

## Author

**Braulio Gómez**
* LinkedIn: https://www.linkedin.com/in/braulio-g%C3%B3mez-39102631a?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app

---
*This project was inspired by the controversy surrounding Marilyn vos Savant's correct answer to this problem in 1990.*
