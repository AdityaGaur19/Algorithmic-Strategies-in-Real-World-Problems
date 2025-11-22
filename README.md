# 🧠 Algorithmic Strategies in Real-World Problem Solving  

### _A comprehensive lab project demonstrating the application of algorithmic paradigms — Greedy, Dynamic Programming, Backtracking, and Brute-Force — to real-world computational problems._

---

## 📘 Overview  

This project explores how **different algorithmic strategies** can efficiently solve distinct classes of **real-world problems**.  
Developed as part of the **Design and Analysis of Algorithms Lab (ENCA351)** under the **BCA (AI & Data Science)** program at **KR Mangalam University**, it highlights the performance, trade-offs, and visual analysis of each algorithmic approach.  

---

## 🧩 Learning Objectives  

- Apply **Greedy, Dynamic Programming, Backtracking, and Brute-Force** algorithms to real scenarios.  
- Visualize **runtime and memory trade-offs** across algorithms.  
- Compare **theoretical and observed** complexities using experimental profiling.  
- Gain practical experience with **algorithm design, optimization, and performance analysis**.

---

## ⚙️ Environment Setup  

The project was built and tested on **Google Colab (Python 3.10)**.  

### 🔧 Install Dependencies
```bash
!pip install matplotlib==3.9.2 numpy==1.26.4 pandas==2.2.2 memory_profiler==0.61.0
````

### 📦 Requirements File

`requirements.txt`

```
matplotlib==3.9.2
numpy==1.26.4
pandas==2.2.2
memory_profiler==0.61.0
itertools
time
```

---

## 📂 Project Structure

```
Algorithmic-Strategies-in-Real-World-Problems/
│
├── algo_strategies_notebook.ipynb     # Main notebook with all implementations
├── images/                            # Performance plots
│   ├── ads_vs_revenue.png
│   ├── knapsack_budget_profit.png
│   ├── sudoku_time_blanks.png
│   └── bruteforce_time_len.png
├── tables/                            # Exported result tables
│   ├── ads_vs_revenue_table.csv
│   ├── knapsack_capacity_results.csv
│   ├── sudoku_time_vs_blanks.csv
│   ├── bruteforce_scaling.csv
│   └── project_summary.csv
├── requirements.txt                   # Dependencies
├── .gitignore                         # Ignored build/cache files
└── README.md                          # Project documentation
```

---

## 💻 Problem Implementations

### 🟩 **1. TV Commercial Scheduling — Greedy Algorithm**

* **Objective:** Schedule ads to maximize revenue before their deadlines.
* **Approach:** Sort ads by descending profit and allocate in available slots.
* **Complexity:** `O(n log n + nD)`
* **Visualization:**

  * Plot — `ads_vs_revenue.png`
  * Table — `ads_vs_revenue_table.csv`

---

### 🟦 **2. Investment Profit Maximization — Dynamic Programming (0/1 Knapsack)**

* **Objective:** Maximize profit without exceeding budget.
* **Approach:** Bottom-up DP to store maximum profit for each sub-capacity.
* **Complexity:** `O(n × C)`
* **Visualization:**

  * Plot — `knapsack_budget_profit.png`
  * Table — `knapsack_capacity_results.csv`

---

### 🟨 **3. Sudoku Solver — Backtracking**

* **Objective:** Fill Sudoku grid so each row, column, and box contains digits 1–9.
* **Approach:** Recursive backtracking with constraint validation.
* **Complexity:** Exponential in empty cells.
* **Visualization:**

  * Plot — `sudoku_time_blanks.png`
  * Table — `sudoku_time_vs_blanks.csv`

---

### 🟥 **4. Password Cracking — Brute-Force**

* **Objective:** Simulate password cracking using all possible character combinations.
* **Approach:** Use `itertools.product()` to test combinations.
* **Complexity:** `O(|charset|^L)`
* **Visualization:**

  * Plot — `bruteforce_time_len.png`
  * Table — `bruteforce_scaling.csv`

---

## 📊 Experimental Profiling

Performance metrics recorded:

* **Runtime (seconds)** via `time.perf_counter()`
* **Memory usage (MB)** via `memory_profiler`
* **Scaling behavior** with varying input sizes

### Example Performance Graphs

| Algorithm           | Visualization                              | Insight                                       |
| ------------------- | ------------------------------------------ | --------------------------------------------- |
| Greedy Scheduling   | ![ads](images/ads_vs_revenue.png)          | Profit growth plateaus with ad volume         |
| Dynamic Programming | ![knap](images/knapsack_budget_profit.png) | Time increases linearly with capacity         |
| Backtracking        | ![sudoku](images/sudoku_time_blanks.png)   | Exponential spike as blanks increase          |
| Brute-Force         | ![brute](images/bruteforce_time_len.png)   | Time grows exponentially with password length |

---

## 🧮 Comparative Summary

| Problem                  | Strategy            | Time Complexity | Space Complexity | Observed Behavior                 |      |                                     |
| ------------------------ | ------------------- | --------------- | ---------------- | --------------------------------- | ---- | ----------------------------------- |
| TV Commercial Scheduling | Greedy              | O(n log n + nD) | O(D)             | Efficient for limited slots       |      |                                     |
| Profit Maximization      | Dynamic Programming | O(nC)           | O(nC)            | Predictable linear growth         |      |                                     |
| Sudoku Solver            | Backtracking        | Exponential     | O(9²)            | Slows sharply for complex puzzles |      |                                     |
| Password Cracking        | Brute-Force         | O(              | charset          | ^L)                               | O(1) | Time explodes with longer passwords |

---

## 📈 Project Summary Table (also exported as `tables/project_summary.csv`)

| Algorithm                      | Strategy            | Domain                | Time Complexity | Space Complexity | Visualization                | Output Table                    |                           |                          |
| ------------------------------ | ------------------- | --------------------- | --------------- | ---------------- | ---------------------------- | ------------------------------- | ------------------------- | ------------------------ |
| TV Commercial Scheduling       | Greedy              | Media & Advertisement | O(n log n + nD) | O(D)             | `ads_vs_revenue.png`         | `ads_vs_revenue_table.csv`      |                           |                          |
| Investment Profit Maximization | Dynamic Programming | Finance & Investment  | O(nC)           | O(nC)            | `knapsack_budget_profit.png` | `knapsack_capacity_results.csv` |                           |                          |
| Sudoku Solver                  | Backtracking        | Gaming / Puzzles      | Exponential     | O(9²)            | `sudoku_time_blanks.png`     | `sudoku_time_vs_blanks.csv`     |                           |                          |
| Password Cracking              | Brute-Force         | Cybersecurity         | O(              | charset          | ^L)                          | O(1)                            | `bruteforce_time_len.png` | `bruteforce_scaling.csv` |

---

## 🧠 Key Insights

* **Greedy** algorithms are fast but not always optimal beyond local constraints.
* **Dynamic Programming** ensures optimal results but consumes more memory.
* **Backtracking** provides precision but is computationally expensive.
* **Brute-Force** illustrates algorithmic limitations and cybersecurity importance.

---

## 🧰 Tools & Environment

| Tool               | Purpose                         |
| ------------------ | ------------------------------- |
| 🐍 Python 3.10+    | Core programming language       |
| 🧮 NumPy           | Random data generation          |
| 📊 Matplotlib      | Visualization                   |
| 📘 Pandas          | Data tables & CSV exports       |
| 🧠 Memory Profiler | Memory usage measurement        |
| ☁️ Google Colab    | Execution environment           |
| 💾 GitHub          | Version control & documentation |

---

## 🧑‍💻 Author

**Aditya Gaur**
🎓 BCA (AI & Data Science), KR Mangalam University
📧 [gauraditya0905@gmail.com](mailto:gauraditya0905@gmail.com)
🔗 [LinkedIn Profile](https://www.linkedin.com/in/adityagaur19)

---

## 🧑‍🏫 Faculty Guide

**Dr. Aarti Sangwan**
Faculty, School of Engineering & Technology
KR Mangalam University

---

## 🛡️ License

This project is open-source under the **MIT License**.
You are free to use, modify, and reference it for educational and research purposes.

---

## 🌟 Acknowledgment

* Guidance by **Dr. Aarti Sangwan**
* Special thanks to the open-source Python and academic communities for continuous innovation.

---

> *“The right algorithm transforms complexity into clarity — every strategy is a step toward smarter problem-solving.”* 💡

````

---

### 📊 Save this CSV as `/tables/project_summary.csv`
```csv
Algorithm,Strategy,Domain,Time Complexity,Space Complexity,Visualization,Output Table
TV Commercial Scheduling,Greedy,Media & Advertisement,O(n log n + nD),O(D),ads_vs_revenue.png,ads_vs_revenue_table.csv
Investment Profit Maximization,Dynamic Programming,Finance & Investment,O(nC),O(nC),knapsack_budget_profit.png,knapsack_capacity_results.csv
Sudoku Solver,Backtracking,Gaming / Puzzles,Exponential,O(9^2),sudoku_time_blanks.png,sudoku_time_vs_blanks.csv
Password Cracking,Brute-Force,Cybersecurity,O(|charset|^L),O(1),bruteforce_time_len.png,bruteforce_scaling.csv
````

---

✅ **Final Deliverables to Include in Repo:**

* `algo_strategies_notebook.ipynb`
* `README.md` (above)
* `requirements.txt`
* `images/` (plots)
* `tables/` (CSV results + summary)
* `.gitignore`

---
