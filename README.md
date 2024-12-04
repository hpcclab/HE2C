# HE2C: A Holistic Approach for Allocating Latency-Sensitive AI Tasks across Edge-Cloud

## Introduction
The HE2C framework is a comprehensive solution designed to address the latency, memory, accuracy, throughput, and energy challenges of Deep Learning (DL) applications across the edge-to-cloud continuum.
Unlike previous approaches that optimize single metrics, HE2C integrates multiple modules to ensure high performance and energy efficiency for latency-sensitive AI tasks.
Key features include:
- **Feasibility-check module** evaluates the likelihood of meeting task deadlines across edge and cloud resources.
- **Resource allocation strategy** ensures optimal task execution by dynamically distributing tasks across edge and cloud resources.
- **Rescue module** trades accuracy for latency to enhance throughput in constrained scenarios.

## Installation
### Prerequisites
- A heterogeneous computing environment with both edge devices and cloud servers.
- Python-based simulation frameworks, such as E2C Simulator (see [E2C-Sim documentation](https://github.com/hpcclab/E2C-Sim)) for evaluating edge-to-cloud workflows.

### Required Libraries
- Python libraries for task profiling and performance evaluation:
  - `numpy`, `scikit-learn`, and `matplotlib` for statistical modeling and visualization.
  - Custom task management scripts included in the project repository.
 
### Deployment
To deploy HE2C, run the following commands:
1. clone the repository:
```
git clone https://github.com/<repository-url>.git
cd he2c-framework
```
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Configure the system for task profiling and workload simulation by modifying `config.json`.
4. Run the simulation or deploy on real-world edge-cloud environments using the command:
```
python main.py --config config.json
```

## Usage
### Task Profiling
- Use the profiling module to analyze incoming tasks' parameters (e.g., deadlines, resource demands).
- Update configuration files with profiling results to optimize resource allocation.
### Feasibility Checking
- Evaluate tasks using cloud and edge feasibility checkers:
  - Cloud Feasibility considers energy and latency constraints.
  - Edge Feasibility considers memory, latency, and energy constraints.
### Task Allocation
- Leverage the `decision maker` for task distribution between edge and cloud:
    - Incorporates `energy-accuracy trade-off handler` based on task requirements.
