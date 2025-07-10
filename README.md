# Vehicle Routing with Simultaneous Delivery and Pickup (VRPSDP) using Artificial Bee Colony (ABC)

## 📦 Project Overview

This project implements a complete simulation and optimization pipeline for solving the **Vehicle Routing Problem with Simultaneous Delivery and Pickup (VRPSDP)** using the **Artificial Bee Colony (ABC)** metaheuristic. It models realistic logistics systems involving multiple depots, vehicles with capacity constraints, and customers with two-way demand (delivery and pickup).

The solution is animated using Matplotlib to visually demonstrate the optimization process and how vehicle routes evolve over iterations.

---

## ✨ Features

* **Multi-Depot Support**: Vehicles can start and end at different depot locations.
* **Simultaneous Delivery and Pickup**: Each customer has both delivery and pickup requirements.
* **Capacity-Constrained Routing**: Each vehicle has a maximum capacity, and solutions violating this are discarded.
* **Artificial Bee Colony Optimization**: Implements employed, onlooker, and scout bee phases with order crossover (OX) for route evolution.
* **Real-Time Visualization**: Animated route updates using Matplotlib’s `FuncAnimation`.
* **Modular Design**: Structured into reusable classes (`Customer`, `Depot`, `VRPSDP`, `Solution`, `ABC_Colony`).

---

## 🧮 Problem Statement

Given:

* A set of depots
* A fleet of vehicles (identical capacity)
* A set of customers, each with a delivery and pickup demand

Find:

* A set of vehicle routes that start and end at depots
* Routes that serve all customers exactly once
* The total distance is minimized
* Vehicle capacities are not exceeded at any point

---

## 🏗️ Project Structure

```
├── main.py                  # Main file with visualization and simulation logic
├── vrpsdp_classes.py        # Contains class definitions (Customer, Depot, VRPSDP, etc.)
├── abc_algorithm.py         # ABC optimization logic with crossover and evaluation
├── README.md                # Project documentation
```





## 📊 Example Output

* Multiple colored routes showing vehicle paths from depots to customers
* Animated progression over 100 iterations of ABC
* Print output like:

  ```
  >> Iteration completed, best cost so far: 142.38
  ```

---

## 🔍 Key Algorithms Used

* **Artificial Bee Colony (ABC)**

  * Employed Bees: Explore solutions using order crossover
  * Onlooker Bees: Exploit based on fitness-based selection
  * Scout Bees: Replace stagnated solutions
* **Order Crossover (OX)**: Used to combine parent routes while preserving order and feasibility
* **Capacity Filter**: Invalid routes with excessive load are automatically discarded

---

## 📈 Visualization

* Built using `matplotlib.animation.FuncAnimation`
* Routes are color-coded per vehicle
* Animation reflects iterative improvement over time

---

## 📚 Citation

This project was inspired by and partially based on the methodology described in the following paper:

> **Fuat Şimşir**, **Dursun Ekmekci**.
> *A metaheuristic solution approach to capacitated vehicle routing and network optimization.*
> **Engineering Science and Technology, an International Journal**, Volume 22, Issue 3, 2019, Pages 727–735.
> [https://doi.org/10.1016/j.jestch.2019.01.002](https://doi.org/10.1016/j.jestch.2019.01.002)


---

## 👤 Author

Sumit — developed as part of summer activities after 2nd year of undergraduation.

Feel free to reach out for collaborations or questions!
