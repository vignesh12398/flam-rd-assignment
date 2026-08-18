# Flam R&D Assignment – Parametric Curve Estimation

## Objective

The objective of this assignment is to estimate the unknown
parameters θ, M, and X of a given parametric curve using the
provided x-y data.

The parameter ranges are:

- 0 < θ < 50°
- -0.05 < M < 0.05
- 0 < X < 100

The parameter t lies in the range:

6 < t < 60

## Methodology

The following approach was used:

1. Load the provided x-y dataset.
2. Sort the data points by x-coordinate so that the points follow
   the curve order.
3. Generate uniformly spaced values of t between 6 and 60.
4. Implement the given parametric equations using NumPy.
5. Define the L1 distance between the actual and predicted points
   as the objective function.
6. Use Differential Evolution from SciPy to minimize the L1 error.
7. Extract the optimized values of θ, M, and X.
8. Visualize the actual data and fitted parametric curve.

## Parametric Equations

x(t) = t cos(θ) - exp(M|t|) sin(0.3t) sin(θ) + X

y(t) = 42 + t sin(θ) + exp(M|t|) sin(0.3t) cos(θ)

## Optimization

Differential Evolution was used with the following parameter bounds:

| Parameter | Range |
|-----------|-------|
| θ | 0 to 50° |
| M | -0.05 to 0.05 |
| X | 0 to 100 |

The objective function minimizes the L1 distance:

L1 = Σ (|x_actual - x_predicted| + |y_actual - y_predicted|)

## Results

The optimized parameters obtained were approximately:

- θ = 30.043636°
- M = 0.029991
- X = 55.015520

Total L1 error:

453.4369

Mean L1 error per point:

0.3029

## Visualization

The notebook contains a visualization comparing the provided
data points with the fitted parametric curve.

## Files

- `flam_assignment.ipynb` – Complete Python implementation and analysis
- `xy_data.csv` – Provided dataset
