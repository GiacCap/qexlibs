# qexlibs
This is a meta repository that contains links to externally hosted libraries.


## List of libraries

| No.| Name         | URL                                                        | Documentation                                                    |
|--- |--------------|------------------------------------------------------------|------------------------------------------------------------------|
| 1. | QSE          | https://github.com/ICHEC/qse                               | https://ichec.github.io/qse                                      |
| 2. | QUEX         | https://github.com/ICHEC/quex                              | https://ichec.github.io/quex                                     |
| 3. | QCAP         | https://github.com/QCT-UEA-management/QCAP                 | https://munich-quantum-software-stack.github.io/MQSS-Interfaces/ |
| 4. | QC2          | https://github.com/qc2nl/qc2                               | https://qc2.readthedocs.io/en/latest/                            |
| 5. | QQuantLib    | https://github.com/NEASQC/FinancialApplications            | https://neasqc.github.io/FinancialApplications/dl.html           |
| 6. | WNTR-Quantum | https://github.com/quantumapplicationlab/wntr-quantum      | N/A (??)                                                         |
| 7. | QSVM4EO      | https://github.com.mcas.ms/ICHEC/qsvm4eo                   | N/A (??)                                                         |

## QSE

Quantum Simulation Environment (QSE) is developed at ICHEC, to explore analog quantum computing.

### Installation

QSE is available via `pip`, so one can install it by following commands in a python environment of one's choice -

```bash

pip install qse                   # basic installation
pip install "qse[pulser]"         # pulser backend
pip install "qse[myqlm]"          # myqlm backend
pip install "qse[myqlm,pulser]"   # both backends
```


## QUEX

Quantum Executor, provides classical simulated circuit runs, in a hardware agnostic way. It targets acceleration via `cupy` and `jax` and works on CPU, Nvidia GPUs and AMD GPUs.

```bash

pip install quex                # basic installation, Numpy
pip install "quex[nvidia]"       # nvidia backend, Cupy and Jax
pip install "quex[amd]"          # amd backend, Cupy and Jax
pip install "quex[metal]"        # apple-metal backend
```

## Exporting environment

The [pyproject.toml](./pyproject.toml) file can be used via `uv` package manager to maintain a cumulative dependencies of the libraries that we add.

If one needs a more traditional `requirements.txt` file to install the necessary libraries, one can export
on using -

```bash
uv export --format requirements.txt --no-hashes --output-file=requirements.txt 
```
