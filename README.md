
<!-- README.md is generated from README.Rmd. Please edit that file -->

<a href="https://travis-ci.org/dynverse/dynwrap"><img src="https://travis-ci.org/dynverse/dynwrap.svg" align="left"></a>
<a href="https://codecov.io/gh/dynverse/dynwrap">
<img src="https://codecov.io/gh/dynverse/dynwrap/branch/master/graph/badge.svg" align="left" /></a>
[**ℹ️ Tutorials**](https://dynverse.org)     [**ℹ️ Reference
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

![](man/figures/overview_wrapping_v3.png)

The advantage of using a common model is that it allows:

  - Comparison between a prediction and a gold standard, eg. using
    [dyneval](https://www.github.com/dynverse/dyneval)
  - Comparing two predictions
  - Easily visualise the trajectory, eg. using
    [dynplot](https://www.github.com/dynverse/dynplot)
  - Extracting relevant features/genes, eg. using
    [dynfeature](https://www.github.com/dynverse/dynfeature)

## Latest changes

Check out `news(package = "dynwrap")` or [NEWS.md](NEWS.md) for a full
list of changes.

<!-- This section gets automatically generated from inst/NEWS.md -->

### Recent changes in dynwrap 1.2 (unreleased)

#### Documentation

  - Added examples to all functions

#### New features

  - Improved RNA velocity handling:
      - Not all features need to be present in the projected expression,
        allowing integration with standard velocyto.R pipelines

### Recent changes in dynwrap 1.1.4 (27-06-2019)

  - BUG FIX: Fixed \#142 where the error message was
truncated

## Dynverse dependencies

<!-- Generated by "update_dependency_graphs.R" in the main dynverse repo -->

![](man/figures/dependencies.png)
