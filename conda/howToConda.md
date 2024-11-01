# Conda

## What is it?
Conda is an open-source package and environment management software. 
- Anaconda is an offshoot of conda.
- Miniconda is a light version of Anaconda.

## Environments
Environments can be thought of as different rooms that you run code in. 

Let's pretend you want to run two R-scripts, but each requires a different version. You can set up a different environment using conda, install the other version of R in that one, and then run your scripts simultaneously but in their respective rooms. If you didn't use conda, for example on HPC, then you could only use whatever version of R that HPC is running.

### Downlaod conda
I personally use Anaconda, which can be downloaded from [here](https://www.anaconda.com/download/success) (you can skip the registration it shows).

### Ensure conda is installed correctly
1. Open a terminal.
   1. If using Visual Studio Code run `ctrl/cmd` + `j`.
      1. If using Windows, change the default terminal in VSCode to be command prompt (instead of powershell). See [here](https://stackoverflow.com/questions/44435697/change-the-default-terminal-in-visual-studio-code) for a guide with pictures.
   2. Type `conda --version`. If you get an error that conda is not recognized, you need to add the correct paths to your Environment Variables (this is primarily for Windows) - (see [here](https://stackoverflow.com/questions/44515769/conda-is-not-recognized-as-internal-or-external-command) and [here](https://stackoverflow.com/questions/44597662/conda-command-is-not-recognized-on-windows-10)).

### Create conda environment
You can create an environment either from a `.yml` file with specified packages already, or you can create an empty one and then load your packages as you need. The [documentation](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) details both of these methods, but see this example `.yml` file [here](https://github.com/mcgregorian1/codePractices/blob/main/conda/sampleCondaEnv.yml).

Remember! Once you've created an environment, you need to type `conda activate <yourEnvironmentName>` in order to code within it. When finished, run `conda deactivate`.
