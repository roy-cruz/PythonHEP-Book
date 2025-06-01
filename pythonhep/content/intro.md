# Python for High Energy Physics

This Jupyter Book contains the course material for the "Python for High Energy Physics" (HEP) workshop, which will be offered as part of PURSUE 2025. The content is designed for students who have some familiarity with the basics of pure Python (i.e., standard Python without external libraries), but it does not require formal programming experience. The primary goal of this material and the associated workshop is to provide a solid foundation for students to begin working with widely used data analysis libraries such as NumPy and Matplotlib, as well as essential tools from the Scikit-HEP ecosystem. By the end of the workshop, students will be equipped to start exploring and analyzing HEP data.

Note: This Jupyter Book is designed to be used alongside an open Jupyter Notebook, allowing you to run code examples and experiment as you learn. 

## Setup

### CMSLPC Cluster

First, connect to the LPC cluster by running the following command.

```bash
ssh -L 8888:localhost:8888 <fermi_user>@cmslpc-el9.fnal.gov
```

Next, run the following command to setup a directory where you will work.

```bash
mkdir ~/nobackup/PURSUE-scikithep
cd ~/nobackup/PURSUE-scikithep
```

We now create the environment we will be using. To do this, run the following commands.

```bash
source /cvmfs/cms.cern.ch/cmsset_default.sh
cmsrel CMSSW_14_1_0_pre3
cd CMSSW_14_1_0_pre3/src
cmsenv
scram-venv
cmsenv
```

To clone this repository using the following commands

```bash
git clone git@github.com:roy-cruz/PURSUE-scikithep.git
cd PURSUE-scikithep
```

Proceed to open Jupyter Lab by running.

```bash
pip3 install jupyterlab
jupyter lab --no-browser --port=8888
```

Navigate to the link that appears in your terminal once it finishes starting up.

### Local

If you prefer working locally, you can use either pip or conda to setup your environment.

#### Using `venv` and `pip3`
In your working directory, create a virtual environment by running
```bash
python -m venv venv
```
and activate this environment by doing

```bash
source venv/bin/activate
```

Now clone the repository, and install the dependencies specified in the `requirements.txt` file.

```bash
git clone git@github.com:roy-cruz/PURSUE-scikithep.git
cd PURSUE-scikithep
pip3 install -r requirements.txt
```

Finally, start up Jupyter Lab and navigate to the link it provides you.

```bash
jupyter lab --no-browser
```

#### Using Conda

To make an environment in conda with all of the required libraries, just run the following commands in your working directory (Note: This may take a long time.)

```bash
git clone git@github.com:roy-cruz/PURSUE-scikithep.git
cd PURSUE-scikithep
conda env create -f environment.yml
```

After everything is done installing, activate the environment you just created by running

```bash
conda activate pursue-scikithep-2024
```

Start up Jupyter Lab by running
```bash
jupyter lab --no-browser
```
and navigate to the link that it provides you once it starts up.


```{tableofcontents}
```
