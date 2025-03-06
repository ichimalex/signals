# Signal Processing in C++

## Overview
This C++ program implements a simple signal processing system. It allows for:
- Creating a signal with given samples.
- Computing the power of a signal.
- Adding noise to a signal.
- Performing convolution on signals.

## Features
- **Display Signal**: Prints the signal type and its sample values.
- **Compute Signal Power**: Calculates the average power of a signal.
- **Add Noise**: Generates a noisy signal by adding noise to the original signal.
- **Perform Convolution**: Computes the convolution of two signals.

## Classes

### `Semnal` (Signal Class)
- **Attributes**:
  - `tip` (Type of signal)
  - `nr_esantioane` (Number of samples)
  - `esantioane` (Array of sample values)

- **Methods**:
  - `Semnal(std::string tip, int nr_esantioane, float *esantioane)`: Constructor to initialize a signal.
  - `Semnal(const Semnal &s)`: Copy constructor.
  - `void display()`: Prints the signal's type and sample values.
  - `float putere_semnal()`: Computes the average power of the signal.
  - `int get_nr_esantioane()`: Returns the number of samples.
  - `float* get_esantioane()`: Returns the pointer to the signal’s samples.

### Functions

#### `Semnal adaugare_zgomot(Semnal semnal_util, Semnal semnal_zgomot)`
Creates a noisy signal by adding noise values to the original signal sample-by-sample.

#### `Semnal convolutie(Semnal semnal_util, Semnal semnal_util_zgomot)`
Computes the convolution of two signals by multiplying reversed samples.
