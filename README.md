# irregular-searchspace-pipeline
 Pipeline for working with irregular search spaces in Platypus-Opt genetic optimisation

## Genetic optimisation in irregular search spaces
Working with platypus-opt, search spaces are assumed to be rectangular. This means irregular search spaces are assumed to have a regular shape, meaning some solutions may exist outside the known space. This pipeline suggests a method for adding an `intersection` objective to a genetic optimisation problem, encouraging solutions to maximise overlap with the search space. 

| | | | |
|:---:|:---:|:---:|:---:|
| ![](/.github/README/shape.png) | ![](/.github/README/outlined.png) | ![](/.github/README/bad%20intersection.png) | ![](/.github/README/good%20intersection.png) |
| An irregular search space. | A boundary outlining the search space. | A solution hardly intersecting search space. | A solution with good intersection of the search space. |

## Blog post
Read about this pipeline in greater detail at [https://cutwell.github.io/spatial-data-boundary/](https://cutwell.github.io/spatial-data-boundary/). 

## Pipeline
1. Follow `get_alpha_shape.ipynb` to produce a set of boundary coordinates for your search space.
2. View `optimise_irregular_space.ipynb` for a simple optimisation problem to find polygons which fit inside the search space. 