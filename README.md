# Smart City Traffic and Emergency Response AI System

A terminal-based Artificial Intelligence system that manages traffic routing, emergency response, and traffic signal allocation in a simulated smart city environment.

Developed as a final project for **AL-2002 Artificial Intelligence Lab**, this project demonstrates multiple AI techniques working together in a unified decision-making pipeline.

---

## Overview

The system accepts different types of city service requests and automatically routes them through the required AI modules to generate intelligent decisions.

Users can:

- Find optimal routes between locations
- Validate vehicle permissions and policies
- Allocate traffic signal phases
- Handle emergency response requests
- Run integrated city service scenarios
- Execute built-in demonstration cases

The system combines Artificial Neural Networks, Knowledge-Based Systems, Constraint Satisfaction Problems, and Search Algorithms into a single intelligent workflow.

---

## Features

### Route Planning
Finds the best path between locations using different search algorithms depending on vehicle type and priority.

### Emergency Response
Processes emergency requests through multiple AI modules to determine priority, validate rules, allocate traffic signals, and generate optimal routes.

### Traffic Signal Scheduling
Uses Constraint Satisfaction Problem (CSP) techniques to assign traffic signal phases while maintaining safety and operational constraints.

### Policy Validation
Checks whether vehicles are authorized to access specific locations or zones using rule-based reasoning.

### Integrated AI Pipeline
Automatically activates only the AI modules required for a particular request.

---

## Request Types

### 1. Route Request
Finds the optimal route for civilian vehicles.

### 2. Policy Check
Validates whether a vehicle is allowed to operate in a specified zone.

### 3. Control Allocation
Uses the CSP Scheduler to assign traffic signal phases along a route.

### 4. Emergency Response
Runs the complete AI pipeline:

- Priority Prediction
- Rule Validation
- Traffic Signal Allocation
- Route Planning

### 5. Integrated City Service
Processes combined smart city service requests through the full pipeline.

### 6. Demo Scenarios
Runs pre-configured demonstration cases without requiring manual input.

---

# AI Modules

The system consists of seven AI modules that work together as a processing pipeline.

## 1. Input Preprocessing Module

Responsibilities:

- Validates user input
- Cleans request data
- Encodes features into numerical values
- Prepares data for AI processing

---

## 2. Request Router

Responsibilities:

- Determines request category
- Selects the required AI modules
- Creates the execution pipeline

Example:

- Route Request → Search Module Only
- Emergency Request → Full AI Pipeline

---

## 3. ANN Priority Module

A hand-built Artificial Neural Network implemented entirely from scratch without machine learning libraries.

### Features

- Sigmoid Activation
- ReLU Activation
- Softmax Output Layer

### Priority Classes

- Low
- Normal
- High
- Critical

### Network Structure

#### Binary Classifier
Determines whether elevated priority exists.

#### Multi-Class Classifier
Predicts the exact priority level.

---

## 4. Knowledge Base Module

A rule-based expert system that validates requests using logical rules.

### Example Rules

- Is the vehicle an emergency vehicle?
- Is the destination a hospital?
- Does the predicted priority match the declared severity?

The module approves or rejects requests based on these facts.

---

## 5. CSP Scheduler Module

Treats traffic signal allocation as a Constraint Satisfaction Problem.

### Constraints

- Adjacent intersections cannot use the same signal phase.
- Emergency corridors receive priority.
- Signal assignments must remain conflict-free.

### Technique

- Backtracking Search

---

## 6. Search and Navigation Module

Computes optimal routes through the city road network.

### Algorithms Used

#### BFS (Breadth-First Search)
Used for civilian vehicles on unweighted paths.

#### UCS (Uniform Cost Search)
Used when road weights must be considered.

#### A* Search
Used for emergency vehicles to find the fastest route.

---

## 7. Final Response Layer

Collects outputs from all active modules and generates a readable response containing:

- Priority Level
- Approval Status
- Signal Allocation Plan
- Route Information
- Warnings and Recommendations

---

# Project Structure

```text
smart_city_traffic_AI/
│
├── main.py
│
└── modules/
    ├── input_preprocessing.py
    ├── request_router.py
    ├── ann_priority.py
    ├── knowledge_base.py
    ├── csp_scheduler.py
    ├── search_navigation.py
    └── final_response.py
```

---

# City Locations

The simulated city contains 13 interconnected locations:

1. Central Junction
2. North Station
3. East Market
4. South Residential
5. River Bridge
6. City Hospital
7. Police HQ
8. Fire Station
9. Traffic Control Center
10. Airport Road
11. West Terminal
12. Industrial Zone
13. Stadium

---

# How to Run

## Requirements

- Python 3.x
- No external libraries required

## Run the Project

```bash
python main.py
```

Then:

1. Select a request type from the menu.
2. Enter the required information.
3. View the generated AI response.

To run the built-in demonstration scenarios, select:

```text
Option 6
```

from the main menu.

---

# Technologies Used

- Python
- Artificial Intelligence
- Artificial Neural Networks (ANN)
- Knowledge-Based Systems
- Constraint Satisfaction Problems (CSP)
- Breadth-First Search (BFS)
- Uniform Cost Search (UCS)
- A* Search Algorithm

---

# Academic Project

This project was developed for:

**AL-2002 – Artificial Intelligence Lab**

The objective was to integrate multiple AI techniques into a single intelligent smart city management system capable of handling routing, emergency response, traffic control, and policy validation tasks.

---

## Author

**Moeen Arshad**

GitHub: https://github.com/moeenarshad2005
