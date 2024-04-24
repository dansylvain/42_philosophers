# 42_philosophers
the dining philosophers problem - threads coordination

# Philosophers Project Documentation

## Introduction

The "philosophers" project is an implementation of the dining philosophers problem in C. The dining philosophers problem is a classic synchronization problem in computer science, which illustrates the challenges of resource allocation and deadlock avoidance in concurrent systems.

In this project, I provide a solution to the dining philosophers problem using C programming language. The goal is to simulate the behavior of philosophers sitting around a dining table, where each philosopher alternates between thinking and eating. However, there is a limited number of forks available, and a philosopher can only eat if they have both the fork to their left and right. This leads to potential deadlock situations if not properly managed.

My implementation aims to demonstrate one synchronization technique to prevent deadlocks and ensure the safety and liveness of the philosophers' dining process. Through this project, users can explore fundamental concepts of concurrency and synchronization in a practical setting.

## Execution

### Cloning the Repository

To get started with the project, clone the repository from GitHub using the following command:

```bash
git clone <repository_url>
```

### Compiling the Project

Navigate to the project directory and compile the source code using the Makefile:
```bash
cd philosophers
make
```
### Running the Program
Once compiled successfully, execute the program by running the generated executable:
```bash
./philo 4 800 200 200 5
```

## Dependencies
My implementation of the "philosophers" project includes all necessary dependencies within the source code, requiring no additional installations.

## Usage
The "philosophers" program takes the following command-line arguments:

- `number_of_philosophers`: The number of philosophers and also the number of forks.
- `time_to_die` (in milliseconds): If a philosopher hasn’t started eating within `time_to_die` milliseconds since the beginning of their last meal or the start of the simulation, they die.
- `time_to_eat` (in milliseconds): The time it takes for a philosopher to eat. During this time, they must hold two forks.
- `time_to_sleep` (in milliseconds): The time a philosopher spends sleeping.
- `[number_of_times_each_philosopher_must_eat]` (optional): If specified, all philosophers must eat at least this many times before the simulation stops. If not specified, the simulation stops when a philosopher dies. <br><br>
**as such:**
```bash
./philo <number_of_philosophers> <time_to_die> <time_to_eat> <time_to_sleep> [number_of_times_each_philosopher_must_eat]
```
**Example usage:**

```bash
./philo 4 800 200 200 5
```
