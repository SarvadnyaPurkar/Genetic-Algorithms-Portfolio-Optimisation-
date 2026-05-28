# Portfolio Optimization using Genetic Algorithms

## Overview

This project implements a **Genetic Algorithm based Portfolio Optimization system** for selecting an optimal stock portfolio using financial performance metrics.

The algorithm evaluates multiple stocks using:

* Sharpe Ratio
* Treynor Ratio
* Jensen’s Alpha

and applies evolutionary optimization techniques such as:

* Selection
* Crossover
* Mutation

to identify the best portfolio configuration under a fixed portfolio size constraint.

---

## Objective

The goal of this project is to use **Genetic Algorithms (GA)** to determine the most suitable combination of stocks that maximizes portfolio fitness while satisfying investment constraints.

---

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* yFinance

---

## Dataset

Historical stock data is fetched using the `yfinance` API.

### Stocks Used

* Apple (AAPL)
* Microsoft (MSFT)
* Amazon (AMZN)
* Google (GOOGL)
* Tesla (TSLA)
* Johnson & Johnson (JNJ)
* Procter & Gamble (PG)
* Coca-Cola (KO)
* Intel (INTC)
* IBM

### Market Benchmark

* S&P 500 (`^GSPC`)

### Time Period

* January 2022 to January 2023

---

## Financial Metrics

### Sharpe Ratio

Measures risk-adjusted return.

### Treynor Ratio

Measures return earned per unit of systematic risk.

### Jensen’s Alpha

Measures portfolio performance relative to expected market return.

These metrics are combined to generate a fitness score for each stock.

---

## Genetic Algorithm Workflow

### 1. Population Initialization

Random binary portfolios are generated where:

* `1` indicates stock selected
* `0` indicates stock not selected

### 2. Fitness Evaluation

Each portfolio is evaluated based on:

* Financial metric scores
* Portfolio constraints
* Fixed ticket size investment

### 3. Selection

Tournament selection is used to select parent portfolios.

### 4. Crossover

Single-point crossover combines parent portfolios to create offspring.

### 5. Mutation

Random mutation introduces diversity into the population.

### 6. Evolution

The process repeats for multiple generations until convergence.

---

## Parameters Used

| Parameter                 | Value    |
| ------------------------- | -------- |
| Population Size           | 100      |
| Number of Generations     | 500      |
| Mutation Rate             | 0.05     |
| Crossover Rate            | 0.95     |
| Portfolio Size Constraint | 4 Stocks |

---

## Output

The project:

* Prints the fittest portfolio in each generation
* Tracks fitness progression over generations
* Visualizes convergence using a fitness graph

---

## Fitness Convergence Graph

The following graph is generated to visualize optimization progress:

* X-axis → Generations
* Y-axis → Best Fitness Score

This helps analyze how the algorithm converges toward an optimal portfolio.

---

## How to Run

### Install Dependencies

```bash
pip install numpy pandas matplotlib yfinance
```

### Run the Notebook

Open the Jupyter Notebook and execute all cells:

```bash
jupyter notebook
```

---

## Project Structure

```text
Genetic Algorithms Portfolio Optimisation/
│
├── Genetic Algorithms(Portfolio Optimisation).ipynb
├── README.md
```

---

## Applications

* Portfolio Optimization
* Financial Decision Making
* Evolutionary Computing
* Quantitative Finance
* Algorithmic Investment Strategies

---

## Future Improvements

Possible enhancements include:

* Dynamic portfolio weighting
* Multi-objective optimization
* Risk minimization constraints
* Real-time stock updates
* Comparison with traditional optimization methods

---

## Conclusion

This project demonstrates how Genetic Algorithms can effectively solve complex portfolio optimization problems by simulating natural evolutionary processes. The approach provides an intelligent and flexible method for selecting high-performing stock portfolios under practical investment constraints.
