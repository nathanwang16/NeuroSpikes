


# Neural Spiking Simulation in Python

This project demonstrates how to simulate the activity of neurons using Python. It provides tools to generate spiking activity, model neural behavior using mathematical functions, and visualize the results. The code is modular and can be extended to simulate complex neural dynamics.

## Features

- **Spike Generation**: Simulate individual spikes lasting 1 ms.
- **Random Spiking**: Generate a random spike train based on a given spike probability.
- **Regular Spiking**: Model neurons that fire at fixed intervals (e.g., every 50 ms or 100 ms).
- **Sigmoid Function**: Use a sigmoid function to approximate neural spiking based on input voltage and a threshold.
- **Visualization**: Plot neural spiking activity over time, showing multiple neurons on the same graph with customizable colors and tick mark positions.

## Getting Started

### Prerequisites

- Python 3.8 or later
- Libraries:
  - `numpy`
  - `matplotlib`

### Installation

Install the required libraries using pip:

```bash
pip install numpy matplotlib
```

## Usage

### Simulate Spiking Activity

1. **Generate Random Spikes**:

   ```python
   spike_train_random = generate_spike_train(duration_ms=1000, spike_prob=0.1)
   ```
2. **Generate Regular Spikes**:

   ```python
   spike_train_50ms = generate_regular_spiking_activity(duration_ms=1000, interval_ms=50)
   ```
3. **Sigmoid Function for Voltage-Threshold Spiking**:

   ```python
   output = sigmoid(x=2.0, threshold=1.0, beta=10)
   ```

### Plot Neural Spiking Activity

1. **Plot a Single Neuron**:

   ```python
   plot_spike_train(spike_train_random)
   ```
2. **Plot Two Neurons on the Same Graph**:

   ```python
   plot_combined_spike_trains(
       spike_train_1=spike_train_random,
       y_value_1=1,
       color_1='black',
       label_1='Neuron 1 (Random Spiking)',
       spike_train_2=spike_train_50ms,
       y_value_2=2,
       color_2='blue',
       label_2='Neuron 2 (Spikes every 50ms)'
   )
   ```

## Examples

- **Random Spiking Activity**:
  ![Random Spiking Example](path/to/random_spiking.png)
- **Regular Spiking Activity**:
  ![Regular Spiking Example](path/to/regular_spiking.png)

## What You Can Learn

1. How to simulate neural spiking behavior using Python.
2. Use of the sigmoid function to approximate neural threshold behavior.
3. Techniques for plotting and visualizing spiking activity in a clear, interpretable format.
4. Modular code structure for simulating complex neuron models.

## Extend This Project

- Add more biologically realistic neuron models (e.g., integrate-and-fire models).
- Incorporate external stimuli to drive spiking behavior.
- Simulate networks of interconnected neurons.

## License

This project is open-source and available under the GNU License.
