# 🃏 Poker Genius: Professional Equity Calculator

**Poker Genius** is an advanced web tool for analyzing Texas Hold'em hands. The application combines the functions of an equity calculator, a range visualizer, and a GTO trainer, running entirely in the browser without the need for installation.

The application is designed for both beginners who want to understand poker math and professionals analyzing complex spots.

## 🌐 Live Demo

The application is deployed and ready to use. You don't need to download or install anything.
Simply click the link below to start analyzing hands immediately on any device:

🚀 **[Launch Omni Poker](https://igarok88.github.io/poker-genius/index.html)**

## ✨ Key Features

- **Two Operation Modes:**
  - **Training (Vs Range):** Analyze your hand against an opponent's estimated range (13x13 matrix).
  - **PvP (Hand Vs Hand):** Precise calculation of odds for a specific hand against another specific hand (e.g., AA vs KK).
- **Range Matrix:** An interactive grid for precise tuning of the opponent's spectrum with Drag-and-Drop support (drawing with mouse/finger).
- **Pot Odds Calculator:** A built-in assistant that compares your Equity with pot odds and suggests a move (Call or Fold).
- **Deep Analytics:** A histogram showing not just the win percentage, but the distribution of combinations (how often you will hit a Straight, Flush, Pair, etc.).
- **Professional 4-Color Deck:**
  - ♠ Spades — Dark Grey
  - ♥ Hearts — Red
  - ♣ Clubs — Black
  - ♦ Diamonds — Light Red (Coral)
- **Adaptive Interface:** Convenient to use on both a large monitor and a smartphone with one hand.

---

## 🚀 How to Run

The application is a **Single File Application**. This means it does not require a server, Node.js, or Python installation.

1.  Download the `index.html` file.
2.  Open it in any modern browser (Chrome, Safari, Firefox, Edge).
3.  Done! No internet is required; all calculations happen locally on your device.

---

## 📖 Interface Guide

### 1. Left Panel: Game Field

- **Hero (You):** Slots for your hole cards.
- **Board:** Slots for community cards (Flop, Turn, River).
- **Villain (Opponent):** Appears only in _PVP_ mode.
- **Matrix (In Training Mode):**
  - **Yellow cells (diagonal):** Pocket Pairs (22-AA).
  - **Blue cells (top right):** Suited hands.
  - **Green cells (bottom left):** Offsuit hands.
  - _Controls:_ Click cells or click-and-drag to select an area. Use presets (All, Top 20%) for quick filling.

### 2. Right Panel: Analytics

- **WIN EQUITY:** Your probability of winning in the long run.
  - Green color: You are a favorite (>50%).
  - Red/Yellow: You are an underdog.
- **Pot Calculator:** Enter the **Pot** size and the opponent's **Bet (Call)**. The system automatically calculates Expected Value (EV) and suggests a decision.
- **Histogram (Bars):** Shows the top 4 probable combinations you are likely to hit by the river.

### 3. Bottom Panel: Deck (Picker)

- Keyboard for selecting cards. Already selected cards are dimmed to avoid duplicates.
- Cards display rank and suit in the 4-color format.

---

## 🧠 Usage Examples and Strategies

### Scenario 1: Preflop All-in

You want to know how profitable it is to go all-in with **Jacks (JJ)** against a tight player.

1.  Switch to **Training** mode.
2.  Set your hand to `J♠ J♦`.
3.  In the matrix, select the **Top 20%** preset or manually select only strong hands (AA, KK, QQ, AK).
4.  **Result:** You will see that against a very strong range (QQ+, AK), you have only ~36% equity. This is an easy fold.

### Scenario 2: Hunting for Outs (Draw)

You have a **Flush Draw** on the flop. You want to understand if you should call a bet.

1.  **Hero:** `A♥ 5♥`.
2.  **Board:** `K♥ 9♥ 2♣` (You need one more Heart).
3.  Enter the pot size (e.g., 1000) and the opponent's bet (e.g., 500).
4.  **Analysis:**
    - Chance to hit a flush by the river is ~36%.
    - Pot odds require 33% equity (500 / 1500).
    - **Verdict:** The app will show **CALL**, as 36% > 33%. Mathematically, this is a profitable action.

### Scenario 3: Analyzing a "Cooler"

You lost with a Full House against Quads. Was it bad luck or a mistake?

1.  Switch to **PVP (Hand vs Hand)** mode.
2.  Set exact cards for yourself and the opponent.
3.  Set the board cards.
4.  Check the Equity. Most likely, in such a situation, the odds shifted drastically on a single card. This helps understand the nature of variance and avoid tilt.

---

## 🛠 Technical Details

- **Core:** Pure JavaScript (Vanilla JS).
- **Simulation:** Monte Carlo method (600-1000 iterations) for instant probability calculation.
- **Performance:** Optimized Hand Evaluator algorithms without using heavy libraries.
- **UI/UX:** CSS Grid/Flexbox for full responsiveness on any screen.

---

### License

Free for personal use and learning.
