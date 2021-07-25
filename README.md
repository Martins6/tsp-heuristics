# tsp-heuristics

Python Package of meta-heuristics applied to the Travelling Salesman Problem (TSP). The TSP problems arise from the hypothetical challenge that a merchant wants to visit a collection of cities but only visit once each one of them and then come straight back home. How could he do this by minimizing the distance traveled?

# Heuristics

The following heuristics are implemented:

* Greedy algorithm or Nearest Neighbor. (**nn_algo**)
* Local Search with 2-opt: Best improvement and First Improvement (**local_search_algo**).
* Greedy Randomized Adaptive Search Procedure (GRASP) (**solve_tsp_grasp**).

# Using

First install through pip through:

```bash
pip install tsp-heuristics
```

Then use the functions like so:

```python
tsplib_file = "tests/test_data/a280.tsp"
distance_matrix = tsplib_distance_matrix(tsplib_file)

print(solve_tsp_grasp(distance_matrix))

initial_tour = nn_algo(distance_matrix)[0]
print(local_search_algo(initial_tour, distance_matrix, method='first improvement'))
```