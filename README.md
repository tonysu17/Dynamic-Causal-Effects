# Estimating Dynamic Causal Effects Using an Approximated Bayesian LSTM

This repository contains the code and methodologies developed in collaboration with **Tony Su** and **Raad Khraishi** (UCL Institute of Finance and Technology, and Data AI Innovation Lead at NatWest). The project leverages an **approximated Bayesian Long Short-Term Memory (LSTM)** network to estimate dynamic causal effects of policies or shocks over time, with a focus on counterfactual scenario analysis and uncertainty quantification.

---

## **Project Overview**

Dynamic causal effects are critical for understanding time-dependent impacts of interventions, such as financial policies or economic shocks. Traditional econometric models often fail to capture the non-linear, long-term dependencies present in complex systems like economies. This project addresses these challenges by:

1. Using **deep learning** to compute counterfactual periods, enabling the estimation of dynamic causal effects.
2. Quantifying uncertainty using **Monte Carlo dropout**, providing posterior sampling for probabilistic confidence intervals.
3. Demonstrating the approach on the Dutch economy during the **2008 global financial crisis**, showing a cumulative loss of $15,656 in real GDP per capita and a total GDP decline of approximately $261 billion from 2008 to 2014.

---

## **Key Features**

- **Counterfactual Estimation**:
  - Predicts "what-if" scenarios using LSTM to estimate periods without the observed intervention.
  - Captures dynamic impacts across various time horizons, offering insights into immediate and lagged effects.

- **Uncertainty Quantification**:
  - Uses Monte Carlo dropout to simulate posterior distributions.
  - Provides uncertainty intervals, enhancing model reliability and interpretability.

- **Flexible Architecture**:
  - Employs a simple but robust Bayesian LSTM to handle non-linearities and long-term dependencies in time-series data.

---

## **Highlights of the Methodology**

- **Interrupted Time-Series Analysis**:
  - Combines pre-treatment and post-treatment data to compute counterfactual periods.
  - Estimates dynamic causal effects by comparing the observed ground truth with the counterfactual.

- **Monte Carlo Dropout for Bayesian Inference**:
  - Approximates posterior distributions through multiple stochastic forward passes.
  - Quantifies epistemic uncertainty efficiently and computationally inexpensively.

- **Case Study**: 
  - Application to the **Dutch economy** during the 2008 financial crisis:
    - Point-wise effects show significant GDP contraction immediately after the crisis.
    - Cumulative effects highlight long-term economic scarring.

---
## **Getting Started**

### **Installation**

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/dynamic-causal-effects.git
   cd dynamic-causal-effects
Install dependencies:
bash
Copy code
pip install -r requirements.txt

## **Running the Project**
Preprocess the data:

Run the data_preprocessing.ipynb notebook to scale and split time-series data.
Train the Bayesian LSTM:

Use the model_training.ipynb notebook to train the model on pre-treatment data.
Perform Counterfactual Analysis:

Execute the counterfactual_analysis.ipynb notebook to estimate counterfactual periods and compute causal effects.

## **Results**
**Model Accuracy**:
Achieved a low mean squared error of 0.000210 on normalized training data.

**Causal Effects**:
Point-wise and cumulative effects quantified the long-term impact of the 2008 financial crisis on Dutch GDP.
Uncertainty Intervals:

Prediction intervals demonstrated high reliability (PICP = 1), with narrow confidence bounds enhancing precision.

## **Collaborators**
Tony Su: University College London (UCL)
Raad Khraishi: UCL Institute of Finance and Technology, Data AI Innovation Lead at NatWest
Acknowledgements
This work builds on foundational studies in causal inference, Bayesian deep learning, and interrupted time-series analysis, with applications inspired by macroeconomic policy evaluation.

## **License**
This project is licensed under the MIT License. See the LICENSE file for details.
