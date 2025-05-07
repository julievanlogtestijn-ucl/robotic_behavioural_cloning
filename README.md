# 🤖 Robotic Behavioural Cloning

Coursework for the **"Deep Representations and Learning"** module in the MSc AI for Biomedicine and Healthcare.

---

## 🧠 Project Overview

This project focuses on **behavioural cloning**, a supervised learning technique for training robotic agents using demonstration data. The core objective is to learn a policy function:

\[
f:\mathcal{X} \rightarrow \mathcal{Y}
\]

Where:
- \(\mathcal{X}\) represents the **observation space**
- \(\mathcal{Y}\) represents the **action space**

Given a dataset of observation-action pairs:

\[
d = \{(x_1, y_1), ..., (x_n, y_n)\}
\]

the goal is to learn a model that maps robot observations to appropriate actions.

---

## 📦 Dataset Description

The dataset contains demonstration trajectories where a robotic arm is required to:
- **Pick up** objects
- **Drop** objects (if holding one) in a designated location

Each **trajectory** is a sequence of:
- \(x_i\): A set of observations at time \(i\)
- \(y_i\): The action taken at time \(i\)

### 🧾 Observations (\(\mathcal{X}\)) include:
- `front_cam_ob`: Third-person camera view of the scene
- `mount_cam_ob`: First-person view from the robotic arm’s mounted camera
- `ee_cartesian_pos_ob`: End-effector position and orientation coordinates
- `ee_cartesian_vel_ob`: End-effector velocity
- `joint_pos_ob`: Gripper joint position

### 🎯 Actions (\(\mathcal{Y}\)) include:
- 3D movement coordinates for the robotic arm
- Discrete gripper actions: open, close, or no movement

📚 **More information** on the dataset can be found here:  
[clvr_jaco_play_dataset GitHub Repo](https://github.com/clvrai/clvr_jaco_play_dataset?tab=readme-ov-file)

---

## 📌 Tasks

The coursework is structured into three main tasks:

### ✅ Question 1: End-to-End Supervised Learning
- Evaluate a proposed deep learning architecture that takes in all observations and predicts both types of actions.
- Propose and implement a new model architecture to improve upon the baseline.

### 🔁 Question 2: Self-Supervised Learning with a VAE
- Develop and tune a **Variational Autoencoder (VAE)** to learn a latent representation of the observations.
- Use this latent space as input to a downstream supervised behaviour cloning model.

### ⚖️ Question 3: Comparative Evaluation
- Compare the performance of:
  - The best end-to-end model from Question 1
  - The VAE + supervised head model from Question 2
- Evaluate both models on the provided test set.

---

## 🚀 Goals
- Improve behaviour cloning performance using deep representation learning
- Explore the utility of self-supervised learning in robotic policy training
- Gain hands-on experience with multimodal inputs and sequential data

---
