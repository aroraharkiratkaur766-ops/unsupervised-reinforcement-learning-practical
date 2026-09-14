# 🤖 Unsupervised & Reinforcement Learning Practical

## 📌 Project Overview

This practical demonstrates two important areas of Machine Learning:

1. **Unsupervised Learning** – Customer Segmentation using K-Means Clustering
2. **Reinforcement Learning** – Learning through Actions and Rewards

The practical focuses on understanding how Machine Learning concepts can be applied to real-world business decision-making.

---

## 🎯 Learning Objectives

By completing this practical, we understand how to:

* Perform customer segmentation using **K-Means Clustering**
* Identify groups of similar customers
* Interpret customer clusters from a business perspective
* Understand the basic concept of **Reinforcement Learning**
* Identify an **Agent, Action, Environment, and Reward**
* Understand **Exploration vs Exploitation**
* Connect Machine Learning techniques with business applications

---

# Part A: Customer Segmentation Using K-Means

## 💼 Business Problem

An online retailer wants to understand different types of customers.

The available customer information includes:

* **Monthly Spending**
* **App Visits**

K-Means Clustering is used to divide customers into **3 groups (K = 3)**.

---

## 📊 Dataset

The practical uses a small customer dataset containing 8 customers:

| Customer | Monthly Spending | App Visits |
| -------- | ---------------: | ---------: |
| A        |             9000 |         20 |
| B        |             8500 |         18 |
| C        |             1200 |          3 |
| D        |             1500 |          4 |
| E        |             5000 |         10 |
| F        |             5500 |         12 |
| G        |             8800 |         19 |
| H        |             1800 |          5 |

The clustering features are **Monthly Spending** and **App Visits**. Customer names are used only as identifiers.

---

## 🔹 K-Means Clustering

K-Means divides customers into groups based on similarity in their characteristics.

In this practical:

```text
K = 3
```

The model is implemented using:

```python
KMeans(n_clusters=3, random_state=42, n_init=10)
```

---

## 📈 Cluster Results

The model creates three customer groups:

| Cluster   | Customers | Behaviour                                 |
| --------- | --------- | ----------------------------------------- |
| Cluster 0 | C, D, H   | Lower spending and fewer app visits       |
| Cluster 1 | A, B, G   | High spending and high app activity       |
| Cluster 2 | E, F      | Medium spending and moderate app activity |

### Possible Business Interpretation

**Cluster 0 – Low-Engagement Customers**

* Lower spending
* Fewer app visits
* May require re-engagement campaigns

**Cluster 1 – Premium Customers**

* High spending
* High app activity
* Can receive loyalty rewards and personalised recommendations

**Cluster 2 – Medium-Value Customers**

* Moderate spending
* Moderate app activity
* Can be targeted with personalised offers to increase engagement

These business names are interpretations based on customer behaviour; the cluster numbers themselves do not represent good, average, or bad customers.

---

# Part B: Introduction to Reinforcement Learning

## 🤖 What is Reinforcement Learning?

Reinforcement Learning is a type of Machine Learning in which a system learns through interaction.

The basic process is:

```text
Take an Action
      ↓
Receive a Reward
      ↓
Learn from the Result
      ↓
Improve Future Decisions
```

The practical demonstrates this concept using a delivery-route example.

---

## 🚚 Business Scenario

A delivery company has two possible routes:

* Route A
* Route B

The objective is to select the route that generally provides faster delivery.

A faster delivery receives a higher reward, while slower delivery receives a lower reward.

---

## 🎯 Agent, Environment, Action & Reward

| RL Component | Example                                |
| ------------ | -------------------------------------- |
| Agent        | Delivery decision system               |
| Environment  | Roads and traffic                      |
| Action       | Choose Route A or Route B              |
| Reward       | Feedback based on delivery performance |

---

## 📊 Reward Analysis

The practical defines the following rewards:

```text
Route A → [5, 4, 6, 5, 4]
Route B → [8, 9, 7, 10, 8]
```

Average rewards:

| Route   | Average Reward |
| ------- | -------------: |
| Route A |            4.8 |
| Route B |            8.4 |

Therefore, **Route B has the higher average reward** and becomes the best-known route in the example.

---

# 🔄 Exploration vs Exploitation

### Exploration

Exploration means trying a new or less-used option to learn more about it.

**Example:**
Trying Route A even when Route B has previously performed better.

### Exploitation

Exploitation means choosing the option that is already known to perform well.

**Example:**
Choosing Route B because it has produced higher rewards previously.

---

# 🧰 Technologies Used

* Python
* Pandas
* Matplotlib
* Scikit-learn
* K-Means Clustering
* Google Colab
* Jupyter Notebook

---

# 📁 Project Structure

```text
unsupervised-reinforcement-learning-practical/
│
├── part-a/
│   └── unsupervised-learning/
│       ├── Unsupervised_and_Reinforcement_Learning_Practical_Name.ipynb
│       └── customer-segmentation.png
│
├── README.md
└── requirements.txt
```

The practical specifically recommends placing the notebook under:

```text
part-a/unsupervised-learning/
```

and adding a screenshot of the customer-segmentation graph.

---

# 📌 Machine Learning Comparison

| Learning Type          | Main Idea                      | Business Example          |
| ---------------------- | ------------------------------ | ------------------------- |
| Supervised Learning    | Learn from known answers       | Customer churn prediction |
| Unsupervised Learning  | Discover hidden patterns       | Customer segmentation     |
| Reinforcement Learning | Learn from actions and rewards | Route optimization        |

---

# 💡 Key Takeaways

* **K-Means** can identify natural customer groups based on similar behaviour.
* Customer segmentation can support targeted marketing strategies.
* **Reinforcement Learning** allows systems to learn from feedback.
* Rewards help an agent identify actions that produce better outcomes.
* **Exploration** helps discover new possibilities.
* **Exploitation** uses previously successful choices.
* Machine Learning techniques can be connected directly to business decision-making.

---

## 👩‍💻 Practical Submission

This repository contains the Google Colab practical for **Unsupervised Learning and Reinforcement Learning**, including customer segmentation, cluster visualisation, reinforcement learning concepts, reward analysis, and exploration/exploitation examples.
