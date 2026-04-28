	📖 Objective
The goal of this project is to analyze a DNA sequence using a Hidden Markov Model (HMM) and determine the most probable sequence of hidden states (Exon, Splice Site, Intron).

🧬 Problem Description
We are given:

A DNA sequence

Transition probabilities between states

Emission probabilities for nucleotides

States used:

s → Start

E → Exon

5 → Splice site

I → Intron

e → End

⚙️ Methodology
1. Model Definition
Transition matrix defines movement between states

Emission matrix defines probability of nucleotides (A, C, G, T)

2. Log Probability Calculation
Log scale is used to avoid numerical underflow

Probabilities are added instead of multiplied

3. Path Evaluation
Multiple possible state sequences were tested:

Different splice positions (E → 5 → I)

One sequence with only Exon states

4. Comparison
Log probabilities were computed for each sequence

The sequence with highest probability (least negative value) was selected

📊 Results
Tested sequences and their probabilities:

EEEEEE5IIIIIIIIIIIIIIIIIII
EEEEEEEE5IIIIIIIIIIIIIIIII
EEEEEEEEEEEE5IIIIIIIIIIIII
EEEEEEEEEEEEEEE5IIIIIIIIII
EEEEEEEEEEEEEEEEEE5IIIIIII
EEEEEEEEEEEEEEEEEEEEEE5III
EEEEEEEEEEEEEEEEEEEEEEEEEE
✅ Final Output:
Most probable state sequence:
EEEEEEEEEEEEEEEEEEEEEEEEEE
🧠 Interpretation
The model predicts that the entire sequence is Exon (E)

Transition to splice site (5) is not favored due to lower transition probability

Hence, no exon–intron boundary is detected

🛠️ Tools Used
Python

NumPy

Math (log functions)

🚀 Conclusion
This project demonstrates how Hidden Markov Models can be used for gene prediction. The results depend heavily on transition and emission probabilities, which influence whether biological features like splice sites are detected.
