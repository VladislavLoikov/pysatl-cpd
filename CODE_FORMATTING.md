# PySATL CPD project code formatting guide

This document describes the standards for coding in the project.
Please follow them when working on the project.

# Modules

Each article should begin with a title that includes a brief description, author information, license, and editing rights.
```python
"""
Modul for ...
"""
__author__ = "<author_name>"
__copyright__ = "Copyright (c) 2025 PySATL project"
__license__ = "SPDX-License-Identifier: MIT"
```

# Packages, `__init__.py` files and imports

Each package must contain an `__init__.py` file, which, like the module, has an information header.

To create a good API, do not leave init files empty.[Official documentation on working with modules and packages](https://docs.python.org/3/tutorial/modules.html#standard-modules). For example:
```python
from pysatl_cpd.core.algorithms.abstract_algorithm import Algorithm
from pysatl_cpd.core.algorithms.bayesian_algorithm import BayesianAlgorithm
from pysatl_cpd.core.algorithms.bayesian_linear_heuristic import BayesianLinearHeuristic
from pysatl_cpd.core.algorithms.bayesian_online_algorithm import BayesianOnline
from pysatl_cpd.core.algorithms.classification_algorithm import ClassificationAlgorithm
from pysatl_cpd.core.algorithms.graph_algorithm import GraphAlgorithm
from pysatl_cpd.core.algorithms.kliep_algorithm import KliepAlgorithm
from pysatl_cpd.core.algorithms.knn_algorithm import KNNAlgorithm
from pysatl_cpd.core.algorithms.online_algorithm import OnlineAlgorithm
from pysatl_cpd.core.algorithms.rulsif_algorithm import RulsifAlgorithm

__all__ = [
    "Algorithm",
    "BayesianAlgorithm",
    "BayesianLinearHeuristic",
    "BayesianOnline",
    "ClassificationAlgorithm",
    "GraphAlgorithm",
    "KNNAlgorithm",
    "KliepAlgorithm",
    "OnlineAlgorithm",
    "RulsifAlgorithm",
]
```
# Don't mix absolute and relative paths in imports.Use only absolute imports

```python
from pysatl_cpd.core import CpdCore, CpdProblem
from pysatl_cpd.core.algorithms import Algorithm
from pysatl_cpd.core.scrubber import LabeledDataProvider, Scrubber
from pysatl_cpd.icpd_solver import CpdLocalizationResults, ICpdSolver
from pysatl_cpd.labeled_data import LabeledCpdData

```

# Also use a consistent style for class/module names (if one exists). For example, all abstract class names start with `I`
