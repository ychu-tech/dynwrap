
<!-- README.md is generated from README.Rmd. Please edit that file -->

<a href="https://travis-ci.org/dynverse/dynwrap"><img src="https://travis-ci.org/dynverse/dynwrap.svg" align="left"></a>
<a href="https://codecov.io/gh/dynverse/dynwrap">
<img src="https://codecov.io/gh/dynverse/dynwrap/branch/master/graph/badge.svg" align="left" /></a>
  | [**ℹ️ Tutorials**](https://dynverse.org) | [**ℹ️ Reference
documentation**](https://dynverse.org/reference/dynwrap)
<br><img src="man/figures/logo.png" align="right" />

# Tools for inferring and wrapping single-cell trajectories

**dynwrap** contains the code for a common model of single-cell
trajectories. The package can:

  - Wrap the input data of a trajectory inference method, such as
    expression and prior information
  - Run a trajectory inference method in R, in a docker container or a
    singularity container
  - Wrap the output of a trajectory inference method, such as the
    pseudotime, a clustering or a branch network, and convert it into a
    common trajectory model
  - Further postprocess and adapt the trajectory model, such as
    labelling the milestones and rooting the trajectory

![](man/figures/trajectory_model.png)

Documentation and the API reference for dynwrap can be found at the
dyvnerse documentation website: <https://dynverse.org/> .

dynwrap was used to wrap 50+ trajectory inference method within docker
containers in [dynmethods](https://github.com/dynverse/dynmethods).

![](man/figures/overview_wrapping_v2.png)

The advantage of using a common model is that it allows:

  - Comparison between a prediction and a gold standard, eg. using
    [dyneval](https://www.github.com/dynverse/dyneval)
  - Comparing two predictions
  - Easily visualise the trajectory, eg. using
    [dynplot](https://www.github.com/dynverse/dynplot)
  - Extracting relevant features/genes, eg. using
    [dynfeature](https://www.github.com/dynverse/dynfeature)

## Latest changes

Check out `news(package = "dynwrap")` or [NEWS.md](inst/NEWS.md) for a
full list of
changes.

<!-- This section gets automatically generated from inst/NEWS.md, and also generates inst/NEWS -->

### Recent changes in dynwrap 1.0.0 (28-03-2019)

  - MAJOR CHANGE: Add support for Singularity 3.0, drop support for
    previous releases of Singularity and singularity-hub.

  - MAJOR CHANGE: dynwrap now always works with sparse count and
    expression matrices

  - FEATURE: Add `create_ti_method_definition()` to create a definition
    from a local script.

  - DOCUMENTATION: Major update of all documentation for dynbenchmark
    publication

  - MINOR CHANGE: Rename `compute_tented_geodesic_distances()` to
    `calculate_geodesic_distances()`

  - MINOR CHANGE: Harmonisation of function arguments to either
    `dataset` or `trajectory`

### Recent changes in dynwrap 0.3.1.2 (01-02-2019)

  - BUG FIX: `simplify_replace_edges()` would sometimes swap edges in
    milestone network around, but forget invert percentages.

  - BUG FIX: Close sinks when interupting the R process

  - MINOR CHANGE: Work with new babelwhale, which includes support for
    singularity
3.0

## Dynverse dependencies

<!-- Generated by "update_dependency_graphs.R" in the main dynverse repo -->

![](man/figures/dependencies.png)
