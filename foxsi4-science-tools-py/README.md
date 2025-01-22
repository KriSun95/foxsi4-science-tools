# `foxsi4-science-tools-py`

A repository to store all software tools for FOXSI-4 science in Python (woo, Python).

The tools being developed in Python should be placed in the `foxsi4_science_tools_py` folder (note the underscores and not dashes).

There is an "examples" and a "tests" folder. The "examples" folder is a great place to include scripts that show how some of the code in the repository works and the "tests" folder is a fantastic place to put code that tests the tools that have been created.

More information will be placed here with regards as to how this package is recommended to be used.

## Install tips

In order to work with some preliminary data, it would be instructive to set up a virtual environment (more information below) and install some packages needed. One way to do this is to:

1. Create an environment with `conda create -n foxsi4-science-tools-env python`.
2. Activating that environment with `conda activate foxsi4-science-tools-env`.
3. While in this directory with the `setup.py` file, the command `pip install -e .` will install the Python code into that environment.

## Namespace

The base `foxsi4_science_tools_py` namespace includes:

- `~foxsi4_science_tools_py.obsInfo`
  - The information stored in a YAML file that includes information from the flight and also the flare that was observed.

## Examples

```python
# importing the module is as easy as:
>>> import foxsi4_science_tools_py as f4st

# then accessing, e.g., the observational information for the flight/flare
>>> print(f4st.obsInfo)
{'flight': {'foxsi4': {'launch_time': {'utc': '2024-04-17T22:13:00', 'akdt':...}...}...}...}

# that can be accessed like a native Python dictionary
>>> print(f4st.obsInfo["flight"]["foxsi4"]["launch_time"]["clock"])
0
```

## A useful Python tip

It might be a good idea to look into ([conda](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)) virtual environments if you are not familiar, this includes looking into them yourself or getting in touch with someone to help explain.
