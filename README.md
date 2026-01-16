# Decentralized Mechanisms: Pricing Online Decisions

This repository contains a LaTeX document exploring how pricing mechanisms can incentivize online agents to make decisions that improve overall social welfare. The work examines two related examples demonstrating how costs can guide decentralized agents to simulate centralized decision-making algorithms.

## Overview

The document covers two main problems:

### 1. The k-Server Problem for Line Metrics
- Demonstrates how the deterministic Double Coverage (DC) algorithm for the k-server problem on a line can be simulated through dynamic pricing
- Shows that natural greedy behavior (choosing the nearest server) leads to arbitrarily bad competitive ratios
- Proves that with appropriate pricing mechanisms, greedy agents can achieve k-competitive performance by weakly simulating the lazy DC algorithm

### 2. The Parking Problem on the Line
- Models a simplified parking scenario where drivers seek to minimize the distance between their parking spot and destination
- Shows that uncoordinated greedy parking decisions result in exponential (O(2^n)) competitive ratio
- Demonstrates how randomized dynamic pricing can incentivize agents to simulate the Harmonic algorithm, achieving O(log n) competitive ratio

## Authors

- **Allan Borodin** (University of Toronto)
- **Denis Pankratov** (University of Toronto)
- **Modified by: Nic Bolton**

## Content

The document provides:
- Formal proofs and theorems for both problems
- Detailed mathematical analysis of pricing mechanisms
- Comparison between centralized optimal solutions and decentralized agent behavior
- Techniques for handling tie-breaking in greedy decisions through perturbation arguments

## Building the Document

This project uses LaTeX to generate the PDF document. To build:

```bash
cd tex
pdflatex pricing-online-decisions.tex
biber pricing-online-decisions
pdflatex pricing-online-decisions.tex
pdflatex pricing-online-decisions.tex
```

Or if you have `latexmk` installed:

```bash
cd tex
latexmk -pdf pricing-online-decisions.tex
```

## Repository Structure

```
.
├── README.md                           # This file
├── tex/
│   ├── pricing-online-decisions.tex    # Main LaTeX document
│   ├── pricing-online-decisions.pdf    # Compiled PDF (generated)
│   ├── openwork.sty                    # Custom LaTeX style file
│   └── references.bib                  # Bibliography references
└── .gitignore                          # Git ignore rules for LaTeX artifacts
```

## Reference

This work is based on research in mechanism design and online algorithms. The document references:

**Pricing Online Decisions: Beyond Auctions**  
Authors: Ilan Reuven Cohen, Alon Eden, Amos Fiat, Łukasz Jeż  
arXiv: [1504.01093](https://arxiv.org/abs/1504.01093) (2015)

## Key Concepts

- **Competitive Ratio**: Measures algorithm performance relative to optimal offline solutions
- **Lazy Algorithms**: Variants where only one server moves per request
- **Mechanism Design**: Using prices to align individual incentives with social welfare
- **Online Algorithms**: Making decisions without knowledge of future requests

## License

Please refer to the original authors for licensing information.
