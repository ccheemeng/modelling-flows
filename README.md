# Modelling Flows  

This repo provides a notebook to graph material flows of unlimited types for a given system.  

## Installation  

### Using Conda  

Reproduced from [Conda's user guide](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file).

1. Create a Python environment:  
    ```shell
    conda create -n modelling-flows python=3.12
    ```

2. Activate the new environment:  
    ```shell
    conda activate modelling-flows
    ```

3. Verify that the new environment was installed correctly:  
    ```shell
    conda env list
    ```

    You can also use ```conda info --envs```.  

4. Install necessary packages:  
    ```shell
    conda install conda-forge::cxx-compiler graphviz ipykernel sqlite
    ```

5. Install Python libraries:
    ```shell
    pip install matplotlib networkx pygraphviz
    ```

### Colab  

A read-only [Colab notebook](https://colab.research.google.com/drive/1_uOuMpyyJK_tYM-QSFqZ7Nv6ASjIfi3F?usp=sharing) is provided with minor modifications to work on Colab.  

Make a copy in your Drive to use the notebook on your flows.  

## Inputs  

The notebook reads all ```.csv```s in a directory specified in the parameters.  

Make sure the input files adhere to the following constraints:  
* Each ```csv``` is named in the format ```name-of-flow.csv``` (all standard filename characters are allowed).  
* Each ```csv``` has a header row with 3 columns.  
* The first column of each ```csv``` defines the names of the nodes. Nodes in common across ```csv```s will represent the same node.  
* The second and third column of each ```csv``` represents the in and out flows per node. Each set of in/out flows per node is in the format ```ratio1 material1; ratio2 material2; ratio3 material3```.  

Example inputs are provided in [./flows/](./flows/).
