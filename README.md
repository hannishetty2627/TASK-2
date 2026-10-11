# Dining Philosophers Problem — Semaphore and Monitor

## 📌 Project Overview

This project implements the classic **Dining Philosophers Problem** from Operating Systems using two synchronization approaches:

1. Semaphore-based solution
2. Monitor-based solution

The simulation demonstrates how multiple philosophers share a limited number of chopsticks while avoiding synchronization problems such as race conditions and deadlock.

## 🎯 Objective

The main objective is to understand process synchronization and resource sharing in an Operating System.

The implementation demonstrates:
- Synchronization between multiple philosophers.
- Safe sharing of chopsticks.
- Prevention of two philosophers using the same chopstick simultaneously.
- Philosopher states: Thinking, Hungry, and Eating.
- Visualization of state changes using an HTML simulation.

## 🍽️ Problem Description

There are **4 philosophers sitting around a circular table with 4 chopsticks**.

Each philosopher alternates between thinking and eating. To eat, a philosopher needs the chopsticks on both sides.

Since chopsticks are shared resources, synchronization is required to prevent conflicts.

## 🔹 1. Semaphore-Based Solution

The semaphore-based approach uses semaphores to control access to shared chopsticks.

### How it works
- Each chopstick is protected by synchronization.
- A philosopher requests the required chopsticks before eating.
- The philosopher releases the chopsticks after eating.
- Other philosophers can use the released chopsticks.
- Synchronization prevents multiple philosophers from using the same chopstick simultaneously.

## 🔹 2. Monitor-Based Solution

The monitor-based approach uses a monitor abstraction with locks and condition variables to coordinate philosophers.

### How it works
- Each philosopher has a state: THINKING, HUNGRY, or EATING.
- A philosopher becomes hungry when requesting to eat.
- The monitor checks whether the philosopher's neighboring philosophers are eating.
- If eating is safe, the philosopher is allowed to eat.
- After eating, the philosopher releases the shared synchronization control and notifies waiting philosophers.

## 📊 Semaphore vs Monitor

| Feature | Semaphore | Monitor |
|---|---|---|
| Synchronization | Semaphores | Lock and condition variables |
| Resource control | Controls chopstick access | Coordinates philosopher states |
| State management | Depends on implementation | Usually managed inside the monitor |
| Main purpose | Prevent resource conflicts | Organize safe access to shared resources |

## 🌐 HTML Simulation

The HTML simulation displays the philosophers' states and chopstick ownership as the program executes.

It helps visualize:
- Which philosopher is thinking, hungry, or eating.
- Which chopsticks are currently in use.
- How synchronization controls access to shared resources.
- How the state of the system changes during execution.

**Note:** The HTML visualization is animated only if the implementation includes code that updates the display over time.

## 🛠️ Technologies Used

- Programming language: [Add the language used]
- Operating Systems concepts
- Semaphores
- Locks and condition variables
- HTML, CSS, and JavaScript for visualization (if used)

## 📚 Concepts Learned

- Process synchronization
- Critical sections
- Mutual exclusion
- Deadlock prevention
- Shared resource management
- Semaphores and monitors

## 🚀 How to Run

1. Download or clone this repository.
2. Open the source-code files using the appropriate editor or IDE.
3. Run the semaphore-based solution.
4. Run the monitor-based solution separately.
5. Open the HTML simulation in a web browser if it is provided as a separate file.

## 👨‍💻 Conclusion

This project demonstrates two approaches to solving the Dining Philosophers Problem. It helps explain how synchronization mechanisms coordinate concurrent processes and manage shared resources safely.

The project provides practical understanding of important Operating Systems concepts through implementation and visualization.
